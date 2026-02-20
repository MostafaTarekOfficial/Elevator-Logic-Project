# 8-Level Autonomous Elevator Control System (Hardware Prototype) 🏗️

A comprehensive engineering project documenting the design and construction of a fully functional, 100 cm vertical transportation system (Ground + 7 floors). This system operates entirely on **Discrete Digital Logic**, without the use of microcontrollers like Arduino or ESP-32.

## 🚀 Key Features
- **Height:** 100 cm vertical structure.
- **Capacity:** Ground + 7 floors.
- **Logic-Based Control:** Built using only combinational and sequential logic components.
- **Memory Retention:** Implemented hardware registers to store user requests during movement.
- **Closed-Loop Feedback:** Real-time floor detection using IR sensors.

## 🛠️ Hardware Architecture & Components
The system's "brain" is built from discrete ICs:
- **Priority Encoder (74148):** To handle and prioritize multiple floor requests.
- **Magnitude Comparator (7485):** To compare the current floor with the target floor for decision making.
- **D-Flip-Flops (7474):** Used as **Command Registers** to prevent data loss during transitions.
- **Motor Driver (L293D):** For controlling the lift motor direction and speed.
- **Sensors:** IR sensors for precise floor leveling.

## 📁 System Logic Flow
1. **Request Phase:** User presses a button; the 74148 encoder converts the request into binary.
2. **Comparison Phase:** The 7485 comparator decides if the elevator should move Up, Down, or stay Idle.
3. **Execution Phase:** The motor driver receives the command while Flip-Flops hold the state until the target is reached.

## 🧠 Engineering Challenges Overcome
- **Signal Polarity Conflict:** Resolved using NOT gates to ensure logic compatibility.
- **Clock Synchronization:** Solved timing issues between the logic gates and mechanical feedback.
- **Mechanical Stability:** Designed a dual-pillar structure to handle the 100 cm height smoothly.

## 💡 Conclusion
This project served as a transition from theoretical classroom concepts to a complex, real-world hardware application. It redefined our approach to problem-solving, proving that "engineering is the ability to turn a desperate problem into a logical, working solution".

---
**Supervised by:** Dr. Fatma Sakr.
