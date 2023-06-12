# HomeAutomation
This project allows you to control a home appliances using voice command.

## Prerequisites
- Arduino board (i used 1 arduino UNO and arduino nano )
- servo motors
- RF Transmitter-receiver module
- Stepper motor and driver
- 12 volt battery
- potentiometer
- Python
- Required libraries: pyserial (for serial communication with Arduino)
- and some other hardware stuff

# Working 
In the code you provided, the communication between Python and Arduino is established using the Serial class from the pySerial library and RF module. 

In the 'Python_DataSender' file:
SpeechRecognition module is used to recognise the user command
The write() method is used to send commands or data to the Arduino.for example, in Python_DataSender the command 't' is sent as a byte string using the b't' notation. You can modify this line to send different commands or data depending on your requirements.

In the 'MainArduino_DataSende & DustbinTrasnmitter' file:
The readline() method is used to read data. It reads a line of text until a newline character ('\n') is encountered. The received data is stored in the response variable for further processing.
And in for certain commands it sends data through transmitter to reciever that is attached to dustbin arduino.

In the 'DustbinArduino_Reciever' file:
When the dustbin arduino recieves certain commands from reciever it moves the dustbin.
