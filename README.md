# Adaptive Assembly Robot

A vision-guided robotic assembly system using the SO-101 arm, Viam, and ESP32.
The robot uses computer vision to detect part misalignment and correct its
pick position in real time before assembly.

## System architecture
- **SO-101 arm** — pick, inspect, and place
- **Viam** — vision service, motion planning, control logic, dashboard
- **ESP32** — IR presence sensor, status LEDs, override button
- **OpenCV** — color detection, centroid extraction, offset computation

## Repo structure
firmware/esp32/     ESP32 sensor + LED firmware
robot_control/      Python control scripts (Viam SDK)
vision/             OpenCV detection pipeline
viam_config/        Viam machine JSON config
cad/                3D printable parts and mounts
media/              Demo GIFs and screenshots

## Quick start
\`\`\`bash
pip install -r requirements.txt
python3 robot_control/pick_and_place.py
\`\`\`

## Status
Active development — arm not yet connected, running fake arm via Viam.
