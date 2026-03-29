XIAO 4 key macropad with 128 by 32 OLED

Anyone looking for an easy-to-use macro panel will find what they’re looking for here. Built on the Seeeduino XIAO, it lives inside KMK Firmware using CircuitPython - so all actions speak without any need to compile. Four mechanical buttons connect straight into place while an OLED screen shows what matters. 

I am fresh at this, my code stays simple for now. As my knowledge grows, I will make changes - step by step.

Features:

- Python powers KMK Firmware: connect it and start using it.
- OLED screen: A 128x32 SSD1306 display shows your device status.
- Direct pin layout: A simple wiring configuration.

Keyboard shortcuts:

- SW1- CTRL + C (copy)
- SW2- CTRL + V (paste)
- SW3- CTRL + Z (undo)
- SW4- CTRL + SHIFT + ESC (Task Manager)

OLED screen displays two lines of text: "XIAO MACROPAD" and "Ready!".

BOM
- 1x Seeed XIAO RP2040
- 4x MX-Style switches
- 1x 0.91 inch OLED display
- 4x white blank DSA keycaps
- 2x M3x16mm screws
- 2x M3x5mmx4mm heats inserts
- 1x custom PCB

Hardware Specification

Pin mapping:
- SW1 - D10 - Key Switch 1 
- SW2 - D9 - Key Switch 2
- SW3 - D8 - Key Switch 3 
- SW4 - D7 - Key Switch 4
- OLED SDA - D4 - I2C Data
- OLED SCL - D5 - I2C Clock

Oled pin
1. Ground
2. 3.3v
3. SCL
4. SDA

Software
- kb.py: Handle hardware stuff
- code.py: Controls the logic

Getting Started

1. Flash CircuitPython onto the Seeeduino XIAO
2. Start by placing the KMK folder along with the Adafruit libraries inside the lib/ directory of the device.
3. Place kb.py together with code.py into the main folder named CIRCUITPY.
4. A fresh signal kicks it back online, ready to act like keys. After that reset, typing begins without extra steps.

* Folder lib/ 
	kmk/ 
	adafruit_bus_device/
  "adafruit_ssd1306.py"
  "adafruit_framebuf.py"
	
Fine, just plug it in. Then off you go.

I make this project under the MIT License. You are free to use it.

<img width="902" height="670" alt="Zrzut ekranu 2026-03-26 175812" src="https://github.com/user-attachments/assets/fda982bd-7e2e-4655-91c5-3d8b9997faa8" />
<img width="1104" height="690" alt="Zrzut ekranu 2026-03-26 175825" src="https://github.com/user-attachments/assets/57960fcb-8d9f-4b0a-89c7-d8fae6ce7dd3" />
<img width="1087" height="849" alt="Zrzut ekranu 2026-03-26 175856" src="https://github.com/user-attachments/assets/64ba9d97-f85f-4735-adc8-4eace01d9603" />
<img width="864" height="560" alt="Zrzut ekranu 2026-03-26 212112" src="https://github.com/user-attachments/assets/3c32fa7c-6097-4b1a-973c-0ddd57013c2e" />
