# 👣 Footprint Count Using Face Recognition

### 🎓 Bachelor of Engineering 
**Department:** Electronics & Telecommunication Engineering  
**Institution:** Yeshwantrao Chavan College of Engineering, Nagpur  
**Academic Year:** 2019–2023  

**Team Members:**  
- Saloni Giratkar  
- Samruddhi Uplapwar  
- Yashaswi Rewatkar  
- Nikita Parate  

**Guide:** Dr. Yogita Chitriv (Dubey)  

---

## 🧠 Executive Summary

The project **"Footprint Count Using Face Recognition"** presents a real-time system that counts and classifies people entering a shopping center using **facial recognition** and **gender detection**.  

The system uses a **Raspberry Pi** and **Pi Camera** to capture live video feeds. It applies the **Viola–Jones Algorithm** for face detection and the **Convolutional Neural Network (CNN)** for gender classification.  
Detected faces are matched with a stored dataset — known faces (employees) are identified, and unknown faces (customers) are counted automatically.  

All data is transmitted via **MQTT Protocol** to an Android app dashboard for real-time display.  
This innovative system provides insights into customer traffic, gender demographics, and shop growth analytics.  

---

## ⚙️ Methodology

The project is divided into five main phases:

### 1. **Face Detection**
- The input image is captured via Pi Camera.  
- Converted to grayscale and enhanced through contrast stretching.  
- **Viola–Jones Algorithm** is applied for fast and accurate detection using:
  - **Haar-like features**
  - **Integral Image**
  - **Adaboost algorithm**
  - **Cascade Classifier**

### 2. **Face Recognition & Counting**
- Detected faces are compared with a known dataset.
- If the face does not match, it is labeled **“Unknown”**.
- The system sends a message with the tag *“unknown”* to the **MQTT App**, which increments the visitor count.

### 3. **Gender Detection**
- Implemented using **Convolutional Neural Network (CNN)**.
- CNN is divided into:
  - **Pre-processing:** Noise reduction and normalization (96×96 image resizing).  
  - **Feature Extraction:** Convolution + Pooling + ReLU layers.  
  - **Classification:** Fully connected layer with **sigmoid classifier** to label **Male** or **Female**.

### 4. **Hardware Setup**
- **Raspberry Pi 3 Model B+**
- **Pi Camera Module**
- **5V 2A Power Supply**
- **PVC setup enclosure**

### 5. **Software & Tools**
- **Programming Language:** Python  
- **Libraries:** OpenCV, NumPy, TensorFlow, Keras, paho-mqtt  
- **Dashboard:** Android MQTT App  

---

### 📊 Methodology Flowchart
<img width="682" height="442" alt="image" src="https://github.com/user-attachments/assets/7ff0fa5a-e74d-4e21-8f1f-4679d76f44a5" />


