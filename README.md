# Remote-Controlled LEGO Car Using Arduino and Web Interface

## Project Description

This project involves transforming a LEGO car into a remote-controlled vehicle using an Arduino microcontroller, an L298N motor driver, and a Wi-Fi module. The car can be controlled remotely via a web interface, allowing the user to control the direction and speed of the car's movement by simply pressing buttons on a web page.

## Features

- **Remote Control**: The car's movement (forward, backward, and stop) can be controlled through a web interface.
- **Speed Control**: The speed of the car can be adjusted using a slider or numeric input on the web page.
- **Wi-Fi Connectivity**: The car is connected to a Wi-Fi network, enabling remote control from any device on the same network.
- **Web Interface**: A user-friendly web page is hosted by the Arduino, providing an intuitive interface for controlling the car.

## Components Used

- **LEGO Car**: A basic LEGO car chassis to which motors and wheels are attached.
- **Arduino Board**: The brain of the project, responsible for controlling the motors and handling the web server.
- **L298N Motor Driver**: Used to drive the DC motors that move the car.
- **DC Motors**: Two DC motors to power the car's wheels.
- **Wi-Fi Module (WiFiNINA)**: Provides Wi-Fi connectivity, allowing the Arduino to host a web server.
- **Power Supply**: A battery pack to power the Arduino and motors.
- **Jumper Wires**: For connecting components.

## Circuit Diagram

1. **Motor Connections**:
   - Connect the motor pins (IN1, IN2) to digital pins 5 and 6 on the Arduino.
   - Connect the ENA (enable) pin on the L298N to the PWM pin 9 on the Arduino.
   - Connect the power supply to the L298N motor driver and the motors to the output pins of the L298N.
   
2. **Wi-Fi Module**:
   - Connect the WiFiNINA module to the Arduino using SPI connections.
   - Ensure the module is properly powered through the 3.3V and GND pins.

3. **Power Supply**:
   - Connect a battery pack to the L298N motor driver to provide power to the motors.
   - Power the Arduino separately or use a shared power source.

## Software Setup

### Arduino IDE Setup

- Install the `WiFiNINA` library through the Arduino IDE Library Manager.
- Upload the provided Arduino code to the board.

### Code Overview

- The code initializes the Wi-Fi connection and sets up a web server on the Arduino.
- The server listens for HTTP GET requests from the client (your web browser).
- Based on the request, the Arduino sets the direction and speed of the motors.
- The web page served by the Arduino allows the user to control the car’s movement and speed.

### Web Interface

- The web page includes buttons for controlling the car's direction (forward, backward, stop) and an input field for setting the speed (0-255).
- The speed value is retained across requests to prevent it from resetting.

## How to Use

1. **Setup the Car**:
   - Assemble the LEGO car chassis and attach the motors.
   - Connect the motors to the L298N motor driver, and the driver to the Arduino.
   - Ensure the power supply is connected and the Arduino is powered.

2. **Connect to Wi-Fi**:
   - Power on the Arduino and wait for it to connect to your Wi-Fi network.
   - The Arduino will print the IP address to the Serial Monitor.

3. **Control the Car**:
   - Open a web browser and enter the Arduino's IP address.
   - Use the buttons on the web page to control the car’s direction.
   - Adjust the speed using the input field and click "Set Speed" to apply the changes.

## Troubleshooting

- **Wi-Fi Connection Issues**: Ensure the Wi-Fi credentials in the code are correct. Check the Serial Monitor for connection status.
- **Car Not Moving**: Double-check all motor connections and ensure the power supply is sufficient.
- **Web Interface Not Loading**: Verify the Arduino's IP address and ensure your device is connected to the same network.

## Future Enhancements

- **Add Steering Control**: Implement a steering mechanism to control the car's direction left and right.
- **Battery Monitoring**: Add a feature to monitor the battery level and display it on the web interface.
- **Mobile App Integration**: Develop a mobile app to control the car, providing a more seamless user experience.

## Acknowledgments

This project was inspired by the desire to combine the simplicity and creativity of LEGO with the power and flexibility of Arduino. Special thanks to the Arduino and open-source community for providing the resources and libraries that made this project possible.

---

Enjoy building and controlling your very own remote-controlled LEGO car!
