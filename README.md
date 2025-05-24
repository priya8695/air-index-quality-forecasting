

# 🌫️ Air Quality Index (AQI) Forecasting with Deep Learning

A collaborative project focused on forecasting the Air Quality Index (AQI) using a hybrid deep learning model combining **BiLSTM**, **CNN**, and **Attention Mechanisms**. This system is designed to accurately predict AQI levels across major Indian cities using time-series pollutant data.


---

## 📌 Project Summary

Air quality index (AQI) prediction is an important problem in environmental engineering and public health, as it allows policymakers and individuals to take appropriate actions to reduce exposure to air pollution. Having the possibility to predict the trend that pollution will allow to study the future pollutant levels and extract patterns. With all that information it is possible to take the necessary actions to reduce the exposure and take care of the public health.
In this project, we proposed a machine learning approach for AQI prediction using data from multiple cities across India. Our model is trained on a large dataset of daily pollutants measurements from multiple locations, and is able to make accurate predictions for future AQI values up to 2 months in advance. Our proposed system is formed by an attention mechanism in combination with an LSTM+CNN model. We compare the performance of our model to other
state-of-the-art approaches and show that it achieves superior results in terms of prediction accuracy and robustness.
Our approach has the potential to improve air quality forecasting and help mitigate the negative impacts of air pollution on human health and the environment. 
Key techniques used:
- **BiLSTM** for sequential learning
- **CNN** for feature extraction
- **Attention Mechanism** for dynamic weighting

---

## 📊 Dataset

- **Source**: [Kaggle - Air Quality Data in India](https://www.kaggle.com/datasets/rohanrao/air-quality-data-in-india)
- **Duration**: 2015–2020
- **Cities**: 9 major cities across India
- **Pollutants**: `CO`, `PM2.5`, `PM10`, `SO2`, `NOx`, `NH3`, `O3`

---

## 🧠 Model Architecture

The model consists of:
1. **Input Layer**: Windowed time-series data of 7 pollutants.
2. **BiLSTM Layer** × 2: Captures temporal dependencies.
3. **Self-Attention Layer**: Assigns dynamic importance to time steps.
4. **1D Convolution Layer**: Extracts spatial features.
5. **Output Layer**: Predicts AQI by calculating sub-indices.

![Model Diagram](path_to_model_diagram.png) <!-- Replace with actual path -->

---

## ⚙️ Training Details

| Hyperparameter         | Value              |
|------------------------|--------------------|
| Epochs                 | 200                |
| Batch size             | 8                  |
| Window size            | 7 days             |
| Optimizer              | Nadam              |
| Loss Function          | MSLE               |
| Learning Rate          | 0.001              |
| Evaluation Metrics     | MAE, MSLE          |

---

## 📈 Results

### 📍 Prediction Horizon: 1 Month

| Metric | Value     |
|--------|-----------|
| MSLE   | 0.1942    |
| MAE    | 10.6509   |

### 📍 Prediction Horizon: 2 Months

| Metric | Value     |
|--------|-----------|
| MSLE   | 0.2442    |
| MAE    | 11.8528   |

### 📍 City-wise Example: Hyderabad (2 Months)
| Metric | Value     |
|--------|-----------|
| MSLE   | 0.4317    |
| MAE    | 20.1928   |

---

## 🚀 Use Case

This tool can be adapted for:
- City-level pollution forecasting
- Traffic restriction planning
- Environmental monitoring dashboards
- Public alert systems

---

## 🧩 Future Improvements

- Joint prediction of **AQI and temperature**
- Integration with **real-time data streams**
- Model generalization to **global datasets**
- Deployment as a **web service or API**

---

## 👩‍💻 Authors

- **Vicent Descals Carbonell** - [v.descals.carbonell@umail.leidenuniv.nl](mailto:v.descals.carbonell@umail.leidenuniv.nl)
- **Priya Prabhakar** - [priya8695@gmail.com](mailto:priya8695@gmail.com)

---



