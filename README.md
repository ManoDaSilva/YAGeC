# YAGC
Yet Another Geiger Counter - simple design for integration as a sensor into other projects.
Created using EasyEDA 

## Schematic - hardware design
Design is based off a random number generator [I made some time ago](https://github.com/ManoDaSilva/RNG), based off [DIYGeigerCounter's design](https://sites.google.com/site/diygeigercounter/technical/circuit-description?authuser=0)
![Schematic](img/schematic.png?raw=true "Schematic")



## PCB
Here's the PCB for the first version. It integrates a buzzer, an LED for quick feedback, as well as an FPC connector to use the counter as an integrated sensor.
![Main Board](img/main_board.jpg?raw=true "Main Board")
The PFC connector uses the following pinout:
1. VCC
2. VBATT
3. MCU_D2: Raw pulses out, 130µs/count (active low)
4. MCU_A2: Streched pulses out, 2ms/count
5. MCU_D12: Speaker out
6. MCU_D9: Power supply disable (pull low to disable)
7. NC
8. GND

As for the jumpers:

* SJ1 is a "Speaker Select" jumper. It can either be driven by the counter, or by the external PFC input. 
* SJ2 connects the "Power Supply Disable" pin to the PFC
* SJ3 decouples VCC from VBATT, and allows to use the BATT pads to power something else through the PFC header.



