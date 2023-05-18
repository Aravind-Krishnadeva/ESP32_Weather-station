# ESP32_Weather-station

### Objective
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
The objective of this project is to build a compact, battery powered ESP32 based weather station module
![20230518_133924](https://github.com/Aravind-Krishnadeva/ESP32_Weather-station/assets/26503600/8ee60086-a6c7-42ce-829d-e6a6d7a9b152)






### Requirements / functional specifications
1. The module has to measure environmental parameters such as temperature, humidity, atmospheric pressure, as well as battery voltage
2. The module is powered with a li battery rated 3.7V
3. The module has 3 onboard led indicators, one while led that displays data transfer, red led for battery low indication and green led for battery good display


### Firmware flow
1. Read battery voltage [ function 1: battery_check ]
2. If battery voltage is in the range of 3.5 to 3.7V (Battery good) turn on green led and  read sensor values [ function 2: sensor_read ]
3. Send sensor values to monochrome lcd display [ function 3: display_lcd ]
4. If battery voltage is less than 3.5V, turn on red led, do not display sensor values and print an error message on the lcd screen
5. Repeat the above process from 1 to 4


