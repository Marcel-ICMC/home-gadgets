talk about
* inspiration
The inspiration behind this one is keeping a breeze for plants. I didn't know this before this project but wind isn't only important to plants for carrying seeds and pollen, it also helps stregthen their stems giving it more structure. Also by having a constant breeze blowing there's less chances of insects choosing the place as their food source and the air exchange help avoid harmful fungis from overtaking the plants resources.


* wiring
3 Cooler Master, SickleFlow MF140
12v power supply rated with 4A current, this was more than enough 
ESP32-S3 SupmerMini
LM2596 Buck converter
AO3407 P-Channel MOSFET
AO3400 N-Channel MOSFET

12V+ -> LM2596+
LM2596+ -> ESP32 3.3v pin
ESP32 -> GND
ESP32 GPIO12 -> 100Ohm -> Gate of AO3400
AO3400 Source -> GND
AO3400 Drain -> 1kOhm -> 12V+
AO3400 Drain -> AO3407 Gate
AO3407 Source -> 12V+
AO3407 Drain -> 1kOhm -> GND
AO3407 Drain -> Fans 12v+ pin
Fans GND -> GND
ESP32 GPIO10 -> 1kOhm -> Fans PWM pin
ESP32 (Confirm which pin was used)-> 10kOhm -> Tach

* yaml file
* challenges
* End result