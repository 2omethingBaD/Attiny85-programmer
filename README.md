# ATtiny85 Programmer User Guide

This project is designed to assist in programming **ATtiny microcontrollers**, providing a simple USB-based programmer for flashing code using the Arduino IDE.

![ATtiny85 programmer banner](https://github.com/2omethingBaD/Attiny85-programmer/blob/main/img/Untitled%20design%20(2).png?raw=true)

---

## 📋 Table of Contents
- [Assembly](#assembly)
- [Setting Up the Programmer](#setting-up-the-programmer)
- [Uploading Code](#uploading-code)
- [Tech Notes](#tech-notes)

---

## 🧰 Assembly

<details>
<summary><strong>Installing the ATtiny85</strong></summary>

Carefully place your **ATtiny85** into the 8-pin DIP socket on the programmer.

Make sure the **notch on the ATtiny85 faces outward**, as shown in the image below. Proper orientation is important — inserting the chip backwards can prevent programming and may damage components.

Once the chip is fully seated, plug the programmer board into a USB port on your PC.

![ATtiny85 installation orientation](https://github.com/2omethingBaD/Attiny85-programmer/blob/main/img/Take%20This....png?raw=true)

</details>

---

## ⚙️ Setting Up the Programmer

<details>
<summary><strong>Arduino IDE Configuration</strong></summary>

1. Open the **Arduino IDE**
2. Go to **Tools → Board → Boards Manager**
3. Search for and install **“ATtiny by David A. Mellis”**

After installation, configure the following under the **Tools** menu:

- **Board** → ATtiny25/45/85
- **Processor** → ATtiny85
- **Clock** → *(your preferred clock setting)*
- **Programmer** → **Arduino as ISP** *(not ArduinoISP)*

Finally, click **Burn Bootloader** to apply the selected chip configuration.

![Arduino board settings](https://github.com/2omethingBaD/Attiny85-programmer/blob/main/img/Screenshot%202025-12-18%20203354.png?raw=true)
![Arduino programmer selection](https://github.com/2omethingBaD/Attiny85-programmer/blob/main/img/Screenshot%202025-12-18%20204034.png?raw=true)

</details>

---

## ⬆️ Uploading Code

<details>
<summary><strong>Flashing Your Sketch</strong></summary>

Once the board and programmer settings are correct:

1. Open or write your sketch in the Arduino IDE
2. Go to **Sketch → Upload Using Programmer**

This writes your code directly to the ATtiny85 through the programmer.

![Upload using programmer](https://github.com/2omethingBaD/Attiny85-programmer/blob/main/img/Screenshot%202025-12-18%20203935.png?raw=true)

</details>

---

## 🧠 Tech Notes

<details>
<summary><strong>Learning more about the ATtiny85</strong></summary>

### What is the ATtiny85?
The **ATtiny85** is a compact **8-bit AVR microcontroller** designed for embedded projects where size, simplicity, and low power use matter.

### Memory Overview
The ATtiny85 includes:
- **8 KB Flash** for storing your program
- **512 bytes EEPROM** for storing data that should persist after power loss
- **512 bytes SRAM** for temporary runtime variables

### GPIO and Peripherals
Despite its small size, the ATtiny85 offers:
- **6 programmable I/O lines**
- a **10-bit ADC**
- timers, PWM output, and a **Universal Serial Interface (USI)** for simple communication tasks

### Internal Clock
The chip includes a built-in **calibrated internal oscillator**, so many projects can run without needing an external crystal.

### Why “Upload Using Programmer”?
When using an external programmer, Arduino IDE uses the selected programmer for:
- **Burn Bootloader**
- **Upload Using Programmer**

That makes this workflow ideal for bare ATtiny chips that are not connected through a normal USB serial bootloader.

### Why Use a Dedicated Programmer Board?
A dedicated programmer makes it easier to:
- insert and remove DIP chips safely
- keep pin orientation consistent
- avoid messy jumper wiring during repeated testing and flashing

</details>

---

💡 *Created by [SomethingBAD Studios](https://github.com/2omethingBaD) — “BAD ideas, genius built.”*
