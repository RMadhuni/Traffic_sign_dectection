# Traffic Light Detection & Autonomous Control in CARLA 0.9.11

This project implements a simple autonomous control system using the CARLA simulator (version 0.9.11). The system detects **traffic lights** using camera data, and controls the vehicle to **stop at red lights** and **go at green lights** accordingly.

## Features:

-  **Traffic Light Detection** using RGB camera and bounding boxes.
-  **Stop and Go Logic**: The vehicle halts at red lights and resumes movement on green.
-  **Autonomous Control**: Adjusts throttle and brake automatically based on the traffic light state.

## Technologies Used

- **Simulator**: [CARLA Simulator 0.9.11](https://github.com/carla-simulator/carla)
- **Language**: Python 3
- **Libraries**:
  - `pygame` – For rendering the simulation window
  - `cv2` (OpenCV) – For image processing (if extended)
  - `numpy`, `time`, `math`, `random` – For computations and timing logic


## How It Works

1. **Sensor Setup**: The vehicle is equipped with a front-facing RGB camera and other sensors in CARLA.
2. **Traffic Light Detection**:
   - The script detects traffic lights using CARLA's built-in environment information (bounding boxes).
   - Determines the state of the light (Red/Green).
3. **Control Logic**:
   - If the traffic light is red and ahead, the vehicle applies brakes and stops.
   - If the traffic light is green or there’s no relevant red light, the vehicle continues driving.

##  How to Run the Project

1. **Install Python Dependencies**:
   ```bash
   pip install pygame opencv-python numpy
   
2. **How to use:**
CarlaUE4.exe    # On Windows

3. **Expected Behavior:**
    Vehicle stops smoothly when a red light is detected in front of it.
    It resumes motion once the light turns green.
    Behavior is handled automatically via control logic.

