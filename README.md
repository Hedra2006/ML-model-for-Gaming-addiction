# ML-model-for-Gaming-addiction
# Gaming Addiction Predictor 🎮

A Streamlit web app that predicts whether a person is likely to be addicted to gaming, based on lifestyle, psychological, and gaming behavior features. The model is trained on a gaming addiction dataset using **Logistic Regression**.

## Demo

Fill in the form with your gaming habits and lifestyle data, click **Predict**, and the app will tell you whether the model classifies you as *Addicted* or *Not Addicted*.

## Project Structure

```
gaming_app/
├── app.py                 # Streamlit application
├── requirements.txt        # Python dependencies
├── model.pkl               # Trained Logistic Regression model
├── scaler.pkl               # StandardScaler fitted on training data
├── encoders.pkl             # LabelEncoders for categorical columns
├── feature_columns.pkl      # Ordered list of feature columns
├── cat_columns.pkl          # List of categorical columns
└── num_columns.pkl          # List of numerical columns
```

## How It Works

1. The model was trained on a dataset of gaming habits, lifestyle, and psychological indicators (age, playtime, stress score, sleep hours, etc.).
2. Categorical features are label-encoded and numerical features are standardized using `StandardScaler`.
3. The trained artifacts (model, scaler, encoders) are saved with `joblib` and loaded by the Streamlit app.
4. The app dynamically builds an input form from the saved feature list, so dropdown options always match the categories seen during training.

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/<your-username>/gaming_app.git
cd gaming_app
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Run the app locally

```bash
streamlit run app.py
```

The app will open automatically at `http://localhost:8501`.

## Model Info

| Model | Accuracy |
|---|---|
| Logistic Regression (deployed) | 0.96 |
| SVM (RBF kernel) | 0.96 |
| Decision Tree | 0.94 |
| Random Forest | 0.92 |
| Neural Network | 0.80 |

## Tech Stack

- Python
- scikit-learn
- pandas
- Streamlit
- joblib

## Notes

- The raw dataset (`gaming_addiction.csv`) is **not required** to run the app — only the saved `.pkl` artifacts are needed.
- If you want to retrain the model on new data, re-run the training script and replace the `.pkl` files.

## License

This project is for educational purposes as part of an NTI Machine Learning course.
