# 🚨 Disaster Tweet Classifier 🐦🔥

Ever wondered if that tweet about "a crash in the office" is about an actual disaster or just someone’s Monday morning mood? This app classifies whether a tweet is genuinely about a disaster or just melodrama in 280 characters. 💥😅

Built with 💖 using `XGBoost`, `Sentence Transformers`, and `Streamlit`, this project blends NLP and ML to become a tweet truth detector.

---

## 🧠 What It Does

This project uses semantic text embeddings + location/keyword context to:

✅ Detect real disasters in tweets
✅ Filter noise like jokes, metaphors, or clickbait
✅ Provide a clean, interactive interface to test your own tweets

---

## 📦 Prerequisites

* Python 3.9+
* `pandas`, `numpy`, `scikit-learn`
* `xgboost`
* `sentence-transformers`
* `joblib`
* `streamlit`

Install all dependencies with:

```bash
pip install -r requirements.txt
```

---

## 🛠️ Project Structure

```bash
.
├── app.py                  # Streamlit UI app
├── train_model.py          # Script to train and save the XGBoost model
├── model.joblib            # Saved classifier model
├── encoder.joblib          # One-hot encoder for keywords/locations
├── data/
│   └── disaster_tweets.csv # Dataset used
└── README.md               # This file!
```

---

## 🧭 Workflow

1. 🗃️ **Data Loading** – Load the dataset with tweet text, keyword, and location
2. 🧼 **Preprocessing** – Clean text and encode categorical variables
3. 🧠 **Text Embedding** – Convert tweet text to dense vectors using SentenceTransformer
4. ➕ **Feature Fusion** – Combine text and categorical features
5. 📈 **Model Training** – Train an `XGBoostClassifier` on processed features
6. 💾 **Save Model** – Store the model and encoders for deployment
7. 🌐 **Streamlit App** – Build a frontend where users can test tweets in real time

---

## 🚀 Running the App

Make sure you've trained and saved the model using `train_model.py`.

Then, run the Streamlit app with:

```bash
streamlit run app.py
```

---

## 💡 Example Inputs

* **Text:** "Massive earthquake shakes California!"
* **Keyword:** earthquake
* **Location:** United States

🧙‍♂️ Output: `Disaster Detected ✅` or `Not a Disaster ❌`

---

## 👏 Credits

* Dataset adapted from: [Figure Eight Disaster Tweets](https://www.figure-eight.com/data-for-everyone/)
* Built with 🤖 by \[Your Name or Team Name]
* NLP embeddings from `sentence-transformers` and boosted magic from `xgboost`

---

## 📜 License

MIT License. Feel free to remix and improve!
