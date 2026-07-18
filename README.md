Set up the hardware:
        Connect two buttons to the ESP8266 D1 Mini Pro.
        Connect an LED to the ESP8266 NodeMCU.

    Program the ESP8266 D1 Mini Pro:
        One button will send a signal to turn the LED on.
        The other button will send a signal to turn the LED off.

    Program the ESP8266 NodeMCU:
        Receive the signal from the ESP8266 D1 Mini Pro to control the LED.

Here is an example of how to implement this using the Arduino IDE with the ESP8266 boards.
Hardware Connections

ESP8266 D1 Mini Pro:

    Button 1 connected to GPIO 5 (D1).
    Button 2 connected to GPIO 4 (D2).
    GND connected to one side of each button.

ESP8266 NodeMCU:

    LED connected to GPIO  (D2) through a current-limiting resistor.
    GND connected to the cathode of the LED.
Explanation

    ESP8266 D1 Mini Pro:
        Connects to WiFi.
        Monitors button presses.
        Sends an HTTP GET request to the NodeMCU to turn the LED on or off based on which button is pressed.

    ESP8266 NodeMCU:
        Connects to WiFi.
        Sets up a simple web server to handle HTTP GET requests.
        Controls the LED based on the received command.

Replace your_SSID and your_PASSWORD with your actual WiFi credentials and NodeMCU_IP with the IP address of your NodeMCU.

This setup will allow you to control the LED on the NodeMCU using the buttons connected to the D1 Mini Pro.
