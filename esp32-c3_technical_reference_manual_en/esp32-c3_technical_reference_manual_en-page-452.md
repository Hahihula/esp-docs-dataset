

```markdown
overflow and loop mode is enabled, ASSIST_DEBUG_LOG_MEM_CURRENT_ADDR_REG is the starting address of the first packet.

* Read and parse data from the starting address. Read 128 bits each time.
* Use START_FLAG to determine the starting bit of the first packet. Starting bit = START_FLAG * 25 + 3.

Note that START_FLAG is only used to locate the starting bit of the first packet. Once the starting bit is located, START_FLAG should be filtered out in the subsequent data.

After packet parsing is completed, clear the ASSIST_DEBUG_LOG_MEM_FULL_FLAG flag bit by setting ASSIST_DEBUG_CLR_LOG_MEM_FULL_FLAG.
```