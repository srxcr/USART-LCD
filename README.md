# 📄 PIC Microcontroller USART to LCD Project

## 💡 Overview

This project demonstrates how to receive characters through the USART module of a PIC18F4550 microcontroller and display them on a 16x2 LCD, while simultaneously echoing the received characters back to the sender.

---

## ⚙️ Hardware Requirements

- **Microcontroller**: PIC18F4550
- **Display**: 16x2 LCD (e.g., LM016L)
- **Virtual Terminal**: For serial communication simulation (e.g., Proteus virtual terminal)
- **Connections**:
  - LCD data lines: PORTD
  - LCD control lines: RA0 (RS) and RA1 (EN)
  - USART TX/RX pins connected to virtual terminal

---

## 💻 Software Requirements

- Compiler: MPLAB XC8 or any compatible C compiler for PIC
- Proteus Design Suite (or any other simulator for verification)

---

## 🔌 Circuit Description

- LCD is configured in 8-bit mode and controlled through PORTD, with RS and EN signals on RA0 and RA1.
- The USART module is configured for asynchronous communication at 9600 baud rate.
- Characters received over USART are shown on the LCD and echoed back to the sender.


## 📝 Code Explanation
- `command()`: Sends an LCD command (e.g., clear display, set cursor).
- `data()`: Sends a character to display on LCD.
- `trans()`: Sends (transmits) a character over USART.
- `rec()`: Receives a character from USART.
- `delay()`: Creates approximate delay for LCD timing.

## 🛠️ Steps to Do
- Write the code in MPLAB X IDE or your preferred editor.
- Compile the code using XC8 to generate a HEX file.
- Connect the circuit as shown in usart-lcd.png.
- Load the HEX file into Proteus or flash to the physical PIC.
- Open the virtual terminal and start typing — each character will display on LCD and echo back in terminal.

## ⚡ USART Configuration
- **Baud rate**: 9600
- **Mode**: Asynchronous
- **Transmission and reception**: Enabled

## 🖼️ Schematic
![Schematic](usat-lcd.png)

## ⚠️ Limitations
- Blocking receive — no interrupt used.
- Only one character handled at a time.
- Software delay is approximate.

## 📄 License
This project is shared for educational purposes only. Unauthorized reproduction or commercial use is prohibited.

## 🙏 Acknowledgments
Developed and tested on a PIC18F4550 development board and Proteus simulation.
