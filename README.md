# TECHIN515 Lab 4 - Magic Wand

This project implements a gesture recognition system on an ESP32 using an MPU6050 IMU and a model trained with Edge Impulse. The system detects three gestures ("Z", "O", "V") and gives real-time feedback using an RGB LED. A button (limit switch) is used to trigger gesture capture and inference.

--

## Setup Instructions

### 1. Hardware Assembly

- **Connect the MPU6050 (I2C)**  
  - SDA → GPIO21  
  - SCL → GPIO22  
  - VCC → 3.3V  
  - GND → GND

- **Connect the RGB LED (Common Anode)**  
  - R → GPIO3  
  - G → GPIO4  
  - B → GPIO5

- **Connect the Button (Trigger)**  
  - One end to **GPIO20**  
  - Other end to **GND**

- **Power the board** via USB-C or battery.

--

### 2. Data Collection (Optional for training)

1. Upload `gesture_capture.ino` to your ESP32.
2. Run the Python script to collect data:
   ```bash
   python process_gesture_data.py --gesture "Z" --person "yourname"
