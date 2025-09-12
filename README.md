# AI/ML Appliance Usage Predictor & Energy Optimization

## Project Overview
This project uses machine learning and deep learning (Random Forest, with option for LSTM/DNN) to predict household appliance energy usage from environmental and temporal data. It provides actionable optimization advice and usage trend visualization to help users practice sustainable energy habits.

## Features
- Predicts appliance energy usage from key features (hour, temperature, humidity, etc.)
- Provides personalized energy optimization advice
- Displays energy usage trends using intuitive charts
- Simple and clear user input fields with tooltips for each feature
- Extensible for deep learning model integration

## Tech Stack
- Python, Streamlit (web UI)
- scikit-learn (Random Forest)
- Keras/Tensorflow (Deep Learning, optional)
- MySQL (optional, for data storage)

## Installation & Usage

1. **Clone or download this repository**
2. Place your trained model file (e.g. `final_energy_model.pkl`) in the project directory.
3. Ensure dependencies are installed:
    ```bash
    pip install streamlit numpy joblib matplotlib scikit-learn
    ```
4. Run the web application:
    ```bash
    streamlit run app.py
    ```
5. Open your browser at `http://localhost:8501` and enter required feature values to predict your appliance energy use.

## Inputs
| Feature         | Description                                                  |
|-----------------|-------------------------------------------------------------|
| hour            | Current hour of day (0–23)                                  |
| T3              | Indoor temperature from sensor 3 (°C)                       |
| RH_3            | Relative humidity from sensor 3 (%)                         |
| lights          | State or count of lights switched ON                        |
| Press_mm_hg     | Outdoor atmospheric pressure (mm Hg)                        |
| RH_out          | Outdoor relative humidity (%)                               |
| Windspeed       | Outdoor wind speed                                          |

All other features use average values for robust prediction.

## Output
- Predicted appliance energy usage (in Wh)
- Advice for optimizing usage and sustainability
- Hourly usage trend chart

## Dataset
Trained on the **Appliances Energy Prediction dataset** (UCI/Kaggle), featuring environmental, temporal, and appliance usage data.


