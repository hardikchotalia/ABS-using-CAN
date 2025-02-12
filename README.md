# Automatic Breaking System using CAN Protocol

### About Project 

This project develops an automatic braking system (ABS) for vehicles using the Controller Area Network (CAN) protocol for communication. The system uses an ultrasonic sensor to detect objects in front of the vehicle. The data from the sensor is sent to a microcontroller (STM32F407) that processes the information. If an obstacle is detected, the microcontroller sends a signal over the CAN network to another microcontroller, which controls the vehicle’s brakes through a motor drive circuit. The system also has a buzzer that sounds an alert when there’s danger.
The CAN protocol helps ensure that all parts of the system communicate reliably and quickly, which is important for safety. This project shows that a simple and effective ABS can be built using common parts and the CAN protocol, improving vehicle safety and reducing the risk of collisions. In the future, more sensors could be added for better awareness of the surroundings, and smarter control systems could improve braking performance.

![Block_Diagram](https://github.com/user-attachments/assets/a51ea73d-3df6-4be0-8ba8-573f09833250)

1. STM32F407 [TX]: The microcontroller acts as the "transmitter" and is responsible for gathering data from the sensor and initiating the braking action. This unit is primarily transmitting data onto the CAN bus.
2. STM32F407 [RX]: The microcontroller acts as the "receiver" and is responsible for receiving the braking command and controlling the actual braking mechanism. This unit is primarily receiving data from the CAN bus.
3. MCP2551 are transceivers that convert the digital signals from the STM32F407 into the differential signals required for the CAN bus and vice versa. They act as a bridge between the microcontroller and the physical CAN bus. The two wires that make up the CAN bus. CAN H (High) and CAN L (Low) carry the differential signals that enable communication between the nodes.
4. Ultrasonic Sensor [HC-SR04]: This sensor measures distance to obstacles by emitting ultrasonic pulses and measuring the time it takes for the echo to return. This data is crucial for the automatic braking system to detect potential collisions.
5. MOTOR DRIVE [L298N]: The Motor driver module controls the speed and direction of a DC motor. In this system, it's used to control the braking mechanism.
6. BUZZER: An audible alarm used to provide warnings or alerts to the user about potential dangers.
7. UART [CP2102]: This indicates a serial communication interface (Universal Asynchronous Receiver/Transmitter) using a CP2120 converter. This is used for displaying distance for external devices.

![setup](https://github.com/user-attachments/assets/9f5903f5-6c1b-4be1-b444-670b1b0ba3a3)

### Circuit Diagram
![Circuit_Diagram](https://github.com/user-attachments/assets/1e2d2f12-94cf-4ed2-99fe-9feffa76611d)

### Conclusion
The Automatic Braking system, if implemented can avert lots of accidents and can save invaluable human lives and property. Implementation of such an advanced system can be made compulsory similar to wearing of seat belts so that accidents can be averted to some extent. Our Automatic braking system provides a glimpse into the future of low cost automotive safety, and how much more advanced these individual systems can be for avoiding accidents and protecting vehicle occupants when they are integrated into one system. The future of automotive safety is more than just developing new technology, it is shifting the approach to safety. Automatic Braking System approach represents a significant shift from the traditional approach to safety, but it is fundamental to achieving the substantial benefits.

