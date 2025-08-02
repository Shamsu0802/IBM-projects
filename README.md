# Smart Sprinkler System

An AI-powered farm irrigation system that predicts the ON/OFF status of 20 sprinkler zones using sensor values. This project aims to optimize water usage and ensure efficient crop irrigation based on sensor data.

---

## Table of Contents

- [Problem Statement](#problem-statement)  
- [Objectives](#objectives)  
- [Proposed Solution](#proposed-solution)  
- [Architecture](#architecture)  
- [Tech Stack Used](#tech-stack-used)  
- [Installation Steps](#installation-steps)  
- [How to Run](#how-to-run)  
- [Model Overview](#model-overview)  
- [Features](#features)  
- [Sample Use-Case](#sample-use-case)  
- [Output Screenshots](#output-screenshots)  
- [Future Scope](#future-scope)  
- [Acknowledgements](#acknowledgements)  
- [File Structure](#file-structure)  


---

## Problem Statement

Efficient irrigation is a major concern in modern agriculture. Over-irrigation leads to water wastage, while under-irrigation affects crop yield. Farmers need a reliable, automated solution to control sprinkler systems based on real-time sensor input.

---

## Objectives

- Develop a system that takes scaled sensor inputs and predicts sprinkler states.
- Provide an intuitive web interface for farmers to input data and view results.
- Reduce water wastage through intelligent irrigation decisions.
- Demonstrate the feasibility of AI in real-world agricultural applications.

---

## Proposed Solution

We propose a **Smart Sprinkler System** built using machine learning and deployed with a Streamlit interface. The model predicts whether each sprinkler (parcel_0 to parcel_19) should be ON or OFF based on environmental sensor data.

---

## Architecture

```
Sensor Data (0–1 scaled)
        ↓
Pre-trained ML Model (classification)
        ↓
Predicted ON/OFF for each sprinkler
        ↓
Streamlit Interface Output
```

---

## Tech Stack Used

- **Python**
- **NumPy**
- **Streamlit**
- **scikit-learn**
- **Joblib** (for model serialization)

---

## Installation Steps

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/smart-sprinkler-system.git
   cd smart-sprinkler-system
   ```

2. Create a virtual environment and activate it:
   ```bash
   python -m venv venv
   source venv/bin/activate   # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Place the `Farm_Irrigation_System.pkl` model in the project directory.

---

## How to Run

Run the Streamlit app using:

```bash
streamlit run app.py
```

Then open the provided local URL in your browser to interact with the system.

---

## Model Overview

- The model is trained on scaled sensor data (20 features).
- It performs multi-output binary classification to predict the ON/OFF state for each of 20 sprinklers.
- Output: An array of 20 binary values (0 = OFF, 1 = ON).

---

## Features

- Accepts 20 real-time scaled sensor inputs.
- Predicts ON/OFF status for each sprinkler.
- Clean, interactive UI using Streamlit.
- Lightweight and fast response.

---

## Sample Use-Case

A farmer inputs current soil moisture, humidity, temperature, etc. (scaled between 0 and 1) into the app. The model instantly predicts which sprinkler zones should be turned ON, helping save water and optimize crop growth.

---

## Output Screenshots

Below are some sample screenshots of the Smart Sprinkler System in action:

### 🎛️ Input Interface
Users can input scaled sensor values (0 to 1) using sliders for each of the 20 sensors.
<img width="1920" height="961" alt="image" src="https://github.com/user-attachments/assets/90245b0e-d57c-489b-ae6b-21d53d28be29" />
<img width="1920" height="991" alt="image" src="https://github.com/user-attachments/assets/22216493-4953-43de-a791-da66598a8e66" />
<img width="1920" height="976" alt="image" src="https://github.com/user-attachments/assets/d253f3a6-8b76-4cb8-bea7-a5a59505532e" />



---

### ✅ Prediction Output
After clicking the **Predict Sprinklers** button, the system displays the ON/OFF status for each sprinkler zone (parcel_0 to parcel_19)
<img width="1920" height="1003" alt="image" src="https://github.com/user-attachments/assets/142fd274-1163-4bf9-944b-79809971236a" />

---


## Future Scope

- Integrate live sensor feed using IoT.
- Add automatic actuator control to trigger sprinklers directly.
- Use time-series models to predict irrigation schedules.
- Provide alerts or daily reports to farmers via SMS/email.

---

## Acknowledgements

- **Edunet Foundation**
- **AICTE**
- **Shell India**
- **Mentor**: Hariharan Sir  
- **Coordinator**: Nikita Ma’am – [LinkedIn](https://www.linkedin.com/in/nikita)

---

## File Structure

```
├── app.py                      # Main Streamlit application
├── Farm_Irrigation_System.pkl  # Trained ML model
├── requirements.txt            # List of Python dependencies
└── README.md                   # Project documentation
```
