Aim of the project: Create a data storage system using an ESP 32. 

Hardware used: ESP 32S. 
Programming Language: Embedded C.
GUI: Arduino Ide

About the Project: The main Aim of the project is to read and store the data from the PC that the user enters and then read back the data to the user when the user asks the Data to be read out.

- This project is built using the Embedded c-programming language where the data is stored in the EEPROM of the ESP 32.

The program achieves 3 specific tasks:
1) Receive the text input from the user and store it in the EEPROM of the ESP 32.
2) Read/ Display the text data that is stored in the EEPROM of the ESP 32.
3) Displays the transmission speed in live and we can ensure that the Data is being transferred from both the ends.

The protocol used to do this is UART: UART protocol uses only 2 pins(Rx and Tx) with no clock pulse(Optional for inclusive too) and data can be communicated b/w the Source and destination without the interrupt of the clock pulse and data loss can be prevented here. The disadvantage of this system is only a small volume of bitwise/ byte data can be transferred and it takes more time and complexity to transmit the data larger than 1Kb.

The Baud rate of this project is 2400 (Can be altered as per the application). 

Note: There is no need to write a separate code (Pc sided code) to run this Firmware as the interfacing and COM port access can be made on the GUI and the serial monitor provided by the GUI is helpful to display the text Data transmissions and the commands can be sent using the command line that is built-in the GUI of Arduino. (Other IDEs such as Espressif Ide can be used to work with this depending upon the application.)

How this project works?

The user is given to select 2 options: 
1) Transmit Data: The user will enter the text data and the data is sent to the ESP 32 and stored in the EEPROM of the ESP-32.

2) Receive Data: The user will enter the Read command and the text data that is stored in the EEPROM of the ESP32 is displayed on the monitor.

Along with the send and receiving the data, the transmission speed of bits/sec is also displayed.
Before the user enters the text, the program will show the available space and no. of characters that the user can enter until the memory is full.
If the no. of characters in the text message exceeds, the program pops up an error message. 
