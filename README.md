# 🎵 Spotify Analytics Project

A complete data analytics and machine learning project exploring how audio features of songs influence their popularity on Spotify. This project covers the entire pipeline from data cleaning to model building using real-world music metadata.

---

## 📌 Project Objective

The goal of this project is to analyze and model Spotify track data to identify which features are most associated with popularity. Using classification models, we attempt to predict whether a song is "popular" based on its characteristics like energy, danceability, acousticness, etc.

---

## 🔍 Key Highlights

- ✅ Cleaned real-world Spotify data (duplicates, missing values, standardization)
- ✅ Performed exploratory data analysis (EDA) with interactive and static plots
- ✅ Trained machine learning models to classify tracks as popular or not
- ✅ Compared model performance using accuracy, F1 score, and ROC-AUC
- ✅ Structured project for clarity and reusability

---

## 🧹 Data Cleaning (`scripts/cleaning_script.py`)

The original dataset had:
- Duplicate tracks (same track ID, different popularity scores)
- Missing values in essential columns
- Inconsistent text formatting

**Cleaning steps included:**
- Keeping only the most popular version of duplicate tracks
- Removing rows with missing values in `track_name`, `artists`, or `popularity`
- Standardizing text columns (lowercase, whitespace trimming)

🟢 Output file: `data/Spotify_Cleaned.csv`

---

## 📊 Exploratory Data Analysis (`notebooks/2_EDA_Process.ipynb`)

EDA was conducted using Seaborn, Matplotlib, and Plotly.

**Key insights explored:**
- Distribution of popularity scores
- Correlation heatmap of all numerical audio features
- Most common genres and popular artists
- Trends in duration, energy, danceability, and more

📈 Optional visualizations can be added to the `images/` folder.

---

## 🤖 Machine Learning Models (`notebooks/3_Modeling_Code.ipynb`)

We performed binary classification where:
- Songs with popularity above a threshold (e.g., 70) = **Popular**
- Others = **Not Popular**

### 🔧 Models Used:
- Logistic Regression (CV)
- Random Forest Classifier
- XGBoost Classifier
- Dummy Classifier (baseline)

### 🧪 Evaluation Metrics:
- Accuracy Score
- F1 Score
- Confusion Matrix
- ROC-AUC Curve

🧠 Feature importance was analyzed to understand which audio features matter most.

---

## 🗂️ Project Structure

Spotify-Analytics-Project/
├── data/
│   └── Spotify_Cleaned.csv
├── notebooks/
│   ├── 2_EDA_Process.ipynb
│   └── 3_Modeling_Code.ipynb
├── scripts/
│   └── cleaning_script.py
├── requirements.txt
├── LICENSE
└── README.md

## 🛠️ Requirements

To run this project, install the dependencies listed in `requirements.txt`:

```bash
pip install -r requirements.txt

Libraries used:

pandas, numpy

matplotlib, seaborn, plotly

scikit-learn, xgboost


---

### 🔹 Section 9: Author & Contact

```markdown
## 👩‍💻 Author

**Kajal Singh**  
Data Analytics Student @ Douglas College  
📍 Vancouver, Canada  
📧 kajalsingh.1303@gmail.com  
🔗 [kajalsingh3010](https://www.linkedin.com/in/kajalsingh3010)

## 📝 License

This project is licensed under the MIT License — see the `LICENSE` file for details.

> “Turn data into direction, and insights into impact.”
