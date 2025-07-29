# StriX Controller

The StriX Controller is a custom-designed game controller for flight simulation games, featuring dual analog joysticks, four switches, and a user-friendly USB Type-C interface. Built with an AtMega32U4 microcontroller, it supports HID protocol for plug-and-play compatibility. The controller includes an OLED display for real-time feedback via I2C and supports configuration through a rotary encoder (KY-040) or a software driver. Designed with modularity in mind, it includes an SPI interface for potential integration with the StriX UAV project via an NRF24L01 module.

## Features

- **Dual Analog Joysticks**: Precise control for flight simulation games.
- **Four Switches**: Additional input options for customizable actions.
- **USB Type-C Connectivity**: Modern, reliable connection for data and firmware updates.
- **AtMega32U4 MCU**: Provides native HID support for seamless integration with PCs.
- **OLED Display**: Displays real-time information via I2C communication.
- **Configurability**: Adjust settings using a KY-040 rotary encoder or a software driver.
- **SPI Interface**: Reserved pins for NRF24L01 module, enabling future StriX UAV integration.
- **Firmware Updates**: Update firmware via USB Type-C using standard tools like avrdude.

## Project Structure

- **Hardware/**: Contains KiCad project files for the controller’s PCB design and schematics.
- **Software/**: Placeholder for the software driver
- **Firmware/**: PlatformIO project for the AtMega32U4, including firmware code for controller functionality.

## Hardware Requirements

- AtMega32U4 microcontroller
- Dual analog joysticks
- Four switches
- USB Type-C port
- OLED display (I2C-compatible)
- KY-040 rotary encoder
- Optional: NRF24L01 module for future wireless expansion

## Setup Instructions

1. **Hardware Setup**:
   - Assemble the controller using the KiCad schematics in the `Hardware/` folder.
   - Ensure proper connections for the AtMega32U4, joysticks, switches, OLED, and KY-040.
2. **Firmware Installation**:
   - Clone the repository and open the `Firmware/` folder in PlatformIO.
   - Build and upload the firmware to the AtMega32U4 via USB Type-C using a compatible tool (e.g., avrdude).
3. **Software Driver**:
   - (TBD) Develop or install the driver from the `Software/` folder to configure controller settings.
4. **Testing**:
   - Connect the controller to a PC via USB Type-C.
   - Verify HID functionality and OLED display output.
   - Test joystick, switch, and KY-040 inputs in a flight simulation game.

## Firmware Updates

To update the firmware:

1. Connect the controller to a PC via USB Type-C.
2. Use a tool like avrdude to flash the updated firmware from the `Firmware/` folder.
3. Follow the PlatformIO documentation for detailed build and upload instructions.

## Future Expansion

The StriX Controller is designed for future integration with the StriX UAV project. The reserved SPI pins allow connection to an NRF24L01 module, enabling the controller to function as a transmitter (TX) for UAV control.

## Contributing

Contributions are welcome! Please fork the repository, make changes, and submit a pull request. Ensure your code follows the project’s coding standards and includes appropriate documentation.
