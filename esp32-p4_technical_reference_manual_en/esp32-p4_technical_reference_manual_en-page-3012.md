

```markdown
# Chapter 61  
## Temperature Sensor (TSENS)  

### 61.1 Overview  
ESP32-P4 provides a temperature sensor for real-time monitoring of temperature changes within the chip. The sensor converts analog voltage to digital values and provides compensation for temperature offsets.  

### 61.2 Features  
The temperature sensor has the following features:  
- Software-triggered temperature measurement, which once triggered, the sensor continuously measures temperature. Software can read the data at any time.  
- Hardware-triggered automatic temperature monitoring, supporting two wake-up modes  
- Configurable temperature offset based on the application scenario for improved accuracy  
- Configurable temperature measurement range  
- Support for Event Task Matrix (ETM)-related events and tasks  

### 61.3 Architecture  
Figure 61.3-1 shows the internal structure of the temperature sensor.
```