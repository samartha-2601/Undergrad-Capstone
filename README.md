# Air Pollution Monitoring, Forecasting and Controlling System

An IoT-based system that monitors real-time air quality, forecasts future pollution levels, and provides actionable recommendations to improve air quality and protect public health.

## Overview

Air pollution poses significant risks to human health and the environment. This project demonstrates a low-cost, IoT-enabled solution that combines hardware sensors with machine learning to provide comprehensive air quality management.

## Features

- **Real-time Monitoring**: Continuous measurement of air pollutants using multiple sensors
- **5-Day Forecasting**: Machine learning-powered predictions of future air quality levels
- **Web Dashboard**: Interactive analytics displaying current and forecasted AQI
- **Smart Recommendations**: Automated suggestions for pollution control measures
- **Health Advisories**: Precautionary measures based on current air quality

## System Architecture
```
Air Pollutants → Arduino + Sensors → Cloud Server → Web Application
                                    ↓
                              ML/DL Model (Forecasting)
```

The system follows a modular approach with three main components:

1. **IoT Device**: Arduino-based monitoring station with gas sensors
2. **Cloud Backend**: Data storage and ML model for forecasting
3. **Web Interface**: User-facing dashboard with analytics and recommendations

## Hardware Components

- **Arduino Microcontroller**: Central processing unit
- **MQ135 Sensor**: General air quality measurement
- **MQ131 Sensor**: Ozone (O₃) detection
- **MQ7 Sensor**: Carbon monoxide (CO) detection
- **PM2.5 Sensor**: Particulate matter measurement

## Methodology

### 1. Monitoring Module
The IoT device continuously measures concentrations of various air pollutants. Sensor data is processed to calculate the Air Quality Index (AQI) and stored in a database for analysis and forecasting.

### 2. Forecasting Module
Using historical data collected from the monitoring module, an AutoRegression machine learning model predicts AQI levels for the next 5 days. This model was selected based on extensive research and literature review for optimal accuracy.

### 3. Controlling Module
Based on the current AQI category (Good, Satisfactory, Moderate, Poor, Very Poor, or Severe), the system provides:
- Targeted recommendations to improve air quality
- Precautionary health measures for different population groups

## AQI Categories

| Category | AQI Range | Health Implications |
|----------|-----------|---------------------|
| Good | 0-50 | Minimal impact |
| Satisfactory | 51-100 | Minor breathing discomfort |
| Moderate | 101-200 | Breathing discomfort for sensitive groups |
| Poor | 201-300 | Breathing discomfort for most people |
| Very Poor | 301-400 | Respiratory illness on prolonged exposure |
| Severe | 401-500 | Health alert - everyone may experience serious effects |


## Usage

1. **Deploy the IoT Device**: Place the Arduino-based monitoring station in your desired location
2. **Access the Dashboard**: Navigate to the web application URL
3. **View Current AQI**: Check real-time air quality measurements
4. **Check Forecast**: Review 5-day AQI predictions
5. **Follow Recommendations**: Implement suggested control and precautionary measures

## Technologies Used

- **Hardware**: Arduino, MQ135, MQ131, MQ7, PM2.5 sensors
- **Machine Learning**: AutoRegression model
- **Backend**: Python (Flask/Django)
- **Database**: MySQL/PostgreSQL
- **Frontend**: HTML, CSS, JavaScript
- **IoT Communication**: MQTT/HTTP

## Project Team

**Students:**
- Prateek M Gummaraju (1BM19IS117)
- Ruchi Agarwal (1BM19IS133)
- Samartha S (1BM19IS219)

**Supervisor:**
- Prof. Pallavi B, Assistant Professor

**Institution:**
- Department of Information Science and Engineering
- B. M. S. College of Engineering
- Autonomous College under VTU

## Future Enhancements

- Integration with government air quality monitoring networks
- Mobile application for on-the-go monitoring
- Extended forecast period (7-14 days)
- Advanced visualization with heat maps
- Multi-location monitoring support
- SMS/Email alerts for critical AQI levels

## Acknowledgments

- B. M. S. College of Engineering for providing resources and support
- Prof. Pallavi B for guidance throughout the project
- Open-source community for various libraries and tools used


---

**Note**: This project was developed as part of an academic curriculum at B. M. S. College of Engineering.
