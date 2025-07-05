
#  Stepper Motor Control Using LCD – Wokwi Simulation

This project simulates a **stepper motor control system** using an **Arduino Uno**, a **20×4 I2C LCD**, and an **A4988 stepper driver**, developed and tested in the [Wokwi simulator](https://wokwi.com/projects/394509063346644993). It allows users to control the stepper motor using analog and digital inputs with real-time feedback on an LCD screen.

## 🎯 Features

- ✅ **Two Modes of Operation**:
  - **Degree Mode (DEG)**: Rotate motor by a specific angle at a set RPM.
  - **RPM Mode**: Run the motor continuously at a specified RPM.
- ✅ **User Interface via LCD**:
  - Mode (DEG / RPM)
  - Rotation direction (CW / ACW)
  - Analog value (potentiometer)
  - Digital input (increment/decrement via buttons)
  - Required combined value
  - Resolution setting (0.01 / 1 / 10 / 100)
- ✅ **Microstepping Support** using A4988 driver
- ✅ **State-based execution** with `enter` key to proceed through steps

---

## 🧩 Components Used (in Simulation)

| Component         | Description                          |
|------------------|--------------------------------------|
| Arduino Uno       | Main microcontroller board           |
| A4988 Driver      | Stepper motor driver                 |
| Stepper Motor     | Controlled by AccelStepper library   |
| 20×4 I2C LCD      | For displaying status and inputs     |
| Potentiometer     | For analog RPM/degree input          |
| Push Buttons      | For direction, mode toggle, input inc/dec, enter |
| Wokwi Platform    | Virtual prototyping and testing tool |

---

## 🔌 Controls and Pin Configuration

| Function              | Arduino Pin |
|-----------------------|-------------|
| Step Pin (A4988)      | 9           |
| Dir Pin (A4988)       | 8           |
| Microstep Enable      | 7           |
| Power Button          | 2           |
| Mode Toggle (DEG/RPM) | 3           |
| Rotation Direction    | 4           |
| Button Increase       | 5           |
| Button Decrease       | 6           |
| Enter Button          | 10          |
| Resolution Button     | 13          |
| POT Input             | A0          |
| I2C LCD (SDA/SCL)     | A4 / A5     |

---

## 📺 Live Simulation

👉 [Open Project in Wokwi](https://wokwi.com/projects/394509063346644993)

---

## 🧠 Libraries Used

- [AccelStepper](https://www.airspayce.com/mikem/arduino/AccelStepper/) – for smooth stepper control  
- [LiquidCrystal_I2C](https://github.com/johnrickman/LiquidCrystal_I2C) – for LCD interfacing over I2C

---

## 📌 How It Works

1. **Power on** using the Power button.
2. **Select mode** (DEG or RPM) using the toggle button.
3. Use the **POT** and **buttons** to adjust input value.
4. Press **Enter** to:
   - In DEG Mode: First set degrees → enter → then RPM → enter → motor runs for calculated steps.
   - In RPM Mode: Set RPM → enter → motor runs continuously until next enter press.
5. Press **Resolution button** to change the increment/decrement step for digital input (0.01 / 1 / 10 / 100).
6. **LCD displays** all real-time inputs and motor status.

---

## 📦 Future Improvements

- Add button debounce logic  
- Include step/RPM feedback display during motion  
- Add EEPROM storage for saving last used values  
- Include buzzer or LED indicators for status alerts  

---

## 🛠 Developed By

**Group Spartans**  
Made for academic learning and demonstration purposes using the Wokwi simulator.

---

