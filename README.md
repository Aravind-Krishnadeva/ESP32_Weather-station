# ESP32_Weather-station

### Objective
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
The objective of this project is to build a compact, battery powered ESP32 based weather station module

![weather station](https://user-images.githubusercontent.com/26503600/229715483-0b4ea387-03f1-424f-8ad8-accac3342967.jpg)



### Requirements / functional specifications
1. The module has to measure environmental parameters such as temperature, humidity, atmospheric pressure, as well as battery voltage
2. The module is powered with a li battery rated 3.7V
3. The module has 3 onboard led indicators, one while led that displays data transfer, red led for battery low indication and green led for battery good display


### Firmware flow
1. Read battery voltage [ function 1: battery_check ]
2. If battery voltage is good (3.7V ), read sensor values [ function 2: sensor_read ]
3. Display sensor data on OLED screen


