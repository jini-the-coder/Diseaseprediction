<h1 align="center">🩺 Disease Prediction from Symptoms</h1>

<p align="center">
  <i>An ML-powered diagnostic assistant that predicts probable diseases from user-reported symptoms — built with Python, scikit-learn, and Tkinter.</i>
</p>

<p align="center">
  <img src="https://img.shields.io/github/stars/jini-the-coder/Diseaseprediction?style=for-the-badge&color=ffd33d" alt="Stars"/>
  <img src="https://img.shields.io/github/forks/jini-the-coder/Diseaseprediction?style=for-the-badge&color=8a63d2" alt="Forks"/>
  <img src="https://img.shields.io/badge/Python-3.7+-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python"/>
  <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white" alt="scikit-learn"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge" alt="License"/>
</p>

---

## 📌 Overview

Classical diagnosis requires patients to visit a doctor and undergo multiple medical tests before reaching a conclusion — a slow and often expensive first step. **Disease Prediction** is a lightweight desktop application that streamlines this initial triage: a user selects up to **5 symptoms** from a curated list, and the app returns the **most probable disease** based on a trained machine-learning model.

The app is built as a self-contained Python script with a Tkinter GUI and a Multinomial Naive Bayes classifier trained on a structured symptoms-to-diseases dataset.

> ⚠️ **Disclaimer:** This is an academic project intended for learning and demonstration purposes only. It is **not** a substitute for professional medical advice or diagnosis.

---

## ✨ Features

- 🧠 **Multinomial Naive Bayes** classifier — well-suited for multi-symptom categorical input
- 🩻 **132 unique symptoms** mapped to **41 possible diseases**
- 🖱️ **Simple Tkinter GUI** — select up to 5 symptoms from dropdowns and click **Predict**
- 📊 Separate **training** and **testing** CSV datasets for reproducible evaluation
- 📈 Built-in **accuracy reporting** against the test set on each prediction
- 💡 Validates user input — prompts when no symptoms have been selected

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Language | Python 3.7+ |
| ML | scikit-learn (`MultinomialNB`) |
| Data | pandas, NumPy |
| GUI | Tkinter |
| Dataset | Custom CSV (Training.csv / Testing.csv) |

---

## 🚀 Getting Started

### Prerequisites

- Python 3.7 or newer
- `pip` for installing dependencies

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/jini-the-coder/Diseaseprediction.git
cd Diseaseprediction

# 2. Install dependencies
pip install numpy pandas scikit-learn

# Tkinter is included with most Python installations.
# On Debian/Ubuntu, install it separately if needed:
# sudo apt install python3-tk
```

### Run the App

```bash
python disease_prediction.py
```

A desktop window will open. Select up to 5 symptoms from the dropdowns and click **Predict** to see the most probable disease.

---

## 🧠 How It Works

1. **Data loading** — `Training.csv` and `Testing.csv` are loaded with pandas. Each row represents a disease and its associated symptom vector (binary: 1 = present, 0 = absent).
2. **Label encoding** — Disease names are mapped to integer labels (0–40) for the classifier.
3. **Feature vector** — When the user picks symptoms in the GUI, those symptoms are flipped to `1` in a 132-length feature vector; everything else stays `0`.
4. **Prediction** — `MultinomialNB.fit(X, y)` trains on the dataset; `.predict()` returns the most likely disease index, which is mapped back to a human-readable name.
5. **Accuracy** — The model is evaluated against `Testing.csv` and the accuracy is printed to the console on every run.

---

## 📁 Project Structure

```
Diseaseprediction/
├── disease_prediction.py   # Main app: Tkinter GUI + ML pipeline
├── Training.csv            # Training dataset (symptom-disease mappings)
├── Testing.csv             # Test dataset for evaluation
└── README.md
```

---

## 🏆 Recognition

This project served as the foundation for an academic submission and showcases applied machine learning for healthcare-related triage — earning recognition in undergraduate project showcases.

---

## 🛣️ Roadmap & Ideas

Open to contributions and ideas! Some directions this project could grow in:

- 🌐 Web-based version using Flask / FastAPI + React
- 🔬 Compare classifiers (Random Forest, Decision Tree, KNN) to benchmark accuracy
- 📱 Mobile-friendly UI
- 🧪 Increase symptom support beyond 5
- 📦 Package as a standalone executable

---

## 🤝 Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you'd like to change.

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/awesome-thing`)
3. Commit your changes (`git commit -m 'Add awesome thing'`)
4. Push to the branch (`git push origin feature/awesome-thing`)
5. Open a Pull Request

---

## 📜 License

This project is licensed under the **MIT License** — feel free to use, fork, and adapt with attribution.

---

## 👋 About the Author

Built with ❤️ by **Jinisha Gangadharan** — Senior AI Frontend Specialist passionate about the intersection of AI, engineering, and great user experiences.

<p>
  <a href="https://www.linkedin.com/in/jinisha-kg-3b0783188">
    <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/>
  </a>
  <a href="mailto:jinishakg11@gmail.com">
    <img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"/>
  </a>
  <a href="https://github.com/jini-the-coder">
    <img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white" alt="GitHub"/>
  </a>
</p>

<p align="center"><i>If this project helped you, please consider giving it a ⭐!</i></p>
