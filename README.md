Digilab One
===========

Digilab One is an advanced digital logic lab companion designed to enhance the hands-on learning experience for students and streamline circuit validation for instructors. Originally developed as the Integrated Lab Companion (ILC) during the CPEN 4850 capstone project, it addresses the limitations of existing lab equipment by offering expanded capabilities, automated testing, and modern connectivity options.

**Note:** This project is closed source under Parleii LLC. The source code is not available in this repository. However, this README provides an overview of the project, discussing what it does and how it does it.

Table of Contents
-----------------

-   [Features](#features)
    -   [Hardware](#hardware)
    -   [Software](#software)
-   [Technologies Used](#technologies-used)
-   [Architecture Overview](#architecture-overview)
-   [Getting Started](#getting-started)
-   [Usage](#usage)
-   [Acknowledgements](#acknowledgements)

Features
--------

### Hardware

-   **7 Switches and 7 LEDs**: Allows for more complex circuit designs with manual control and monitoring.
-   **7-Segment Display**: Provides real-time visual feedback.
-   **Male and Female Pins**: Flexible connections for various circuit designs.
-   **Microcontroller (ATMEGA328P)**: Manages input/output logging, circuit validation, and communication.
-   **Power and Connectivity**: USB-C connection and 5V power supply through pins or USB-C.
-   **Standalone Operation**: Can be used independently to test basic logic circuits.

### Software

-   **Web-Based Platform**: A Next.js, React, and TypeScript web application for cross-platform accessibility.
-   **Input Control**: Transfer input switch control to the software for automated testing.
-   **Truth Table Testing**: Input custom truth tables and receive instant pass/fail feedback.
-   **Encrypted .digilab Files**: Uses CHACHA20 encryption to secure test files and maintain academic integrity.
-   **Real-Time Monitoring**: Automated testing with immediate feedback on circuit states.
-   **Serial Communication**: Communicates with the hardware via serial over USB.

Technologies Used
-----------------

-   **Node.js**: Server-side JavaScript runtime environment.
-   **Next.js**: React framework for building web applications.
-   **React**: JavaScript library for building user interfaces.
-   **TypeScript**: Typed superset of JavaScript for improved code quality.
-   **PostgreSQL**: Relational database for storing device UUIDs and user data.
-   **CHACHA20 Encryption**: Ensures secure communication and file encryption.
-   **Serial Communication**: Manages data exchange between the web app and hardware.
-   **CH340 Driver**: Enables USB-to-serial communication with the microcontroller.
-   **ATMEGA328P Microcontroller**: Handles hardware-level operations.

Architecture Overview
---------------------

The Digilab One system integrates multiple technologies to provide a seamless user experience:

1.  **Web Application**: Built with Next.js, React, and TypeScript, the web app serves as the user interface for controlling and monitoring the Digilab One hardware.

2.  **Server-Side Operations**: Node.js powers the backend, handling requests, encryption, and database interactions.

3.  **Database**: PostgreSQL stores device UUIDs, user data, and encrypted truth tables.

4.  **Encryption Protocols**: CHACHA20 ensures that .digilab files and communications maintain academic integrity.

5.  **Serial Communication**: The web app communicates with the microcontroller over USB using serial protocols facilitated by the CH340 driver.

6.  **Microcontroller Firmware**: The ATMEGA328P runs firmware that interacts with the web app, controls hardware components, and performs circuit validation.

<!-- ## Technology Flowchart Below is a simplified flowchart illustrating the interaction between different components: 1. **User Interface (Web App)** - Built with React and Next.js - Communicates with the backend server and hardware 2. **Backend Server** - Runs on Node.js - Handles encryption, database operations, and API endpoints 3. **Database (PostgreSQL)** - Stores device UUIDs, user data, and encrypted files 4. **Hardware Communication** - Uses serial communication over USB via CH340 driver - Interacts with the ATMEGA328P microcontroller 5. **Encryption Layer** - Utilizes CHACHA20 for secure file encryption and communication *Note: Since the project is closed source, specific implementation details are not disclosed.* -->

Getting Started
---------------

### Prerequisites

-   **Digilab One Device**: Ensure you have the hardware device.
-   **CH340 Driver**: Install the CH340 driver to enable USB-to-serial communication.

### Accessing the Software

The Digilab One software is available as a web application. You can access it using the following link:

Digilab One Web App

*Note: Replace the URL with the actual link to the web app.*

Usage
-----

### Connecting the Device

1.  **Hardware Setup**

    -   Connect the Digilab One to your computer using a USB-C cable.
    -   Ensure the CH340 driver is installed.
2.  **Web App Interface**

    -   Open the Digilab One web app in your browser.
    -   The web app will prompt you to select your device.
    -   If multiple devices are listed, unplug and reconnect to identify yours.

### Features Overview

#### Live Status Update

Monitor real-time status of lights, switches, and the 7-segment display directly from the web app.

#### Lab Creation

-   **Create Custom Labs**: Define input and expected output values.
-   **Save as .digilab Files**: Save your labs as encrypted files for secure distribution.
-   **Encryption**: Uses CHACHA20 encryption to maintain academic integrity.

#### Custom Test

-   **Manual Testing**: Observe circuit states without pass/fail conditions.
-   **Real-Time Control**: Manipulate inputs and monitor outputs in real time.

#### Lab Testing

-   **Upload .digilab Files**: Validate circuits against encrypted truth tables.
-   **Automated Testing**: Receive instant pass/fail feedback based on predefined logic.

#### State Machine Testing

-   **Define Sequences**: Test state machines by defining sequences and expected outputs.
-   **Automated Clock Control**: The software toggles the clock and inputs to test your state machine.

Acknowledgements
----------------

-   **Professor Rolland Howell**: For invaluable feedback and support during development.
-   **Parleii LLC**: For rebranding and expanding the project's potential.
-   **University of Tennessee at Chattanooga**: For providing the initial platform for development.

* * * * *

*For more detailed documentation, please refer to the official Digilab One documentation available through the web app.*
