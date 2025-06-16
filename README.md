# 🛍️ Smart Purchase Category Recommender

This is an AI-powered web application that recommends product categories to users based on their online shopping behavior. It leverages **contrastive learning** with **SBERT embeddings** to match users to relevant product categories.

---

## 🚀 Live Demo

* 🌐 Streamlit App: [Click to Try](https://purchase-prediction-app-3fqjntw2sygip8mgd7scfa.streamlit.app/)
* 🧪 Google Colab Notebook (for reproduction): [Open in Colab](https://colab.research.google.com/drive/1i4ZGkAK_DpP7_7a8t1VeHtHjm6gAiL0r?usp=sharing)

---

## 📦 Features

* Select a customer from real transaction data
* View behavioral summary
* Get personalized top-N recommended categories
* Uses PyTorch and Sentence-BERT for deep semantic understanding
* Deployed using Streamlit

---

## 📁 Project Structure

```
project/
├── src/
│   ├── app.py                # Streamlit web app
│   ├── train.py              # Model training logic
│   ├── inference.py          # Prediction/inference logic
│   ├── model_utils.py        # Model class and contrastive loss
│   └── preprocess_utils.py   # Feature engineering
├── data/
│   └── Online_Shopping_Data.csv    # Input dataset
├── saved/
│   └── cat_text_vecs.npy     # Category SBERT embeddings
├── model.pth                 # Saved PyTorch model
├── requirements.txt          # Python dependencies
├── PROCESS.md                # Reproduction guide
└── README.md
```

---


## 📊 Dataset

* **Source:** Originally from [Kaggle – Online Shoppers Purchasing Intention Dataset](https://www.kaggle.com/datasets/mkechinov/ecommerce-behavior-data-from-multi-category-store)
* **Access:** The dataset file `Online_Shopping_Data.csv` is included in the `/data` folder.
* **Note:** If you clone the repository and the dataset is missing, please download it manually from the Kaggle link and place it in the correct folder.

---

## 🧠 Model Details

* **Embedding Layer:** Sentence-BERT (pretrained)
* **Learning Objective:** Contrastive Loss for matching user and category embeddings
* **Output:** Top-N category recommendations
* **Reproducibility:** Fixed seeds for all randomness
* **Artifacts:**

  * `model.pth`: Trained PyTorch model
  * `cat_text_vecs.npy`: Category embeddings
  * `user_embeddings.pkl`: Optional intermediate output

---

## 📄 Setup Instructions

### 1. Clone this repository

```bash
git clone https://github.com/HRChiam/purchase-prediction-streamlit.git
cd purchase-prediction-streamlit
```

### 2. Install dependencies

Make sure you're using **Python 3.10+**:

```bash
pip install -r requirements.txt
```

### 3. Run the Streamlit app locally

```bash
streamlit run src/app.py
```

---

## 🔁 Reproducibility

We ensure full reproducibility by:

* Providing a step-by-step guide in `PROCESS.md`
* Saving trained models and embeddings
* Using fixed random seeds:

  * `torch.manual_seed(42)`
  * `np.random.seed(42)`
  * `random.seed(42)`

---

## 🛠️ Tech Stack

* Python, Streamlit, PyTorch
* Sentence-Transformers (SBERT)
* NumPy, Pandas, scikit-learn
* Google Colab for experimentation

---

## 📚 Documentation

* `README.md`: Project overview and setup
* `PROCESS.md`: Reproduction instructions
* In-code documentation via comments

---

## 👨‍💻 Contributors

* Yap Yu Hang
* Tham Wing Shan
* Tan Wei Ren
* Chiam Huai Ren
* Liu YiXian

---

## 📎 References

* Sentence-BERT: [https://www.sbert.net/](https://www.sbert.net/)
* Streamlit Docs: [https://docs.streamlit.io/](https://docs.streamlit.io/)
* Contrastive Learning: [https://arxiv.org/abs/2002.05709](https://arxiv.org/abs/2002.05709)

---


