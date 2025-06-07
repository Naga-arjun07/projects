# 🔦 LED Control with Hand Gesture using OpenCV, MediaPipe, and Arduino

This project demonstrates a gesture-controlled LED system using **Python**, **OpenCV**, **MediaPipe**, and **Arduino**. Hand gestures captured through a webcam are processed in real-time to toggle an LED connected to an Arduino board — enabling contactless, intuitive control.

# 📸 Features

* Real-time hand tracking using **MediaPipe**
* Gesture recognition using **OpenCV**
* Serial communication with **Arduino** over USB
* Toggle LED with specific hand gestures (e.g., open palm = ON, closed fist = OFF)

# 🛠️ Tech Stack

* **Python 3.x**
* **OpenCV** – for real-time video capture and image processing
* **MediaPipe** – for efficient hand landmark detection
* **PySerial** – for Arduino communication
* **Arduino UNO/Nano** – connected to LED

# 🧠 How It Works

1. **Hand Detection**: The webcam captures live video feed.
2. **Gesture Recognition**: MediaPipe identifies hand landmarks. A simple rule-based system interprets gestures.
3. **Serial Communication**: Recognized gestures send commands (`'1'` for ON, `'0'` for OFF) to the Arduino over serial.
4. **LED Control**: Arduino receives the command and toggles the LED accordingly.

# 🔌 Hardware Requirements

* Arduino UNO/Nano (or compatible board)
* USB Cable for Arduino
* Breadboard + Jumper Wires
* 1x LED + Resistor (220Ω recommended)
* Webcam (Laptop cam or external)

# 🧰 Software Requirements

* Python 3.x
* OpenCV
* MediaPipe
* PySerial
* Arduino IDE

# 📦 Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/yourusername/gesture-led-control.git
   cd gesture-led-control
   ```

2. **Install Python dependencies**

   ```bash
   pip install opencv-python mediapipe pyserial
   ```

3. **Upload Arduino Code**

   * Open `led_control.ino` from the repo in Arduino IDE.
   * Select your board and port, then upload the code.

4. **Run Python Script**

   ```bash
   python gesture_control.py
   ```

# ✋ Sample Gesture Logic

| Gesture     | Action       |
| ----------- | ------------ |
| Open Palm   | Turn LED ON  |
| Closed Fist | Turn LED OFF |

*(You can customize more gestures as needed.)*

# 🧪 Demo

![Demo GIF](link_to_demo.gif)
*Live hand tracking and LED toggling*

# 📁 File Structure

```
gesture-led-control/
├── gesture_control.py       # Main Python script
├── led_control.ino          # Arduino sketch
├── README.md                # Project description
└── requirements.txt         # Python dependencies
```

# 📌 Notes

* Ensure correct COM port is selected in Python script.
* Gesture recognition may vary in low lighting or background clutter.

