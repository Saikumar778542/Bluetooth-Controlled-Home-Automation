1.INTRODUCTION

Speech recognition enables machines to understand human voice commands and respond accordingly. In this project, a Bluetooth-based speech recognition system is developed where voice commands are given through a smartphone, converted into text, and transmitted to an embedded controller via Bluetooth to control devices. Unlike cloud-based systems, this method works offline, making it cost-effective and reliable for short-range applications.

2.OBJECTIVES

To design an offline speech-controlled system To use Bluetooth communication for command transmission To control devices using voice commands To implement a real-time embedded system To demonstrate speech-to-command execution.

3.SYSTEM OVERVIEW

The system works in the following steps User speaks a command into a smartphone Speech is converted to text using a mobile app Text command is sent via Bluetooth Embedded controller receives command Device is controlled accordingly.

4.BLOCK DIAGRAM

<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/7b273152-e303-4745-b4fd-db1e47c22f4a" />

5.HARDWARE REQUIREMENTS

Component Description Arduino UNO / ESP32 Main controller HC-05 / HC-06 Bluetooth module Smartphone Voice command input Relay Module Appliance control LED Demo device Power Supply 5V Jumper Wires Connections.

6.SOFTWARE REQUIREMENTS

Software Purpose Arduino IDE Programming Embedded C/C++ Coding Android Voice App Speech input Bluetooth Terminal Debugging.

7.BLUETOOTH MODULE DETAILS

HC-05 Bluetooth Module Communication type: UART Operating voltage: 3.3V Baud rate: 9600 Range: ~10 meters Pins: VCC → 5V GND → GND TX → RX (Arduino) RX → TX (Arduino via divider).

8.SPEECH RECOGNITION METHOD

Speech recognition is handled by the smartphone Mobile app converts speech to text Recognized text is transmitted via Bluetooth Example Commands:

"LED ON" "LED OFF" "FAN ON" "FAN OFF"

9.COMMAND PROCESSING LOGIC Receive Bluetooth data If command == "LED ON" → Turn LED ON If command == "LED OFF" → Turn LED OFF.

10FLOW CHART START 

| Initialize Bluetooth | Wait for Voice Command | Receive Bluetooth Data | Match Command | Control Device | Repeat.

11.CIRCUIT CONNECTIONS Arduino + HC-05 + LED HC-05 Pin Arduino Pin VCC 5V GND GND TXD RX RXD TX (via resistor divider) LED Arduino Anode D8 Cathode GND.

12.WORKING DEMONSTRATION Demo Procedure: Power ON Arduino Pair smartphone with HC-05 Open voice control app Speak command Bluetooth sends text Arduino executes action Example

Voice command: "LED ON" Result: LED turns ON

13.RESULTS

Voice commands recognized accurately Fast Bluetooth response Reliable device contro Offline operation achieved

14.APPLICATIONS

Home automation Assistive devices Voice-controlled robots Industrial equipment control Smart switches

15.ADVANTAGES

No internet required Low cost Simple implementation Fast response

16.LIMITATIONS

Limited range (~10 m) Mobile app dependency Noise affects recognition

17.FUTURE ENHANCEMENTS

Control multiple appliances Use ESP32 Bluetooth Add password security Voice feedback using speake Integrate sensors

18.CONCLUSION
A Bluetooth-based speech recognition system provides an efficient and low-cost solution for voice-controlled device operation. The system successfully demonstrates offline speech processing, wireless communication, and embedded control.


