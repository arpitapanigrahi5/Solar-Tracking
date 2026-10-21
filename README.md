# Solar-Tracking
Automatic Solar Panel Tracking System Using Light Intensity Sensors
Multidisciplinary Project, VIT Vellore, 2026
Overview
Solar panels convert sunlight into electricity, but a fixed panel cannot follow the Sun and spends much of the day at a suboptimal angle. This project designs a prototype that detects the direction of maximum light intensity and automatically rotates a solar panel toward it. It also tests, with measured data, whether tracking generates more energy than a fixed panel.
How it works
Four Light Dependent Resistors (LDRs) around the panel measure light from different directions. A microcontroller (Arduino or ESP32) compares the readings and drives a servo or geared motor to turn the panel toward the brighter side. After each movement the sensors are read again, and the cycle repeats until the readings balance, meaning the panel is aligned with the light. Voltage and current sensors record the panel’s output (P = V × I).
Experimental investigation
The core of the project is a side-by-side comparison of a fixed panel and a tracking panel. Light intensity, voltage, current, power, panel angle and energy are logged every 15–30 minutes. Energy improvement is calculated as:
Improvement (%) = (Energy tracking − Energy fixed) ÷ Energy fixed × 100
The result is determined by the experiment, not assumed in advance.
Interactive simulation
To demonstrate the concept ahead of the hardware, I built a web-based simulation that models a full day from 6:00 to 18:00. It shows live LDR readings, the controller’s decisions, and the voltage, current, power and energy of both panels. It also plots power and panel angle against time and calculates the percentage improvement. Cloud cover, controller sensitivity and motor energy use can be adjusted. The simulation uses a simplified model and validates the control logic and analysis method. The final results will come from physical testing.
Live demo: https://claude.ai/artifact/8Bk5NQBRBCb8BBvwngp6FB
Multidisciplinary scope
Physics: solar radiation, angle of incidence, the photovoltaic effect
Programming: embedded C/C++, sensor data acquisition, control algorithm, data logging
Electronics: LDR sensing, voltage and current measurement, motor control
Mathematics: sensor comparison, angle, power and energy calculations, statistical analysis
Mechanical engineering: rotating mechanism, panel mounting, structural stability
Deliverables
A working tracking prototype, light-sensing circuit, microcontroller control system, motorised rotation mechanism, voltage and current measurement system, experimental dataset with graphs and performance comparison, final report, and live demonstration.
Limitations and future work
LDRs are affected by shadows, reflections and clouds, and the motor itself uses energy, so these are accounted for in the analysis. Planned improvements include wireless monitoring with the ESP32, a cloud dashboard, more accurate photodiodes, dual-axis tracking, and combining sensor feedback with a solar-position algorithm.
Tools and skills: Arduino IDE, Embedded C/C++, sensor interfacing, data analysis, web-based simulation (HTML/JavaScript)
