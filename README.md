# AI-Enabled-Accident-Detection-and-Alert-System-Using-IoT-and-Deep-Learning-for-Smart-Cities

An end-to-end IoT and AI system that detects road accidents in real time and automatically alerts emergency contacts with location and severity.

This project integrates sensor-based accident detection, GPS tracking, GSM communication, and AI-based severity classification into a complete working system. It was fully implemented and tested on hardware using Arduino and Raspberry Pi.

**System Architecture**
Arduino Uno (Part which I worked on)
* Reads sensor data (FSR + MPU9250)
* Detects impact using thresholds
* Handles false alarm logic
Raspberry Pi (Part which my teammates worked on)
* Captures accident images
* Runs ML model (ResNet / TFLite)
* Classifies severity
Communication
* GPS (NEO-6M) → location
* GSM (SIM800L) → SMS alerts
* Twilio → fallback messaging

**Working Logic**
Sensor monitoring:
* Force Sensor > 600 OR Acceleration > 3g => trigger
* 30-second validation window:
* User can cancel false alarm
If not cancelled:
* GPS coordinates fetched
* First SMS sent
Raspberry Pi:
* Captures image
* Runs AI model
* Classifies severity
Final SMS:
* Location and severity sent

**Tech Stack**
**Hardware:**
* Arduino Uno
* Raspberry Pi 4B
* MPU9250 (IMU)
* NEO-6M (GPS)
* SIM800L (GSM)
* FSR Sensor
* Pi Camera

**Software:**
* Arduino IDE (C++)
* Python
* TensorFlow Lite
* OpenCV
* KiCad (PCB Design)
* Twilio API

**Key Features**
Real-time accident detection, False alarm prevention logic, GPS-based location tracking, AI-based severity classification, Automated SMS alert system, Custom PCB design

**What I Learned**
* Sensor fusion using IMU and FSR
* Threshold-based real-time decision systems
* UART communication between Arduino and Raspberry Pi
* Hardware-software co-design
* PCB design workflow (schematic → routing → DRC → Gerber)
