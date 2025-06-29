# amharic-ecommerce-ner
# Amharic E-commerce NER

Extracting key entities from Amharic Telegram e-commerce messages to power vendor analytics and micro-lending decisions.

## 📌 Project Overview

This project develops a Named Entity Recognition (NER) pipeline fine-tuned on Amharic text from Telegram-based vendors. Entities include:
- 🛍️ Product names
- 💵 Prices
- 📍 Locations
- 🚚 Delivery information
- ☎️ Contact info

Extracted entities are used to compute a **Vendor Lending Score** for micro-loan eligibility.

---

## 🗂 Project Structure

amharic-ecommerce-ner/
├── data/ # Raw + labeled Amharic text from Telegram
├── notebooks/ # Jupyter notebooks for each task
├── scripts/ # Preprocessing, training, scoring
├── outputs/ # Trained models, plots, etc.
├── reports/ # PDF summary and blog
├── README.md
├── requirements.txt
└── .gitignore


---

## 🚀 Key Features

- Fine-tuned transformer models: `xlm-roberta`, `bert-tiny-amharic`, `afroxlmr`
- CoNLL-format labeling and Hugging Face training
- Model interpretability using SHAP & LIME
- Vendor activity analytics and lending scorecard

---

## 🛠️ Installation

```bash
pip install -r requirements.txt
🧪 Run Training

python scripts/train_ner.py
📊 Run Vendor Scorecard

python scripts/scorecard.py
📄 License
This project is open source and available under the MIT License.


---

### ✅ 2. `requirements.txt`

```txt
transformers
datasets
pandas
numpy
scikit-learn
seqeval
matplotlib
shap
lime
jupyter
✅ 3. .gitignore
gitignore

# Byte-compiled / optimized / DLL files
__pycache__/
*.py[cod]
*.so

# Data and models
*.csv
*.pkl
*.pt
*.bin
*.json

# Jupyter notebook checkpoints
.ipynb_checkpoints/

# Virtual environments
.venv/
env/
venv/

# Output
outputs/