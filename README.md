# 🌍 Smart Environment Monitoring & Control System (STM32)

A modular and interactive embedded system developed using **STM32 microcontroller**, designed to monitor environmental light and control connected peripherals (LEDs and buzzer) accordingly. The system features a clear LCD interface, password-protected settings, and UART-based command interaction.

---

## 🚀 Features

- 📟 **LCD Display UI** showing:
  - Real-time light percentage
  - Light condition (Low/Medium/High)
  - Threshold value
  - Beep status
  - Settings and password prompts

- 💡 **Light Sensing** using `lsens_get_val()`
  - Monitors environmental light from 0–100%
  - Compares against a configurable threshold

- 🔔 **Buzzer Control**
  - Auto triggers a 0.5s beep if light falls below or rises above threshold
  - Can be enabled/disabled via UART or keys

- 🔆 **LED Indicators**
  - LED0 ON for good light, LED1 ON for low light

- 🔐 **Password-Protected Settings**
  - Enter via KEYS: KEY0=1, KEY1=3, WKUP=2 (Password = 132)
  - Prevents unauthorized changes

- 🧭 **UART Command Interface**
  - `0` - Show menu
  - `1` - Show light level
  - `2` - Toggle beep
  - `3 [val]` - Set threshold
  - `4` - Enter settings mode

---

## 📁 Project Structure

SmartEnvMonitor/
├── BSP/ # Board Support Packages
│ ├── LED/
│ ├── LSENS/
│ ├── BEEP/
│ ├── KEY/
│ └── LCD/
├── SYSTEM/ # System configuration (clock, delay, etc.)
│ ├── sys/
│ ├── delay/
│ └── usart/
├── main.c # Main application logic
├── README.md # This file
└── [Other headers and config files...]


---

## 🛠️ Setup & Compilation

- Platform: **STM32F103C8T6 / STM32F1 Series**
- IDE: **Keil uVision / STM32CubeIDE**
- Dependencies:
  - Custom libraries for LCD, LED, Buzzer, Keys, USART, Light Sensor
- Baud rate for UART: `115200`

Make sure all `BSP` and `SYSTEM` folders are correctly included in your project.

---

## 💡 Applications

- Smart Home/Office lighting control
- Smart street lighting
- Educational embedded system prototype
- Industrial or agricultural light monitoring
- Access-controlled IoT devices

---

## 📸 Screenshots (Optional)
> Add photos of LCD display, hardware setup, or UART commands in action.

---

## 🧠 Author

**Developed by:** *[Hasan Syed Tabeh]*  
**For:** Midterm Embedded Systems Project  
**Supervised by:** *[Mr.Li Yunrui]*

---

## 🙌 Contributions

Feel free to fork, improve, or suggest enhancements via pull requests.

