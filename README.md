# Path Planning with Obstacle Avoidance (6DOF Robot)

This repository implements global and local path planning with obstacle avoidance for a 6DOF robot arm, powered by the **NVIDIA Jetson Orin Nano**.

---

## 🛠 Prerequisites & Preparation

Before running the system, ensure the following steps are completed:

1.  **Hardware Check**: Verify all cables are correctly connected as shown in the diagram below.
    
2.  **Power On**: Turn on the robot and ensure the **Emergency Stop button is unwound** (released).
3.  **Startup**: Wait for the BIOS startup chime to signify the system is ready.

---

## 🚀 How to Run

1.  Open a new terminal.
2.  Navigate to the workspace directory:
    ```bash
    cd ~/Desktop/p_workspace/xarm_ws_v3/
    ```
3.  Execute the automated startup script:
    ```bash
    bash autosys_demo.sh
    ```

---

## 🛑 How to Stop

To stop the processes normally:
* Press `Ctrl + C` in every active terminal window.

---

## ⚠️ Troubleshooting & Emergency Procedures

### 1. What to do if the arm is moving erratically ("Driving Crazy")?
1.  **Immediately press the Physical Emergency Button.**
2.  Unwind the emergency button.
3.  Press `Ctrl + C` in all terminals to kill the current processes.
4.  Repeat the [How to Run](#-how-to-run) steps to re-initialize.

### 2. What to do if the arm is not moving?
* Check that the robot power is ON.
* Verify all cable connections are secure.
* Ensure the emergency button is fully unwound.

### 3. What to do if path planning fails to execute?
If the script is running but the arm remains stationary:
1.  **Check RViz**: Look for any **purple objects** (collision markers) in the scene.
2.  **Manual Intervention**: If a collision is detected or the arm is stuck, access the Web GUI at: `http://192.168.0.228`.
3.  **Center the Joints**: Use the GUI to manually move the robot, ensuring that joints **J1 through J6** are all within their center range of motion.
4.  Once cleared, restart the process from the [How to Run](#-how-to-run) section.

---
**Last Updated:** 2026-02-09
