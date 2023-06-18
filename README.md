# ESP32_Weather-station

### Objective
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
The objective of this project is to build a compact, battery powered ESP32 based weather station module that is driven by micropython which loads sensor data to an adarfuit IO cloud using MQTT
![20230518_133924](https://github.com/Aravind-Krishnadeva/ESP32_Weather-station/assets/26503600/8ee60086-a6c7-42ce-829d-e6a6d7a9b152)






### Requirements / functional specifications
1. The module has to measure environmental parameters such as temperature , humidity as well as battery voltage.
2. The module is powered with a li 18560 battery rated 3.7V
3. The module has 2 onboard led indicators, green led that displays battery good condition and  red led for battery low indication.
4. The module has to transmit the sensor data on request, only when an external push button is pressed. 


### Event controlled Firmware flow
1. The controller remains in sleep mode ..........[ main loop]
2. When push button is triggered, the interrupt handler is executed.......... [ button_interrupt_handler]
3. The battery voltage is sensed at first. If battery voltage is in the range of 3.5 to 3.7V, green led turns ON and reads sensor data.
4. If battery voltage is less, the system does not read sensor data and displays an error message.
5. After displaying sensor data, system again goes back to sleep ..... [ main loop]


