# Hi, I'm Damian 👋

CS student at the University of the Pacific, building robots that see, fly, and walk.
Outside of robotics, I develop games independently, with a focus on multiplayer systems and AI.

## 🛠️ What I'm building

**[Jetson Gesture Drone](https://github.com/alien4rmspace/jetson-gesture-drone)**: a camera drone you fly with hand gestures, which locks onto its pilot and keeps them in frame
- Fully onboard perception on a Jetson Orin Nano: YOLO pose model on TensorRT FP16, DeepStream with NvDCF tracking and ReID-verified person lock
- Gesture flight in six directions, follow mode with auto yaw, and only the locked pilot's gestures count
- Voice-agent control through a companion iPhone app: it listens for the "Hey Bart" wake word, transcribes speech, and sends it over Wi-Fi to a local Qwen model (llama.cpp) on the Jetson, which turns it into schema-validated drone commands and speaks replies back with a response.
- One safety-gated command router for gesture and voice; MAVLink commands are sent to a Pixhawk 6C (ArduCopter) only when it's armed and in GUIDED mode
- Crash-isolated multiprocess design with a supervisor that restarts the video pipeline
- ~33k lines of Python with ~16.7k lines of tests

**Trash-Picking Hexapod** *(in progress)*: a six-legged robot that picks up litter
- Feetech STS3215 bus servos, tripod/ripple gait switching based on load
- RGB-D camera on the arm for grasping and curb detection, 2D lidar for SLAM
- Grasping policy trained with RL

**[Just Scavenge](https://github.com/alien4rmspace/Just-Scavenge-Multiplayer)**: co-op open-world zombie survival RTS (Unity/C#)
- Server-authoritative multiplayer (Netcode for GameObjects) on PlayFab dedicated servers
- ~36 player-controlled units per instance, NavMesh horde AI with sleep states, distance-based network culling

## 🔬 Other work
- **[Mandelbrot Set (CUDA)](https://github.com/alien4rmspace/Mandelbrot-Set-CUDA)**: GPU-accelerated deep-zoom renderer in C++/CUDA with SFML; ~370× faster than single-threaded CPU (374 ms → 1.0 ms per frame), with a redundant-recompute bug found and fixed using Nsight Systems
- **CUDA performance**: occupancy, warp divergence, and DRAM throughput analysis; Monte Carlo option pricing on GPU
- **ML**: ResNet-18 Pokémon card classifier with an async dataset pipeline, DataLoader tuned with Nsight Systems profiling

## 🧰 Stack
`Python` `C++` `C#` `CUDA` `PyTorch` `TensorRT` `DeepStream` `GStreamer` `MediaPipe` `MAVLink` `llama.cpp` `Jetson` `Unity` `ESP32`

## 📫 Find me
[LinkedIn](#) · [Instagram](#)
