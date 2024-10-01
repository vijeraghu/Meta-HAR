**Meta-HAR: A Meta-Learning Framework for Human Activity Recognition**

**Objective**
Meta-HAR aims to develop a robust meta-learning framework for Human Activity Recognition (HAR), addressing the challenge of domain shift commonly encountered in sensor data from various devices and individuals. Traditional deep learning models require extensive labeled data to generalize across different subjects or sensor devices, which is resource-intensive. Meta-HAR is designed to adapt efficiently to new subjects or devices with minimal data, making it ideal for applications in healthcare, fitness tracking, and smart IoT devices. By leveraging meta-learning, we propose a solution that reduces the need for large-scale data collection while maintaining high performance in real-world scenarios.

**Dataset**
For this project, we use a subset of the PAMAP2 Physical Activity Monitoring Dataset. The dataset includes over 10 hours of data collected from nine subjects performing daily activities. Sensors used:

IMUs on the hand, chest, and ankle, recording at 100Hz
Heart rate monitor with a sampling rate of approximately 9Hz
We focus on four main activity classes:

Lying
Sitting
Standing
Walking
Each data file contains 54 columns, including timestamps, activity IDs, heart rate data, and IMU sensory data like temperature, acceleration, gyroscope, and magnetometer readings.

**Data Preprocessing**
Activity Filtering: We filter out data from activities such as running and cycling.
Downsampling: IMU data is downsampled to 10Hz to match the heart rate sampling frequency for manageable computation.
Missing Data Handling: Missing values are imputed using advanced imputation techniques to ensure data quality.
Introduction
As IoT sensors and wearable devices become integral to daily life, HAR is increasingly important in fields such as healthcare, fitness tracking, and workplace safety. However, deep learning models often face challenges when dealing with domain shifts, where new subjects or devices introduce variations in sensor data. Meta-HAR tackles this issue using meta-learning to build adaptable models, which can generalize to unseen data with minimal retraining, improving efficiency and reducing data collection costs.

**Applications:**
Health Monitoring: For chronic disease management and real-time fitness tracking.
Workplace Safety: HAR can reduce injuries by detecting risky behaviors.
Smart Living: Supports independent living for the elderly by recognizing falls and unusual activity patterns.
State-of-the-Art Approaches
Meta-HAR draws inspiration from the following papers:

Efficient Deep Clustering of Human Activities (Mahon & Lukasiewicz, 2022): This work emphasizes the difficulties of obtaining labeled data for HAR and proposes deep clustering to address this issue. The paper's focus on minimizing labeled data aligns with Meta-HAR's goal of domain shift adaptation.

Invariant Feature Learning for Sensor-based Human Activity Recognition (Hao et al., 2020): The authors propose a framework combining meta-learning and multi-task learning to extract robust features across different domains. Their work highlights the importance of invariant features in tackling domain shift.

RF-Net: A Unified Meta-Learning Framework for One-Shot Human Activity Recognition (Ding et al., 2020): This work explores one-shot HAR with RF signals. The use of meta-learning to adapt with minimal labeled data parallels our goal of quickly generalizing across new subjects and environments.

**Proposed Approach**
Meta-Learning Framework
Meta-HAR employs a meta-learning framework to enable rapid adaptation to new domains (e.g., new subjects or sensors). We focus on learning invariant features from sensor data that can generalize across different individuals and contexts. The proposed framework involves:

Task-based Learning: We define train and test tasks with query pairs to model the adaptation process.
Downsampling & Data Fusion: Sensor data from IMUs and the heart rate monitor are fused and downsampled to a common frequency to improve efficiency while retaining key features.
Imputation for Missing Data: Null values are handled using advanced imputation techniques to preserve data integrity.
Expected Outcome
We expect that by applying meta-learning principles, the model will quickly generalize to unseen subjects or devices without requiring extensive retraining, making it highly applicable to real-world scenarios like personalized health monitoring.

**Contributions**
Meta-Learning for HAR: Introduced a novel meta-learning framework for HAR to address domain shift across individuals and devices.
Efficient Data Handling: Downsampled high-frequency IMU data to improve computational efficiency while maintaining the integrity of key features.
Robust to Missing Data: Employed imputation techniques to handle missing values, ensuring that model performance is not compromised.
Dataset
Source: PAMAP2 Physical Activity Monitoring dataset.
Classes: Lying, Sitting, Standing, Walking.
Sensors: 3D accelerometer, gyroscope, magnetometer (IMU sensors), and heart rate monitor.
Subjects: 9 (1 female, 8 males).

**Conclusion**
Meta-HAR represents a significant step forward in addressing the challenges of domain shift in sensor-based Human Activity Recognition. By incorporating a meta-learning framework, this project enables efficient adaptation across various subjects and sensor devices, reducing the need for large-scale data collection and retraining. This innovation opens doors for broader applications in healthcare, smart devices, and fitness tracking, ensuring that models can generalize and perform effectively across diverse real-world environments.
