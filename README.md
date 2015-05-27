# Desk Sensor Stuff
This repo contains the Arduino code for the RFu328 ultrasonic desk sensor as well as the Node-RED flow for the hub device and the PCB EAGLE files.

Check out localhost:1880/status for output from the sensors.

https://cloud.githubusercontent.com/assets/6317446/7678626/92cf6eda-fd4d-11e4-8980-ae222dfc567b.jpg

Big acknowledgement of Oxford Flood Network, ThingInnovations and Andrew Lesley for great examples.


PS for the EAGLE files: board v3 was designed to take 6-12V input and use two Wirelessthings PowerPods (PowerPOD 1117) to transform to 3.3V (for the RFu328) and 5V (for the HC-SR04 ultrasonic device). However, it was found that these down-regulating pods have unacceptable quiescent currents. We now use board v3 with a bridge (connecting Vin to Vout for the designated 3.3V  pod), and put a PowerPOD NCP1402 to transform incoming 3.6V from a SAFT battery to 5V.

There's a board v4 with a transistor to control the quiescent draw of either ultrasonic or PIR sensors.
