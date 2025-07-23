# 🧬 Blood Group Prediction Using Fingerprint

This project aims to predict a person's **blood group** using their **fingerprint image**. It uses image preprocessing and machine learning (Random Forest classifier) to analyze fingerprint patterns and associate them with known blood group data.

---

## 📁 Project Structure

blood-group-prediction-fingerprint/
├── data/                         # Dataset (fingerprint images)
├── models/                       # Trained model saved here
├── src/                          # Source code (training, prediction, preprocessing)
│   ├── preprocess.py
│   ├── train.py
│   └── predict.py
├── app.py                        # Optional Flask app (for UI)
├── requirements.txt              # Python dependencies
├── .gitignore                    # Files to ignore in Git
└── README.md                     # This file
\`\`\`

---

## 🔧 Requirements

- Python 3.7+
- OpenCV
- NumPy
- scikit-learn
- Flask (for web app)

Install dependencies with:

\`\`\`bash
pip install -r requirements.txt
\`\`\`

---

## 📊 Dataset Format

Fingerprint images should be stored in the \`data/\` folder and named using this format:

\`\`\`
<BLOODGROUP>_<id>.jpg
\`\`\`

**Example:**
- \`A_positive_01.jpg\`
- \`O_negative_14.jpg\`

---

## 🚀 How to Run

### 1. Train the Model

\`\`\`bash
python src/train.py
\`\`\`

This loads fingerprint images from the \`data/\` directory, extracts features, trains a Random Forest model, and saves it to \`models/fingerprint_model.pkl\`.

---

### 2. Predict Blood Group for a New Fingerprint

\`\`\`bash
python src/predict.py
\`\`\`

Or import and use in Python:

\`\`\`python
from predict import predict_blood_group
print(predict_blood_group("data/sample_fingerprint.jpg"))
\`\`\`

---

### 3. Run Flask Web App (Optional)

\`\`\`bash
python app.py
\`\`\`

Then open your browser at: [http://localhost:5000](http://localhost:5000)

Upload a fingerprint image to get a predicted blood group.

---

## 🧠 Model Used

- **Random Forest Classifier**
- Input: Preprocessed grayscale fingerprint image (resized and flattened)
- Output: Predicted blood group class (A+, B−, O+, etc.)

---

## 📌 Future Improvements

- Use deep learning (e.g., CNN) for better accuracy
- Collect and augment more diverse fingerprint datasets
- Build a mobile app for live predictions
- Add blood group confidence scores

---

## 📜 License

This project is licensed under the MIT License. Feel free to use, modify, and share.

---

## 👤 Author

**Janma K Gowda**  
GitHub: [@janmaaa](https://github.com/janmaaa)' > README.md
