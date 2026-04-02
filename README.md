# Tether-Regulation-for-Coordinated-UAV-UGV-Systems
https://youtu.be/vkr6_EDah_g

This repository presents a high-fidelity simulation framework for a tethered UAV–UGV (Unmanned Aerial Vehicle–Unmanned Ground Vehicle) system designed for cooperative inspection tasks in structured environments such as warehouses. The system combines the aerial mobility and sensing capabilities of a UAV with the endurance and support of a ground vehicle, enabling long-duration and reliable inspection operations.

A key focus of this project is the regulation of tether length, which is critical for ensuring safe and stable operation. The tether dynamically connects the UAV and UGV through a motor-driven winch, and its length must continuously adapt to the relative motion between both platforms. Improper regulation can lead to slack or excessive tension, potentially degrading system performance or causing instability.

To address this challenge, the repository implements a Lyapunov-based Event-Triggered PID (ET-PID) control strategy. Unlike conventional PID controllers that update control inputs at every time step, the proposed approach introduces a state-dependent triggering mechanism that updates the control signal only when necessary. This significantly reduces redundant actuation and computational load while maintaining high tracking accuracy. The design explicitly accounts for measurement noise in tether length estimation, improving robustness in realistic operating conditions.

The system is developed within a ROS2–Gazebo simulation environment, forming a Digital Twin of a warehouse inspection scenario. The UAV performs coordinated aerial motion, including vertical transitions for multi-level inspection, while the UGV follows ground trajectories along inspection aisles. The interaction between both platforms introduces realistic variations in tether dynamics, allowing thorough validation of the control strategy.

Simulation results demonstrate that the ET-PID controller achieves tracking performance comparable to a continuous PID baseline while significantly reducing control updates. This highlights its effectiveness in improving efficiency without compromising stability.

This repository includes simulation configurations, control implementations, and example scenarios to support reproducibility and further research. It is intended for researchers and engineers working on cooperative robotics, tethered systems, and efficient control strategies for resource-constrained autonomous platforms.
