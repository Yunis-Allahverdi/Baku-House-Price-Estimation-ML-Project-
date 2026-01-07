
# 🏠 Baku House Price Prediction Project

This project is a **machine learning–based house price prediction system** for **Baku, Azerbaijan**, combined with a **user-friendly desktop application (GUI)** built using **Tkinter**.

Users can enter basic house details (area, rooms, region, etc.), and the system predicts the **estimated house price in AZN** using a trained **Random Forest model**.

---


## Features

- 📊 Data preprocessing & cleaning
- 🤖 Machine Learning model (Random Forest Regressor)
- 🖥️ Interactive GUI (Tkinter)
- 🏙️ Region-based price prediction for Baku
- ⚡ Fast and easy-to-use interface



## Technologies Used

- **Python**
- **Pandas & NumPy** – data handling
- **Scikit-learn** – machine learning
- **Tkinter** – graphical user interface
- **PIL (Pillow)** – image handling
- **Matplotlib & Seaborn** – (optional) data visualization

---
## Project Structure

- ├── processed_file_new.xlsx # Cleaned house dataset
- ├── baku_image.png # Background image for GUI
- ├── favicon.ico # Application icon
- ├── main.py # Main Python script
- └── README.md # Project documentation
## Dataset Description

- Dataset size: **35,458 rows**
- Columns:
    - `area` – House area (m²)
    - `room_number` – Number of rooms
    - `repair` – Repaired or not
    - `title_deed` – Legal document availability
    - `category` – New or old building
    - `region_new` – District of Baku
    - `price` – House price (target variable)

### 🔹 Data Cleaning Steps

- Removed unnecessary columns (`currency`, `title`, `address`, etc.)
- Converted categorical values into numeric format
- Cleaned numeric fields (`area`, `price`)
- Removed outlier regions (`Pirallahi`, `Qaradag`)
- Applied **one-hot encoding** for regions

---
## Machine Learning Model

- **Model Used:** `RandomForestRegressor`
- **Train/Test Split:** 80% / 20%
- **Target Variable:** `price`
- **Features:** area, rooms, repair status, title deed, category, region

The model learns patterns from historical house prices and predicts a realistic price for new inputs.

---
## Graphical User Interface (GUI)

The GUI guides the user step-by-step:

1. Enter house area (20–300 m²)
2. Enter number of rooms (1–10)
3. Select:
   - Title deed (Yes / No)
   - Repair status (Yes / No)
   - Building type (New / Old)
4. Choose region in Baku
5. Get predicted house price 💰

✔ Input validation  
✔ User-friendly buttons  
✔ Error handling  

---
##  How Prediction Works

1. User inputs are collected via GUI
2. Inputs are converted into a DataFrame
3. One-hot encoding is applied for the selected region
4. Trained Random Forest model predicts the price
5. Result is shown in a pop-up window

---
## How to Run the Project

### 1️⃣ Install Required Libraries

```bash
pip install pandas numpy scikit-learn matplotlib seaborn pillow
```

### 2️⃣ Run the Application

```bash
python main.py
```
## ⚠️ Notes

- Predictions are estimates, not exact market prices
- Accuracy depends on dataset quality
- Designed mainly for educational & demonstration purposes
## Future Improvements

- Model evaluation metrics (R², MAE, RMSE)
- More regions and features
- Web version (Flask / Streamlit)
- Save prediction history
- Better UI styling
## License

This project is open-source and free to use for learning and research purposes.