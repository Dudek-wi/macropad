# ⌨️ XIAO 4-Key Macropad with 128x32 OLED

A minimalist, high-performance macropad powered by the **Seeeduino XIAO** and **KMK Firmware** (CircuitPython). This project uses 4 mechanical switches in a direct pin layout configuration, along with an integrated OLED display.

## ✨ Features
- **KMK Powered:** Easy configuration using Python, no compilation necessary.
- **OLED Display:** An integrated 128x32 SSD1306 display is used to view layer and status information.
- **Direct Pin Layout:** A simply pin layout is used
- **The source code is very simple, but it serves only as a basis for further development. I’m still learning and I’ll be looking to improve it.

## BOM
- 1x Seeed XIAO RP2040
- 4x MX-Style switches
- 1x 0.91 inch OLED display
- 4x white blank DSA keycaps
- 4x M3x16mm screws
- 3x M3x5mx4mm heatset inserts
- 1x custom PCB
## 🛠️ Hardware Specification

### Pin Mapping
Based on the Schematic and PCB Design, the pin mapping is as follows:

| Component | XIAO Pin | MCU Pin | Function |
| :--- | :--- | :--- | :--- |
| **SW1** | D10 | PA6 | Key Switch 1 |
| **SW2** | D9 | PA5 | Key Switch 2 |
| **SW3** | D8 | PA7 | Key Switch 3 |
| **SW4** | D7 | PB09 | Key Switch 4 |
| **OLED SDA** | D4 | PA8 | I2C Data |
| **OLED SCL** | D5 | PA9 | I2C Clock |

### J1 Connector (OLED)
A 4-pin I2C header is used on the PCB, which is connected to the OLED display as follows:
1. **GND** -> Ground
2. **VIN** -> 3.3V (From XIAO Pin 12)
3. **SCL** -> Clock
4. **SDA** -> Data

## 📂 Project Structure
- `kb.py`: Hardware Abstraction Layer (Pins, OLED Initialization).
- `code.py`: Logic Layer (Keymaps, Macros, Layers).

## 🚀 Getting Started
1. Flash **CircuitPython** onto the Seeeduino XIAO.
2. Copy the `kmk` folder along with the necessary Adafruit libraries to the `lib/` folder on the device.
3. Upload `kb.py` and `code.py` to the root of the `CIRCUITPY` drive.
4. It will auto-reload, and the device will start acting as a keyboard immediately.

## 📜 License
This project is licensed under the **MIT License**. Feel free to use, modify, and distribute it as you wish.

---
*Created with ❤️ using KMK and Seeeduino XIAO.*
<img width="902" height="670" alt="Zrzut ekranu 2026-03-26 175812" src="https://github.com/user-attachments/assets/e988c5ea-fd1d-4f33-b9f4-48ee5a11c063" />
<img width="1104" height="690" alt="Zrzut ekranu 2026-03-26 175825" src="https://github.com/user-attachments/assets/0b3ab646-00e0-4949-a90b-7104f7569fec" />
<img width="1072" height="655" alt="Zrzut ekranu 2026-03-26 175757" src="https://github.com/user-attachments/assets/17c87e87-0031-4c33-a542-3727a9fc7db9" />
<img width="1087" height="849" alt="Zrzut ekranu 2026-03-26 175856" src="https://github.com/user-attachments/assets/03bb6260-ae71-49d3-8f7e-d2635df93d5e" />
