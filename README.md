# Brain-controlled-car

This project demonstrates a brain-controlled robotic car that uses EEG (Electroencephalogram) signals to control its movement. The system captures brain signals, processes them, and translates them into motion commands for a car.

Currently, the car supports:
Forward movement
Stop control

Future enhancements aim to include:
Left and right directional control

System Architecture
EEG Signal Acquisition
Brain signals are captured using EEG electrodes.

Signal Amplification & Filtering :
Signals are amplified and filtered using the BioAmp EXG Pill to remove noise and extract usable data.

Processing Unit :
The processed signal is fed into an ESP32 microcontroller.
The ESP32 analyzes the signal patterns ( alpha waves) and determines the intended action.

Motor Control :
The ESP32 sends control signals to the motor driver module.
The motor driver controls the movement of the car.

Components Used : 
EEG Electrodes
BioAmp EXG Pill
ESP32 Microcontroller
Motor Driver Module ( L298N)
DC Motors (2 wheel setup)
Battery Pack
Chassis (Car Frame)

Working Principle :
The user wears EEG electrodes to capture brain signals.
The BioAmp EXG Pill amplifies and filters these signals.
The ESP32 reads the analog signal and processes it.
Based on predefined thresholds or patterns:
when Alpha signals exceeds a specific value ( 2000 is used here) , car moves forward and when it is less than 2000 car stops.
The ESP32 sends commands to the motor driver, which controls the motors accordingly.

Features :
Real-time brain signal processing
Wireless-capable microcontroller (ESP32)
Simple and scalable architecture
Expandable for multi-directional control

Future Scope :
Add left and right movement control
Implement machine learning for better signal classification
Improve noise filtering and accuracy
Integrate mobile app monitoring via Wi-Fi/Bluetooth
Add obstacle detection for safety

Challenges :
EEG signals are very weak and noisy
Requires proper electrode placement
Signal classification accuracy can vary between users