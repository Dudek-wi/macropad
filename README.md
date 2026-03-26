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
