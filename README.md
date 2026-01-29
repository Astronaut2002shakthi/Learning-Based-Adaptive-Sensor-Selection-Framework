# **Adaptive Sensor Selection Framework for Air Quality Monitoring Device (APMD)**

This repository contains the implementation and documentation of an Adaptive Sensor Selection Framework developed during the IAS–INSA–NASI Summer Research Fellowship Programme 2022. The framework focuses on improving energy efficiency in IoT-based multi-parameter wireless sensor networks (WSNs) by intelligently selecting active sensors while predicting inactive sensor data using machine learning.

### **📌 Project Overview**

IoT sensor nodes are typically battery-powered and face strict energy constraints. In multi-parameter sensing environments, many sensors exhibit strong cross-correlation, enabling intelligent prediction of certain parameters without activating all sensors. This project presents a learning-based adaptive sensor selection framework that:

* Dynamically selects an optimal subset of sensors
* Predicts inactive sensor readings using Gaussian Process Regression (GPR)
* Minimizes sensing and transmission energy
* Maintains prediction error below 1%
* Achieves up to 54% energy savings

The framework is modeled as a Multi-Armed Bandit (MAB) problem and solved using a Discounted Upper Confidence Bound (UCB) algorithm.

### **🧠 Key Concepts & Techniques**

* Adaptive Sensor Selection
* Gaussian Process Regression (GPR) with composite kernels
* Discounted UCB Algorithm
* Cross-correlation and temporal correlation exploitation
* Nyquist-based adaptive sampling
* Edge intelligence for IoT systems

### **🏗 System Architecture**

**Sensor Hub:** Multi-parameter node with 7 sensors monitoring 9 environmental parameters <br/>
**Active Sensors:** Selected optimally each measurement cycle <br/>
**Sleep Sensors:** Predicted using trained GPR models <br/>
**Edge Node:** Performs learning, prediction, and feedback control <br/>

### **⚙️ Software Requirements**

To run or extend this project, the following tools are required:

* Python 3.9
* Anaconda
* VS Code (recommended)

### **Required Python libraries:**

* numpy
* scikit-learn
* scipy
* matplotlib
* pandas

### **🧪 Experimental Setup**

Deployment: Air Pollution Monitoring Device (APMD) at IIT Delhi

### **Sensors Used:**

* Temperature & Humidity (DHT11)
* NH₃ (MQ-137)
* NO₂, O₃, CO, SO₂ (Alphasense AFE-A4)
* PM₂.₅, PM₁₀ (Alphasense OPC-N3)

Training Data Size: 1500–1600 samples (optimal) <br/>
Correlation Threshold: 0.5 (maximizes reward and energy savings)

### **📊 Performance Highlights**

* Mean Relative Error (MRE): < 1%
* Energy Savings: Up to 54%
* Prediction Confidence: 95% (GPR)

### **🚀 How It Works (High-Level Flow)**

* Collect multi-parameter sensor data
* Train GPR models using correlated parameters
* Compute cross-correlation and energy cost
* Select optimal sensor set using Discounted UCB
* Adapt measurement cycle dynamically
* Predict inactive sensor data
* Transmit reduced data with minimal energy usage

### **📚 References**

1) S. Ghosh, S. De, S. Chatterjee, and M. Portmann, “Learning-based adaptive sensor selection framework for multi-sensing wsn,” IEEE Sensors Journal, vol. 21, no. 12, pp. 13 551–13 563, 2021. doi:10.1109/JSEN.2021.3069264.
2) S. Ghosh, P. Das, S. Murugesh, S. De, S. Chatterjee and M. Portmann, "Energy Aware Smart Sensing and Implementation in Green Air Pollution Monitoring System," ICC 2023 - IEEE International Conference on Communications, Rome, Italy, 2023, pp. 2153-2158, doi: 10.1109/ICC45041.2023.10279138


**👩‍💻 Author**

Shakthi Priya M <br/>
Summer Research Fellow (IAS–INSA–NASI) <br/>
Electrical Engineering <br/>
Guided by Prof. Swades De, IIT Delhi <br/>

**📜 License**

This project is intended for academic and research use only.
Please cite the original references if you use or extend this work.
