# Arduino-BME680-Weather-Station

Project inspired the article published in this [how2electronics.com article](https://how2electronics.com/esp32-bme680-weather-station-iaq-monitoring-on-mqtt/) for the Arduino ESP32 and BME680 sensor.

In the provided example, the endpoint wouldn't be able to process all the parameters sent that frequently. This resulted in some of the parameters never reaching the endpoint, most frequently the ones transmitted the latest. Also, sending that frequently the measurements, it would lead to overloading the free tier of Ubidots, resulting in plenty of measurements being lost.

Fixed the overload of measurements by sequencing the reading of each parameter, and added a LED visual confirmation when a new measurement is transmitted.
