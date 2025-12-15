# 🔐 Secure Embedded Access Control System (ATmega16)

A complete embedded security system implemented using the **ATmega16 microcontroller**, simulated in **Proteus**, featuring RFID-based access triggering, PIN verification, relay-based door locking, tamper detection, and audible alerts.

---

## 📌 Project Overview

This project simulates a real-world **secure door access control system**.  
Access is granted only when a valid RFID trigger is followed by a correct PIN entry.  
Any unauthorized attempt or physical tampering immediately activates an alarm and locks the system.

---

## ⚙️ System Features

- RFID access trigger via UART (Proteus Virtual Terminal)
- 4×3 matrix keypad for PIN entry
- 16×2 LCD for user interaction
- Relay-controlled door lock
- Buzzer alerts for wrong PIN and tamper detection
- External interrupt–based tamper switch (INT0)
- Secure retry logic for incorrect PIN attempts

---

## 🧩 Hardware Components

- ATmega16 Microcontroller
- 16×2 LCD (8-bit mode)
- 4×3 Matrix Keypad
- Relay + BC547 transistor + Flyback diode (1N4007)
- Buzzer
- Tamper Switch (External Interrupt)
- 8 MHz Crystal Oscillator + 22 pF capacitors
- Proteus Virtual Terminal (UART simulation)

---

## 🔌 Pin Configuration

### LCD
- Data Pins: `PORTA (PA0–PA7)`
- RS: `PB2`
- EN: `PB3`
- RW: `GND`

### Outputs
- Relay: `PB0`
- Buzzer: `PB1`

### Inputs
- Tamper Switch: `PD2 (INT0)`
- Keypad: `PORTC`

### UART
- RXD: `PD0`

---

## 🧠 System Workflow

1. System initializes and displays **"Scan RFID"**
2. RFID trigger received via UART
3. User prompted to enter PIN
4. Correct PIN → Access Granted (Relay ON)
5. Wrong PIN → Audible alert and retry
6. Tamper detected → Alarm ON and system locked

---

## 🛠️ Software Details

- Language: **Embedded C**
- Compiler: **AVR-GCC**
- Clock Frequency: **8 MHz**
- Simulation Tool: **Proteus 8 Professional**

---

## 🚀 How to Run (Proteus)

1. Load the HEX file into ATmega16
2. Set clock frequency to 8 MHz
3. Use **Virtual Terminal** to send any character (RFID simulation)
4. Enter PIN using keypad
5. Observe LCD messages, relay operation, and buzzer alerts

---

## 🎯 Learning Outcomes

- Hardware–software co-design
- Secure embedded system logic
- Interrupt handling and UART communication
- Practical embedded security implementation

---

## 📄 License

This project is for educational and learning purposes.

---

## 👤 Author

**Manish Joshi**  
Embedded Systems | AI & ML Engineer  
