# ⚡ Energy Consumption Forecasting using Time Series Analysis with LSTM

This project demonstrates how to forecast hourly electricity consumption using **Long Short-Term Memory (LSTM)** networks — a type of Recurrent Neural Network (RNN) — for time series prediction.

# Output Screenshot

![443652523-fcca2b48-121d-4324-87e5-427f674cf915](https://github.com/user-attachments/assets/b07eaa68-2ebb-4c1d-9dcd-94dee4db8f19)

---

## 📊 Dataset

- **Source:** [Kaggle - Hourly Energy Consumption](https://www.kaggle.com/datasets/robikscube/hourly-energy-consumption)
- **File Used:** `AEP_hourly.csv`  
- **Description:** The dataset contains hourly electricity consumption data in megawatts (MW) for the American Electric Power (AEP) service territory from 2004 to 2018.

## Output Screenshot
![image](https://github.com/user-attachments/assets/fcca2b48-121d-4324-87e5-427f674cf915)


## 📌 Problem Statement

Forecast the future hourly electricity consumption using past observations.  
This helps utilities and grid operators make better load management decisions.

---

## 🛠️ Technologies Used

- Python
- Pandas & NumPy
- Scikit-learn (MinMaxScaler)
- TensorFlow / Keras (LSTM)
- Matplotlib (for visualization)

---

## 🔄 Project Pipeline

### 1. **Data Preprocessing**
- Load CSV and convert the `Datetime` column to datetime format.
- Set `Datetime` as the index.
- Handle missing values using interpolation.
- Normalize consumption values using MinMaxScaler.

### 2. **Sequence Creation**
- Transform the time series into input/output sequences using a sliding window of 60 hours.

### 3. **Train/Test Split**
- Split the dataset into training (80%) and validation (20%) sets.

### 4. **Model Building**
- Build an LSTM model with:
  - 1 LSTM layer with 50 units
  - 1 Dense output layer
- Compile with Adam optimizer and Mean Squared Error loss.

### 5. **Training**
- Train the model for 20 epochs with a batch size of 32.

### 6. **Evaluation**
- Predict on validation data.
- Inverse transform the predictions and compare with actual values using a plot.

---

## 📈 Results

- The model successfully captures the trend and seasonality in electricity consumption.
- Visualization shows a good match between actual and predicted consumption values over time.

![Prediction Plot](example_plot.png)  
*Note: Replace with actual screenshot of your plot*

---

## 🚀 How to Run

1. Clone the repository or download the code.
2. Make sure `AEP_hourly.csv` is in the same directory.
3. Install dependencies:
   ```bash
   pip install pandas numpy scikit-learn matplotlib tensorflow
