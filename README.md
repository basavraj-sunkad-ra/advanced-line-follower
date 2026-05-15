# 🤖 Advanced Line Follower Robot with Obstacle Avoidance

An advanced high-speed Arduino-based Line Follower Robot designed for robotics competitions and atypical tracks with:

- 🚀 High-speed PID line following
- 🧠 Smart curve prediction
- 🔥 Sharp turn handling
- 🚧 Obstacle detection & avoidance
- 🎯 Analog sensor precision
- ⚡ Dynamic speed control

---

# 📌 Features

## ✅ Advanced PID Control
- Proportional + Integral + Derivative control
- Stable tracking at high speed
- Smooth corner handling

## ✅ Analog Sensor Reading
- Better accuracy than digital sensors
- Handles:
  - Faded lines
  - Curves
  - Uneven tracks

## ✅ Dynamic Speed Adjustment
Robot automatically changes speed based on:
- Straight path
- Gentle curves
- Sharp turns

## ✅ Obstacle Avoidance
Uses ultrasonic sensor to:
- Detect nearby obstacles
- Stop robot
- Perform avoidance maneuver

## ✅ Smart Recovery
If line is lost:
- Robot remembers last direction
- Attempts automatic recovery

---

# 🛠 Components Required

| Component | Quantity |
|----------|----------|
| Arduino UNO/Nano | 1 |
| TB6612FNG Motor Driver | 1 |
| DC Motors | 2 |
| IR Sensor Array (8 channel) | 1 |
| Ultrasonic Sensor HC-SR04 | 1 |
| Chassis | 1 |
| Wheels | 2 |
| Castor Wheel | 1 |
| Li-ion Battery | 1 |

---

# 🔌 Pin Configuration

## Motor Driver

| Pin | Arduino |
|------|---------|
| AIN1 | 4 |
| AIN2 | 5 |
| PWMA | 3 |
| BIN1 | 7 |
| BIN2 | 8 |
| PWMB | 6 |
| STBY | 2 |

---

## Ultrasonic Sensor

| Pin | Arduino |
|------|---------|
| TRIG | 12 |
| ECHO | 13 |

---

## Sensor Array

| Sensor | Arduino |
|---------|----------|
| S1 | A0 |
| S2 | A1 |
| S3 | A2 |
| S4 | A3 |
| S5 | A4 |
| S6 | A5 |
| S7 | A6 |
| S8 | A7 |

---

# ⚙️ PID Parameters

```cpp
float Kp = 0.22;
float Ki = 0.0004;
float Kd = 1.1;

These values are optimized for:

High-speed racing
Stable turns
Competition tracks

📜 Main Logic
Line Following
Reads all 8 sensors
Calculates weighted error
Uses PID correction
Adjusts motor speeds
Sharp Turn Handling

If robot detects extreme deviation:

Performs controlled pivot turn
Obstacle Detection

If obstacle < 12 cm:

Stop motors
Avoid obstacle
Resume tracking

🧠 Future Improvements
Auto sensor calibration
Maze solving
Path memory optimization
Bluetooth control
OLED debugging display

🤝 Contribution

Contributions are welcome!

Feel free to:

Optimize PID
Improve obstacle logic
Add maze solving
Improve recovery algorithms

