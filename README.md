# 🤖 6-Axis Robot Arm with MoveIt (ROS 2)

This repository contains a **6-DOF robotic arm simulation** built using ROS 2 and integrated with MoveIt for motion planning and visualization.

The project includes a complete robot description (URDF/Xacro), MoveIt configuration, and launch files for planning, visualization, and controller execution.

---

## 🚀 Featu<img width="1501" height="906" alt="image" src="https://github.com/user-attachments/assets/d6e98763-541e-478d-b4cb-6578f8e39383" />
res

* ✅ 6-DOF robotic manipulator
* ✅ URDF/Xacro-based modular robot description
* ✅ MoveIt 2 integration for motion planning
* ✅ RViz-based visualization and interaction
* ✅ Joint trajectory planning & execution
* ✅ ROS 2 control configuration
* ✅ Ready for simulation and future hardware integration

---

## 📁 Project Structure

```bash
kuka/
 └── src/
      ├── my_robot_description/
      │    ├── launch/
      │    │    ├── display.launch.xml
      │    │    └── rviz.launch.xml
      │    │
      │    ├── urdf/
      │    │    ├── arm.xacro
      │    │    ├── common_properties.xacro
      │    │    ├── my_robot.urdf.xacro
      │    │    └── myrobot.urdf.xacro
      │    │
      │    ├── rviz/
      │    ├── CMakeLists.txt
      │    └── package.xml
      │
      └── my_robot_moveit_config/
           ├── config/
           │    ├── joint_limits.yaml
           │    ├── kinematics.yaml
           │    ├── moveit_controllers.yaml
           │    ├── ros2_controllers.yaml
           │    ├── my_robot.srdf
           │    ├── my_robot.urdf.xacro
           │    └── initial_positions.yaml
           │
           ├── launch/
           │    ├── demo.launch.py
           │    ├── move_group.launch.py
           │    ├── moveit_rviz.launch.py
           │    ├── rsp.launch.py
           │    ├── spawn_controllers.launch.py
           │    └── setup_assistant.launch.py
           │
           ├── CMakeLists.txt
           └── package.xml
```

---

## ⚙️ Requirements

* ROS 2 (Humble recommended)
* MoveIt 2
* RViz2
* colcon build system
* Ubuntu 22.04

---

## 🔧 Installation

Clone the repository into your workspace:

```bash
cd ~/kuka/src
git clone https://github.com/Mugilan-Theroboticist/6axis-robot-moveit.git
```

Build the workspace:

```bash
cd ~/kuka
colcon build
```

Source the workspace:

```bash
source install/setup.bash
```

---

## ▶️ Running the System

### 🔹 Launch MoveIt Demo (Recommended)

```bash
ros2 launch my_robot_moveit_config demo.launch.py
```

This will:

* Load the robot model
* Start MoveIt planning pipeline
* Open RViz with full configuration

---

### 🔹 Launch Robot Description Only

```bash
ros2 launch my_robot_description display.launch.xml
```

---

## 🧠 Motion Planning (MoveIt)

Using MoveIt, you can:

* Plan trajectories for the robotic arm
* Visualize motion in RViz
* Control individual joints
* Execute planned paths interactively

---

## 🎮 Usage (RViz)

1. Launch MoveIt
2. Open RViz interface
3. Use interactive markers to set target pose
4. Click **Plan** → **Execute**

---

## ⚙️ Configuration Highlights

* **Kinematics** → `kinematics.yaml`
* **Joint limits** → `joint_limits.yaml`
* **Controllers** → `ros2_controllers.yaml`
* **Planning scene** → `my_robot.srdf`

---

## 📸 Simulation Preview

(Add your screenshots in `images/` folder)

```md
![MoveIt Planning](images/moveit.png)
![Robot Model](images/robot.png)
```
<img width="192" height="138" alt="image" src="https://github.com/user-attachments/assets/d8636a3b-7706-4850-8759-e4188434b773" />

---

## 🔮 Future Improvements

* Add inverse kinematics optimization
* Integrate with real robotic arm hardware
* Add perception (camera-based object detection)
* Implement pick-and-place tasks
* Integrate with Gazebo for physics simulation

---

## 👨‍💻 Author

**Mugilan**
Robotics & Automation Engineer

---

## 📌 Notes

This project demonstrates a complete **MoveIt-based motion planning pipeline** for a 6-axis robotic arm using ROS 2, including robot modeling, control configuration, and trajectory execution.
