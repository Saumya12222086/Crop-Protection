# Crop-Protection
A cinematic UAV swarm simulation for precision agriculture. Fifteen drones scan a 10×20 farm grid, prioritizing high-stress NDVI zones, healing red areas, and visualizing paths with neon trails. Features priority-based routing, soft-computing heuristics, and MP4 sci-fi animation.
📘 Precision Crop-Health Monitoring Using UAV Swarm Intelligence
A Soft-Computing Based Cinematic Simulation (Python + Matplotlib)

This repository contains a complete simulation of a futuristic UAV swarm monitoring a large wheat farm.
Fifteen drones work collaboratively to scan a 200-zone grid using NDVI-based stress values, prioritizing red zones, and dynamically updating crop health on the fly.

This project was built for Cognitive CodeQuest 2025 to demonstrate soft-computing, optimization, and real-time swarm visualization.

🌾 Overview

The farm is divided into 10×20 = 200 zones.
Each zone has a continuous priority value (0–1) representing NDVI-based crop stress:

🔴 High stress → Priority 0.85–1.0

🟧 Medium-high → 0.6–0.85

🟨 Medium → 0.3–0.6

🟩 Low stress → 0–0.3

Fifteen UAVs coordinate to:

✔ Visit highest priority zones first
✔ Plan efficient routes
✔ Avoid re-scanning healthy zones
✔ Heal or reduce stress values after scanning
✔ Create visually stunning neon-trail cinematic effects

The output is a full MP4 simulation video with sci-fi aesthetics.

⚙️ Key Features
🟥 Priority-First UAV Routing

Zones are sorted by NDVI stress and assigned to UAVs starting from highest priority.
Each UAV starts at its highest-priority zone and uses a priority-weighted nearest-neighbor algorithm to build a path.

🚁 Intelligent UAV Behavior

Each UAV:

Moves toward its target zone

Pauses to scan

Modifies the zone’s stress (visually healing it)

Continues to the next zone

Returns to base after completing its list

✨ Cinematic Visualization

Neon color palette

Glowing UAV halos while scanning

Fading trails

Realistic motion

Smooth transitions

MP4 export using FFMpegWriter (H.264 + yuv420p)
→ 100% compatible with PowerPoint, YouTube, browser players

🎨 Dynamic Zone Color Transformation

After scanning:

Very high stress (≥0.85) → instantly healed (green)

Others reduce to 20% of their previous value

Zones pulse brightly when scanned

The result is a visually striking “healing wave” across the farm.

🧠 Optimization Logic

This simulation uses lightweight soft-computing ideas:

✔ Priority-based global assignment

Zones are sorted by stress and distributed round-robin across UAVs.

✔ Priority-weighted nearest neighbor

Distance → 70% weight
Zone priority → 30% weight
This ensures drones “jump” to important zones even if slightly farther.

✔ Multi-zone path construction

Each UAV scans an entire cluster efficiently.

🗂 Folder Structure
├── uav_sci_fi_sim.py         # Main simulation script
├── uav_sci_fi_sim.mp4        # Generated video output (after running script)
├── README.md                 # Full documentation
└── assets/                   # Screenshots, diagrams, visuals (optional)

▶️ Running the Simulation
Install dependencies
pip install numpy matplotlib imageio

Run the script
python uav_sci_fi_sim.py

Output

A cinematic video appears in the project directory:

uav_sci_fi_sim.mp4

🎯 Applications

This project is ideal for:

Precision agriculture

UAV swarm research

Soft computing demonstrations

Optimization competitions

Robotics & simulation coursework

Presentations & hackathons

Visualization of NDVI-based crop assessment

📡 Future Enhancements

Planned or optional features:

Collision-avoidance rings

Battery-aware routing

Multi-pass scanning

Real-time NDVI variation during simulation

GA/PSO hybrid optimization

Live dashboard overlay (speed, heading, stress level)

✍️ Author

Saumya Singh
