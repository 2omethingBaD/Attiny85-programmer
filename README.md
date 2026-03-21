# ATtiny85 Programmer User Guide

This project is designed to assist in programming **ATtiny microcontrollers**, providing a simple USB-based programmer for flashing code using the Arduino IDE.

![ATtiny85 installation orientation](https://github.com/2omethingBaD/Attiny85-programmer/blob/main/img/Untitled design (2).png?raw=true)

---

## 📋 Table of Contents
- [Assembly](#assembly)
- [Setting Up the Programmer](#setting-up-the-programmer)
- [Uploading Code](#uploading-code)

---

## 🧰 Assembly

<details>
<summary><strong>Installing the ATtiny85</strong></summary>

Carefully place your **ATtiny85** into the 8-pin DIP socket on the programmer.  
Ensure the **notch on the ATtiny85 faces outward**, as shown in the image below.

Once the chip is properly seated, plug the programmer board into a USB port on your PC.

![ATtiny85 installation orientation](https://github.com/2omethingBaD/Attiny85-programmer/blob/main/img/Take%20This....png?raw=true)

</details>

---

## ⚙️ Setting Up the Programmer

<details>
<summary><strong>Arduino IDE Configuration</strong></summary>

1. Open the **Arduino IDE**  
2. Navigate to **Tools → Board → Boards Manager**  
3. Install **“ATtiny by David A. Mellis”**

Once installed, configure the following under the **Tools** menu:
- **Board** → ATtiny25/45/85  
- **Processor** → ATtiny85  
- **Clock** → (Your preference)  
- **Programmer** → Arduino as ISP (NOT ArduinoISP)

Finally, select **Burn Bootloader** to apply the clock settings to your ATtiny85.

![Arduino board settings](https://github.com/2omethingBaD/Attiny85-programmer/blob/main/img/Screenshot%202025-12-18%20203354.png?raw=true)
![Arduino programmer selection](https://github.com/2omethingBaD/Attiny85-programmer/blob/main/img/Screenshot%202025-12-18%20204034.png?raw=true)

</details>

---

## ⬆️ Uploading Code

<details>
<summary><strong>Flashing Your Sketch</strong></summary>

Once your board and programmer are configured:

1. Open or write your sketch in the Arduino IDE  
2. Navigate to **Sketch → Upload Using Programmer**  

This will flash your code directly to the ATtiny85.

![Upload using programmer](https://github.com/2omethingBaD/Attiny85-programmer/blob/main/img/Screenshot%202025-12-18%20203935.png?raw=true)

</details>

---

💡 *Created by [SomethingBAD Studios](https://github.com/2omethingBaD) — “BAD ideas, genius built.”*
