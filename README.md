# multiple-DS18B20-auto-setup-via-MQTT
very easy setup for temperture ds1820 temperature sensor automatically detects and sends MQTT topic based on the ROM id of the sensor.  it will  auto detect and send as soon as  a new sensor is plug in.  at restart it broadcast the sensor ID and topic  descrition  for the sensors at the on the MQTT topic called ID


it simple to use - just modify the wifi and mqtt setting to match your own. and that's pretty much it.
once it connects to wifi and publishes to it, you can easily grab the topic name for each individual ds1820 by simply subscribing to the topic /ID/ from there it will publish the topic of the temperature sensor 20 times then not publish it any more until the device restarts.
it supports up display of 20 DS18b20 ( you can increase that by editing the the sketch count)  but will detect as many DS18b20 sensors that your device can support and automatically transmit temperature info via MQTT even if you do not edit the count-- it just will not list the topics of the  ones  after the first 20 
