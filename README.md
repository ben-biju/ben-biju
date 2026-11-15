# Ben Biju

Robotics and embedded systems engineer. I write the software that runs on real vehicles and edge devices: ROS 2 autonomy stacks, microcontroller firmware, sensor fusion, and hardware-aware optimisation on ARM.

## Team work

### Makara — autonomous underwater vehicle · Team Tiburon

Software lead for **Makara**, the vehicle built for the Singapore AUV Challenge (SAUVC) 2026 by Team Tiburon, the underwater research team of NIT Rourkela. I own the entire software stack (team repository is private).

- **ROS 2 (Jazzy) stack** on a Raspberry Pi: sensor drivers, state estimation, perception, mission logic, control and actuation, organised as layered packages
- **Sensor integration**: VN-200 IMU, Doppler velocity log (DVL) and pressure sensor drivers, with mounting and lever-arm corrections
- **State estimation**: custom estimator alongside a `robot_localization` EKF, fusing IMU, DVL and pressure for depth and pose
- **Control and actuation**: 6-DOF PID running on a Raspberry Pi Pico 2, thrust allocation across eight thrusters, hardware kill switch
- **Tooling**: live tuning plots, a sensor monitor and telemetry logging for pool tests

`ROS 2` · `Python` · `C++ (Arduino)` · `Raspberry Pi` · `Pico 2`

### [VIGIA-ARM](https://github.com/VigiaLabs/vigia-raspi) — real-time road hazard detection on a Raspberry Pi 5 · Vigia Labs

**Winner, Bharat AI SoC.** A multimodal perception system (object detection, monocular depth and temporal fusion) that runs entirely on the Pi 5's CPU. I worked on the hardware side and its optimisation:

- Hardware architecture, and tuning the build for the Raspberry Pi 5
- Raspberry Pi Pico 2 firmware: BNO085 IMU (SPI) and GPS drivers, streaming timestamped IMU data at 100 Hz
- C++ sensor bridge that brings the Pico's IMU and GPS data into the pipeline, and the multimodal sensor fusion wiring
- Hardware attestation with an ATECC608 secure element: ECDSA-signed sensor packets verified on the Pi
- Hazard event logging: edge event promotion, a PostGIS ingest API and a hazard map

`C++17` · `ROS 2` · `Raspberry Pi 5` · `Pico 2` · `ONNX Runtime` · `OpenCV`

### [VIGIASearch](https://github.com/VigiaLabs/vigia-public) — evidence-backed road infrastructure assistant · Vigia Labs

Finalist, BIMSTEC IIT Madras Road Safety Hackathon 2026. A civic assistant that answers questions about Indian road infrastructure from official government documents, with citations. My contributions:

- Initial project architecture and route handling
- Multilingual voice assistant (speech-to-text and text-to-speech integration)
- Offline-first behaviour: PWA polish and replaying queued queries after reconnect
- Chat interface: answer-generation animation, citations bar, collapsible sidebar and settings

`TypeScript` · `Next.js` · `React` · `LangGraph` · `AWS Bedrock` · `PWA`

## Personal projects

| Project | What it is | Stack |
|---|---|---|
| [SiliconForge](https://github.com/ben-biju/SiliconForge) | Agentic pipeline that turns a natural-language spec into SystemVerilog, checks it structurally, simulates it with cocotb, and renders waveforms and FSM diagrams | Python, Gemini, PyVerilog, Icarus Verilog, cocotb, FastAPI, React |
| [GhostNet](https://github.com/ben-biju/ghostnet) | Browser-based peer-to-peer mesh for signed status and location reports, with on-device ML fallback when offline | React, Yjs, WebRTC, Transformers.js, Leaflet |
| [Vidyarthi Raksha models](https://github.com/ben-biju/Vidyarthi_raksha_models) | Analytics pipeline for planning school Aadhaar enrolment drives: backlog estimation, equity metrics, forecasting and route optimisation on synthetic data | Python, pandas, scikit-learn, statsmodels, Streamlit |

## Tools

**Robotics and embedded:** ROS 2 · Raspberry Pi · Pico 2 · sensor fusion · PID control
**Languages:** Python · C++ · TypeScript / JavaScript · SystemVerilog
**Hardware design:** KiCad · Icarus Verilog · cocotb
**Web:** React · Next.js · FastAPI
