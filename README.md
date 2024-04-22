# ESP32 Web Server

This project demonstrates controlling two LEDs using an ESP32 in Access Point (AP) mode. The ESP32 sets up a local Wi-Fi network with predefined credentials and hosts a web server. Users can interact with the web interface to toggle the state of two LEDs.

## Setup

### Hardware Requirements
- ESP32 development board
- Two LEDs
- Resistors (if required)
- Breadboard and jumper wires

### Software Requirements
- Arduino IDE with ESP32 board support
- Required Libraries:
  - WiFi.h
  - WebServer.h

## Installation and Usage

1. Connect the LEDs to the ESP32 GPIO pins as defined in the code.
2. Upload the code to your ESP32 board using the Arduino IDE.
3. Once uploaded, power up the ESP32.
4. Connect to the Wi-Fi network named "ESP32" with the password "ESP32".
5. Open a web browser and navigate to `http://YOURIPADDRESS` (or the appropriate IP address).
6. You should see a web interface with controls for LED1 and LED2.
7. Click the buttons to toggle the LEDs on and off.

## Code Explanation

- The code initializes the Wi-Fi network in AP mode with predefined credentials.
- It sets up a web server on port 80.
- Four endpoints are defined:
  - `/led1on`: Turns on LED1.
  - `/led1off`: Turns off LED1.
  - `/led2on`: Turns on LED2.
  - `/led2off`: Turns off LED2.
- The `SendHTML` function generates the HTML content for the web interface dynamically based on the current state of the LEDs.
- LED states are updated based on the HTTP requests received.
- Serial messages provide debugging information.

## Important Notes

- Ensure that the ESP32 has enough power to drive the LEDs.
- Modify the GPIO pin numbers if different pins are used for connecting the LEDs.
- Customize the Wi-Fi credentials if needed.
- The web interface is optimized for a browser on a desktop or mobile device.

Feel free to modify the code and circuit according to your requirements.
