# 🌡️ IoT Temperature Prediction & Smart Alert System

## 📌 Overview

This project is an **IoT-based smart environmental monitoring system** that uses an ESP8266 (NodeMCU) and DHT22 sensor to measure temperature and humidity. The data is uploaded to ThingSpeak and analyzed using Machine Learning to **predict future temperature conditions** and trigger alerts proactively.

---

## 🚀 Features

* 📡 Real-time temperature & humidity monitoring
* ☁️ Cloud data storage using ThingSpeak
* 🤖 Machine Learning-based prediction (Linear Regression)
* 🌳 Smart decision system (Decision Tree Classifier)
* 🔴🟢 LED indicators for status (High/Normal)
* 🔔 Buzzer alert system with timer control
* 📲 Remote buzzer control via ThingSpeak

---

## 🛠️ Technologies Used

### Hardware

* ESP8266 (NodeMCU)
* DHT22 Sensor
* LEDs (Red & Green)
* Buzzer

### Software

* Arduino IDE
* Python (Pandas, Scikit-learn)
* ThingSpeak Cloud Platform

---

## ⚙️ System Architecture

1. Sensor collects temperature and humidity
2. ESP8266 sends data to ThingSpeak
3. Python script fetches historical data
4. ML model predicts future values
5. Decision model classifies condition
6. System triggers alert (LED + buzzer)

---

## 📊 Machine Learning Approach

### 1. Prediction Model

* Algorithm: Linear Regression
* Input: Previous temperature & humidity values
* Output: Predicted next temperature & humidity

### 2. Decision Model

* Algorithm: Decision Tree Classifier
* Input: Predicted temperature & humidity
* Output: Alert (ON/OFF)

### 3. Logic

* High Temperature → Motor ON + Red LED + Buzzer
* Normal Condition → Motor OFF + Green LED

---

## 📁 Project Structure

```
IoT-Temperature-Prediction-System/
│── arduino_code.ino      # ESP8266 sensor + alert system
│── ml_model.py           # ML prediction + decision logic
│── README.md             # Project documentation
```

---

## 🔌 Circuit Components

* DHT22 → Temperature & humidity sensing
* ESP8266 → WiFi communication
* LEDs → Status indication
* Buzzer → Alert system

---

## ▶️ How to Run

### 🔹 Step 1: Hardware Setup

* Connect DHT22 to ESP8266 (Data pin to D4)
* Connect LEDs and buzzer to digital pins

### 🔹 Step 2: Upload Arduino Code

* Open Arduino IDE
* Install required libraries:

  * ESP8266WiFi
  * ThingSpeak
  * DHT sensor library
* Upload code to ESP8266

### 🔹 Step 3: Run Python Model

```bash
pip install pandas scikit-learn
python ml_model.py
```

---

## 📡 ThingSpeak Fields

* Field 1 → Temperature
* Field 2 → Humidity
* Field 3 → Alert Status
* Field 4 → Manual Buzzer Control

---

## 🔒 Security Note

⚠️ Do NOT upload:

* WiFi credentials
* API keys

Replace them with placeholders before pushing to GitHub.

---

## 🔮 Future Improvements

* 📱 Mobile notifications (IFTTT / SMS alerts)
* 📊 Real-time dashboard visualization
* 🧠 Advanced ML models (LSTM / Time-series forecasting)
* 🌍 Multi-sensor deployment for environment mapping

---

## 🎯 Applications

* Smart homes
* Environmental monitoring
* Industrial safety systems
* Smart agriculture

---


## ⭐ If you like this project

Give it a ⭐ on GitHub and feel free to contribute!
