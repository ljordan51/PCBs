AIL/Precharge - Controls and powers accumulator indicator light with the high voltage (HV) part of the car in order to switch on an LED when the high voltage system on the car reaches 60V. Circuit is designed to be able to function up to 300V (max pack voltage). Currently turns light on at 35V due to the characteristic of the LDO but this issue could be solved by adding a 20-25V Zener diode before the LDO. Additionally, the board contains the precharge circuit which charges the capacitive load of the motor controller before closing the accumulator isolation relays connecting the battery to the rest of the HV circuit.

TSAL - Controls (with HV) and powers (with grounded low voltage (GLV)) the tractive system active light in order to switch on a super bright, flashing indicator light when the high voltage system on the car reaches 60V. Circuit is designed to be able to function up to 300V (max pack voltage). The light must be controlled by the HV but powered by the GLV due to the high current draw.

MSPM - The master switch panel monitor uses an ATmega microcontroller and shutdown sensing transistors in order to communicate which points in the shutdown circuit are receiving GLV and send that information through CAN messaging to the dashboard.

2018_Example_Project - This PCB was designed as part of my role as Electrical Design Lead for Olin College's Formula SAE Electric Vehical Racing Team to introduce new team members to basic electrical circuits, schematic capture, and layout. It includes a 12-5V switching regulator which is standard on all our boards with microcontrollers. Additionally, it has a basic non-inverting amplifier, RC LED delay circuit, voltage divider, and sense module. The sense module consists of an n-channel MOSFET which low side drives an LED when the gate is triggered by the presence of 12V. We use this basic structure to sense voltage at various nodes (switches or relays) in the shutdown circuit of the car (the circuit which uses our low voltage system to close the isolation relays which allow high voltage to connect to the motor controller) but the LED is removed such that the current limiting resistor becomes a pull up resistor and the drain is connected to a digital IO pin.
