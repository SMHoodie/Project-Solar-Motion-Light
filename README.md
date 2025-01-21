Project Overview
A fully self-sustaining, solar-powered motion sensor light system built around an ESP32. It leverages deep sleep modes, RTC-based nighttime detection, and a PIR sensor to activate only when motion is detected—making it ideal for off-grid or remote applications. Planned future upgrades include a custom PCB and LDR integration for enhanced efficiency and scalability.

Key Features
Self-Sustaining Power
Powered by a solar panel and a rechargeable lithium battery, requiring zero manual intervention once set up.

Power Efficiency
Utilizes the ESP32’s deep sleep mode and nighttime RTC checks to minimize energy consumption.

Motion-Activated Lighting
Integrates a PIR sensor to trigger the flashlight only when movement is detected, conserving battery life.

Off-Grid Readiness
Ideal for remote installations due to its autonomous operation and lack of reliance on traditional power sources.

Future Enhancements

Custom PCB: Streamlines the design by merging the solar charging circuit, boost converter, and regulators.
LDR Integration: Dynamically adjusts system behavior based on ambient light levels.
System Components
ESP32 Microcontroller – Orchestrates logic, power modes, and sensor input.
PIR Sensor (HC-SR501) – Detects motion to activate the flashlight.
Solar Panel – Charges the lithium battery during the day.
Lithium Battery & Charging Board – Stores and regulates energy for nighttime use.
Boost Converter & Voltage Regulator – Supplies stable voltages (5V & 3.3V) for the PIR sensor and ESP32.
NPN Transistor – Manages power to the flashlight.
Flashlight – Provides illumination during motion events.
RTC (Built-in ESP32) – Tracks time for day/night recognition.
How It Works
Daytime Charging

Solar panel charges the lithium battery through the charging board.
The ESP32 remains in deep sleep to conserve power.
Nighttime Activation

The ESP32 wakes up based on its RTC, enabling the PIR sensor.
Motion Detected? Transistor switches on the flashlight for a set duration (e.g., 5 seconds).
Sleep & Repeat

After the illumination period, the system returns to deep sleep or monitors again for motion.
Future Steps
Custom PCB Development: Combine the charging circuit, boost converter, and voltage regulators into a more compact solution.
LDR Integration: Implement light-dependent sensing for finer control of when the motion sensor activates, reducing unnecessary light usage.
Use Cases
Outdoor Security Light: Provides motion-triggered illumination for yards, gardens, or driveways.
Remote Installations: Perfect for cabins, campsites, or any off-grid location.
Energy-Saving Lighting: Efficient for areas where utility power is costly or unavailable.
Repository Contents
Firmware Code: ESP32 sketch with deep sleep, RTC timing, and motion sensing logic.
Hardware Documentation: Schematics and diagrams for wiring solar panel, battery, PIR, and flashlight.
Bill of Materials (BOM): List of all components used, including part numbers and potential sources.
Future PCB Files (Coming Soon): Initial designs for the all-in-one PCB solution.
