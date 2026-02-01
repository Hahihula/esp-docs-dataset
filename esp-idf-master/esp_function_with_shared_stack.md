---
original_file_path: api-reference/system/esp_function_with_shared_stack.rst
---

# Call Function with External Stack

`zh_CN:[中文]`{.interpreted-text role="link_to_translation"}

## Overview

A given function can be executed with a user-allocated stack space which is independent of current task\'s stack. This mechanism helps reduce stack usage for tasks that call common functions with heavy stack demands such as `printf`. The given function can be executed on the shared stack space by calling `esp_execute_shared_stack_function`{.interpreted-text role="cpp:func"} and passing it as a parameter.

::::: warning
::: title
Warning
:::

`esp_execute_shared_stack_function`{.interpreted-text role="cpp:func"} does only minimal preparation of the provided shared stack memory. The function passed to it for execution on the shared stack space or any of that function\'s callees should not do any of the following:

::: list
\- Use thread-local storage :esp32p4: - Use the floating-point unit :esp32p4: - Use the AI co-processor - Call vTaskDelete(NULL) to delete the currently running task
:::

Furthermore, backtraces will be wrong when called from the function running on the shared stack or any of its callees. The limitations are quite severe, so that we might deprecate `esp_execute_shared_stack_function`{.interpreted-text role="cpp:func"} in the future. If you have any use case which can only be implemented using `esp_execute_shared_stack_function`{.interpreted-text role="cpp:func"}, please open a [GitHub Issue](https://github.com/espressif/esp-idf/issues).
:::::

## Usage

`esp_execute_shared_stack_function`{.interpreted-text role="cpp:func"} takes four arguments:

- a mutex object allocated by the caller, which is used to protect the shared stack space
- a pointer to the stack used for that function
- the size of stack in bytes
- a pointer to the shared stack function

The user-defined function is executed immediately as a callback, using a user‑allocated stack instead of the current task's stack.

The usage may look like the code below:

``` c
void external_stack_function(void)
{
    printf("Executing this printf from external stack! \n");
}

//Let us suppose we want to call printf using a separated stack space
//allowing the app to reduce its stack size.
void app_main()
{
    //Allocate a stack buffer, from heap or as a static form:
    StackType_t *shared_stack = malloc(8192 * sizeof(StackType_t));
    assert(shared_stack != NULL);

    //Allocate a mutex to protect its usage:
    SemaphoreHandle_t printf_lock = xSemaphoreCreateMutex();
    assert(printf_lock != NULL);

    //Call the desired function using the macro helper:
    esp_execute_shared_stack_function(printf_lock,
                                    shared_stack,
                                    8192,
                                    external_stack_function);

    vSemaphoreDelete(printf_lock);
    free(shared_stack);
}
```

## API Reference {#esp-call-with-stack-basic_usage}

::: include-build-file
inc/esp_expression_with_stack.inc
:::
