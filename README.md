# Python-EV3-Dev-Sumo-Bot
This project focused on developing a fully autonomous sumo robot using EV3Dev2 and Python, with a strong emphasis on clean, efficient behavior design. With no prior experience using the EV3Dev2 library, we rebuilt our entire control system from scratch in under two weeks, producing a compact ~50-line script that prioritizes clarity, modular logic, and real-time responsiveness.

The core architecture is built around a continuous while True control loop that dynamically updates robot behavior based on sensor input. A front ultrasonic sensor continuously measures distance and modifies a shared speed variable. When an opponent is detected within 16 cm, the robot switches from patrol speed (55) to full charge speed (100). This variable-based approach replaced our original motor-in-loop design, which caused locking issues, and resulted in smoother, more stable state transitions.

Two color sensors operate independently rather than sharing mirrored logic. Each sensor checks reflected light intensity and triggers a direction-specific escape maneuver if the arena boundary is detected. This separation allows fine control over turning radius and ensures consistent clockwise movement strategy.

The program also includes a button-triggered start sequence with a timed delay, improving competition reliability. Overall, the project demonstrates strong understanding of embedded systems logic, state-based control, sensor integration, and efficient Python implementation within the EV3Dev2 framework.
