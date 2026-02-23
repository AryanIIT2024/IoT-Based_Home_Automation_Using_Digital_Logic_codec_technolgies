# 🔐 RFID Access Control System (Arduino)

## 📌 Overview

This project is a simple **RFID-based Access Control System** built using an Arduino, RC522 RFID reader, and I2C LCD display.
It scans RFID cards and checks whether the scanned card is authorized. If the card is valid, the system displays a welcome message along with the user’s name. Otherwise, access is denied.

This project is ideal for learning:

* RFID communication
* Arduino SPI interface
* I2C display control
* Basic security system logic

---

## 🧰 Components Used

* Arduino Nano / Uno
* RC522 RFID Module
* 16×2 I2C LCD Display
* RFID Cards/Tags
* Jumper wires

---

## ⚙️ Working Principle

1. The system continuously waits for an RFID card.
2. When a card is scanned, its **UID** is read.
3. The UID is compared with a list of stored authorized UIDs.
4. If matched:

   * LCD shows welcome message with name.
   * Serial monitor prints “Access Granted”.
5. If not matched:

   * LCD shows “Access Denied”.
   * Serial monitor prints “Access Denied”.
6. System resets and waits for next scan.

---

## 🔌 Connections

### RFID → Arduino

* SDA → D10
* SCK → D13
* MOSI → D11
* MISO → D12
* RST → D9
* 3.3V → 3V3
* GND → GND

### LCD → Arduino

* SDA → A4
* SCL → A5
* VCC → 5V
* GND → GND

---

## 📚 Libraries Required

Install from Arduino Library Manager:

* MFRC522
* LiquidCrystal_I2C
* SPI (built-in)
* Wire (built-in)

---

## ➕ Customization

You can modify the code to:

* Add more authorized cards
* Change display messages
* Connect a relay for door lock
* Add buzzer or LED indicators
* Store attendance logs

---

## 🚀 Applications

* Smart Door Lock
* RFID Attendance System
* College/Office Entry System
* IoT Security Projects
* Embedded Systems Practice

---

## 📜 License

This project is open-source and free to use for educational and personal projects.

---

⭐ *If you found this project useful, consider starring the repository!*
