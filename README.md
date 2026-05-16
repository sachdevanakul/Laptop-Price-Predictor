# 💻 Laptop Price Predictor

A machine learning web application that estimates laptop prices based on hardware specifications and brand. Built with Python, scikit-learn, and deployed on Hugging Face Spaces.

[![Hugging Face Spaces](https://img.shields.io/badge/🤗%20Hugging%20Face-Spaces-blue)](https://huggingface.co/spaces/NakulSachdeva/laptop-price-predictor)

---

## 🚀 Live Demo

🔗 **[Try it here → huggingface.co/spaces/NakulSachdeva/laptop-price-predictor](https://huggingface.co/spaces/NakulSachdeva/laptop-price-predictor)**

Enter your laptop's specifications — brand, type, RAM, storage, GPU, and more — and get an instant predicted price.

> ℹ️ The Space may be sleeping due to inactivity. Click **Restart this Space** on the page to wake it up.

---

## 📌 Features

- **Smart Feature Extraction** — Parses brand, processor type, RAM, storage, GPU, screen size, OS, and more from raw data
- **Data Preprocessing Pipeline** — Handles missing values, encodes categorical variables, and scales numerical features automatically
- **Multiple ML Models** — Trains and compares models including Linear Regression and Random Forest Regressor
- **Model Evaluation** — Uses MAE and R² score to select the best-performing model
- **Serialized Pipeline** — Saves the trained pipeline (`pipe.pkl`) and cleaned dataset (`df.pkl`) for fast inference
- **Flask Web App** — Clean, interactive UI for real-time price prediction (`app.py`)

---

## 🗂️ Project Structure

```
Laptop-Price-Predictor/
│
├── Laptop_Price_Prdictor.ipynb   # EDA, preprocessing, model training & evaluation
├── app.py                         # Flask web application
├── laptop_data (1).csv            # Raw dataset
├── pipe.pkl                       # Serialized ML pipeline (model + preprocessor)
├── df.pkl                         # Cleaned dataframe used by the app
└── README.md
```

---

## 🧠 ML Pipeline

The notebook (`Laptop_Price_Prdictor.ipynb`) covers:

1. **Exploratory Data Analysis (EDA)** — Distribution of prices, brand analysis, correlation heatmaps
2. **Feature Engineering** — Extracting GPU type, screen resolution, processor generation, etc.
3. **Preprocessing** — `OneHotEncoding` for categoricals, log-transform on target (price) for better distribution
4. **Model Training** — Multiple regressors benchmarked
5. **Model Selection** — Best model serialized into `pipe.pkl` via `pickle`

---

## 🛠️ Tech Stack

| Layer | Tools |
|---|---|
| Language | Python 3.x |
| ML | scikit-learn, NumPy, pandas |
| Visualization | Matplotlib, Seaborn |
| Web Framework | Flask |
| Serialization | Pickle |
| Notebook | Jupyter Notebook |

---

## ⚙️ Setup & Installation

**1. Clone the repository**
```bash
git clone https://github.com/sachdevanakul/Laptop-Price-Predictor.git
cd Laptop-Price-Predictor
```

**2. Install dependencies**
```bash
pip install -r requirements.txt
```

> If `requirements.txt` is not present, install manually:
> ```bash
> pip install flask scikit-learn pandas numpy matplotlib seaborn
> ```

**3. Run the app**
```bash
python app.py
```

**4. Open in browser**
```
http://localhost:5000
```

**Or use the live deployment directly:**
> 🔗 [huggingface.co/spaces/NakulSachdeva/laptop-price-predictor](https://huggingface.co/spaces/NakulSachdeva/laptop-price-predictor)

---

## 📊 Dataset

The model is trained on `laptop_data (1).csv`, which contains real-world laptop listings with the following features:

| Feature | Description |
|---|---|
| Company | Brand (Dell, HP, Lenovo, Apple, etc.) |
| TypeName | Category (Notebook, Gaming, Ultrabook, etc.) |
| Ram | RAM in GB |
| Weight | Laptop weight in kg |
| Price | Target variable (in INR/USD) |
| ScreenResolution | Display resolution and panel type |
| Cpu | Processor model and speed |
| Memory | Storage type and capacity |
| Gpu | Graphics card |
| OpSys | Operating System |

---

## 📈 Model Performance

| Metric | Value |
|---|---|
| R² Score | ~0.88 |
| MAE | Varies by model |

> Exact numbers may vary depending on train/test split and model selected.

---

## 🔮 Future Enhancements

- [x] Deployed on Hugging Face Spaces
- [ ] Web scraping integration to auto-update dataset with latest listings
- [ ] Hyperparameter tuning with GridSearchCV / Optuna
- [ ] XGBoost / LightGBM model experiments
- [ ] Streamlit frontend upgrade for a richer UI
- [ ] Docker containerization for self-hosting
- [ ] REST API endpoint for third-party integrations

---

## 🤝 Contributing

Contributions are welcome!

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/your-feature`
3. Commit your changes: `git commit -m 'Add your feature'`
4. Push to the branch: `git push origin feature/your-feature`
5. Open a Pull Request

---

## 👤 Author

**Nakul Sachdeva**
- GitHub: [@sachdevanakul](https://github.com/sachdevanakul)

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

> ⭐ If you found this useful, consider starring the repo!
