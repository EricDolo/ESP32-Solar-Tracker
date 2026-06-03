# ☀️ ESP32 Solar Tracker

An autonomous single-axis solar tracking system built with an ESP32 microcontroller. The system continuously monitors sunlight direction using two LDR sensors and drives a stepper motor to rotate the solar panel toward the brightest light source — maximising solar energy absorption throughout the day.

---

## 📸 Project Photos

> _Add your photos here by dragging them into the GitHub repository_

---

## 🎥 Video Presentation

> _Add your YouTube link here:_
> [Watch the project presentation](https://your-youtube-link-here)

---

## 🔧 How It Works

Two LDR (Light Dependent Resistor) sensors are positioned on either side of the solar panel. The ESP32 continuously reads and compares the light intensity from both sensors.

- If the **left sensor** detects more light → the stepper motor rotates the panel to the left
- If the **right sensor** detects more light → the stepper motor rotates the panel to the right
- If both sensors read **equal intensity** → the panel holds its current position

This closed-loop feedback system ensures the panel is always angled toward the strongest light source.

---

## 🛠️ Components Used

| Component | Description |
|---|---|
| ESP32 Dev Board | Microcontroller — handles sensor reading and motor control logic |
| Stepper Motor | Rotates the solar panel on a single axis (left/right) |
| Motor Driver Module | Controls stepper motor direction and steps |
| 2x LDR Sensors | Detect light intensity on either side of the panel |
| 2x Resistors | Form voltage dividers with LDRs for analog readings |
| Solar Panel | The load being positioned |
| Breadboard & Jumper Wires | Prototyping connections |
| Power Supply | Powers the ESP32 and motor driver |

---

## ⚙️ System Architecture

```
[ LDR Left ]──┐
               ├──► [ ESP32 ] ──► [ Motor Driver ] ──► [ Stepper Motor ] ──► [ Solar Panel ]
[ LDR Right ]─┘
```

1. ESP32 reads analog voltage from both LDR sensors
2. Compares the two readings
3. Sends step and direction signals to the motor driver
4. Motor driver drives the stepper motor accordingly
5. Loop repeats continuously in real time

---

## 💡 Key Concepts Demonstrated

- **Embedded C++ programming** on ESP32
- **Analog sensor reading** and signal comparison
- **Stepper motor control** — direction, speed, and step management
- **Real-time closed-loop feedback** system design
- **Hardware-software integration** — physical components responding to live sensor data
- **Renewable energy application** — practical use case in solar optimisation

---

## 📚 Background

This project was developed as part of my studies in Computer Systems Engineering at Tshwane University of Technology (TUT). It was presented to lecturers as a practical demonstration of embedded systems concepts including microcontroller programming, sensor interfacing, and motor control.

---

## 👤 Author

**Eric Dolo**  
Computer Systems Engineering — TUT  
[LinkedIn](https://www.linkedin.com/in/eric-dolo) | Doloeric37@gmail.com