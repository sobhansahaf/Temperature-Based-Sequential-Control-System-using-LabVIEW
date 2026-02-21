# 🔥 Temperature-Based Sequential Control System (LabVIEW)

## 📖 Overview

This project implements a **temperature-driven sequential control system** using **LabVIEW**.
The system simulates an industrial heating process with automated actuator control based on temperature thresholds and time delay logic.

The automation sequence controls:

* 🔥 Heater
* ⚙️ Motor
* 🚨 Alarm

The system ensures controlled startup, timed activation, and safe shutdown using upper and lower temperature limits.

---

## 🎯 System Objective

To design a LabVIEW-based control system that:

1. Starts heating when the system is activated.
2. Activates a motor when temperature exceeds a high threshold.
3. Triggers an alarm after a defined time delay.
4. Safely shuts down when temperature falls below a lower threshold.

---

## 🖥️ Front Panel Components

### Controls

* ▶ **Start Button**

### Indicators

* 🔥 Heater LED
* ⚙️ Motor LED
* 🚨 Alarm LED
* 🌡 Temperature Display

---

## ⚙️ System Operation Logic

### 1️⃣ Start Sequence

* When **Start Button** is pressed:

  * Heater turns ON
  * Temperature begins increasing

### 2️⃣ High Threshold Condition

* When temperature **> 1000**:

  * Motor turns ON
  * 5-second delay timer starts

### 3️⃣ Alarm Activation

* After **5 seconds** of motor operation:

  * Alarm turns ON
  * Temperature begins decreasing

### 4️⃣ Shutdown Condition

* When temperature **< 900**:

  * Heater turns OFF
  * Motor turns OFF
  * Alarm resets (optional)
  * System returns to idle state

---

## 🔁 Control Flow Diagram

```text
Start Pressed
     ↓
Heater ON → Temperature Rising
     ↓ (Temp > 1000)
Motor ON
     ↓ (5 seconds delay)
Alarm ON → Temperature Falling
     ↓ (Temp < 900)
Heater OFF
Motor OFF
System Reset
```


