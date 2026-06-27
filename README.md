# 🎓 Student Exam Performance Predictor

An end-to-end Machine Learning web application that predicts a student's **Math exam score** based on demographic and academic features. Built with **Flask** and **Scikit-learn**, featuring a modern, responsive UI.

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Flask](https://img.shields.io/badge/Flask-2.0+-green.svg)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-Latest-orange.svg)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)

---

## ✨ Features

- 🔮 **AI-Powered Predictions** — Predicts math scores using a trained ML pipeline
- 🎨 **Modern UI** — Clean, responsive design with gradient themes
- ⚡ **Fast & Lightweight** — Instant predictions with no data storage
- 📱 **Mobile Friendly** — Works seamlessly on all devices
- 🧪 **End-to-End Pipeline** — Complete ML workflow from data ingestion to deployment

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| **Backend** | Python, Flask |
| **ML / Data** | Scikit-learn, Pandas, NumPy |
| **Frontend** | HTML5 |
| **Model** | Custom PredictPipeline with StandardScaler |

---

## 📁 Project Structure

```
end-to-end-project/
│
├── app.py                          # Flask application entry point
├── requirements.txt                # Python dependencies
│
├── templates/
│   ├── index.html                  # Landing page (Home)
│   └── home.html                   # Prediction form page (/predictdata)
│
├── src/
│   ├── __init__.py
│   ├── components/                 # Data ingestion, transformation, model training
│   ├── pipeline/
│   │   ├── predict_pipeline.py     # CustomData + PredictPipeline classes
│   │   └── train_pipeline.py       # Training pipeline
│   └── utils.py                    # Helper utilities
│
├── artifacts/                      # Saved models, preprocessors, datasets
│   ├── model.pkl
│   └── preprocessor.pkl
│
├── notebook/                       # EDA & model experimentation
│   └── EDA.ipynb
│
└── README.md                       # You are here!
```

---

## 🚀 Getting Started

### Prerequisites

- Python 3.8 or higher
- pip (Python package manager)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/ruidaspradyut-code/end-to-end-project-.git
   cd end-to-end-project-
   ```

2. **Create a virtual environment (optional but recommended)**
   ```bash
   python -m venv venv

   # On Windows
   venv\Scripts\activate

   # On macOS/Linux
   source venv/bin/activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the application**
   ```bash
   python app.py
   ```

5. **Open your browser**
   ```
   http://localhost:5000
   ```

---

## 📖 Usage

### Landing Page (`/`)
The home page provides an overview of the application with a call-to-action to start predicting.

### Prediction Page (`/predictdata`)
Fill in the student details:

| Field | Description | Type |
|-------|-------------|------|
| **Gender** | Student's gender | Select: Male / Female |
| **Race or Ethnicity** | Ethnic group classification | Select: Group A – E |
| **Parental Education** | Highest education level of parents | Select: High School to Master's |
| **Lunch Type** | School lunch program | Select: Standard / Free-Reduced |
| **Test Prep Course** | Completion status of test prep | Select: None / Completed |
| **Reading Score** | Reading exam score (0–100) | Number |
| **Writing Score** | Writing exam score (0–100) | Number |

Click **"Predict Math Score"** and the model will return the predicted math score instantly!

---

## 🔌 API Endpoints

| Route | Method | Description |
|-------|--------|-------------|
| `/` | `GET` | Landing page |
| `/predictdata` | `GET` | Renders the prediction form |
| `/predictdata` | `POST` | Submits form data and returns prediction |

### Example POST Request
```bash
curl -X POST http://localhost:5000/predictdata \
  -d "gender=male" \
  -d "ethnicity=group+C" \
  -d "parental_level_of_education=bachelor's+degree" \
  -d "lunch=standard" \
  -d "test_preparation_course=completed" \
  -d "reading_score=75" \
  -d "writing_score=80"
```

---

## 🤖 Model Details

- **Algorithm**: Custom ML Pipeline with preprocessing and regression
- **Preprocessing**: StandardScaler for numerical features
- **Features Used**: Gender, Ethnicity, Parental Education, Lunch Type, Test Prep, Reading Score, Writing Score
- **Target Variable**: Math Score (0–100)
- **Pipeline**: `src/pipeline/predict_pipeline.py`

---

## 🖼️ Screenshots

| Landing Page | Prediction Form |
|:------------:|:---------------:|
| *Home page with hero section* | *Clean prediction form with result card* |

---

## 📝 To-Do / Future Improvements

- [ ] Add data visualization dashboard
- [ ] Implement user authentication
- [ ] Deploy to cloud (AWS / Heroku / Render)
- [ ] Add model performance metrics page
- [ ] Support batch predictions via CSV upload

---

## 🤝 Contributing

Contributions are welcome! Feel free to open issues or submit pull requests.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the **MIT License**.

---

## 🙏 Acknowledgments

- [Scikit-learn](https://scikit-learn.org/) for the ML toolkit
- [Flask](https://flask.palletsprojects.com/) for the lightweight web framework
- Student Performance Dataset for providing the training data

---

<p align="center">Built with ❤️ by <a href="https://github.com/ruidaspradyut-code">@ruidaspradyut-code</a></p>
