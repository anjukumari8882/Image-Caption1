# 🖼️ Image Caption Generation using CLIP (Sentence Transformers)

## 📌 Project Overview

This project demonstrates an **Image Caption Generation / Image-Text Similarity** system using the **CLIP (Contrastive Language–Image Pretraining)** model from the **Sentence Transformers** library.

Instead of training a deep learning model from scratch, this notebook uses a pre-trained CLIP model to compare an input image with multiple text descriptions and predicts the caption that best matches the image based on cosine similarity.

The project showcases how modern Vision-Language models can understand both images and text by converting them into the same embedding space.

---

# 🎯 Objectives

- Load an image using Python.
- Encode both images and text into vector embeddings.
- Calculate similarity scores between the image and candidate captions.
- Display the image.
- Predict the most relevant caption.
- Demonstrate the power of CLIP for zero-shot image understanding.

---

# 🚀 Features

- Image loading using Pillow (PIL)
- Image visualization with Matplotlib
- Text embedding generation
- Image embedding generation
- Similarity score calculation
- Automatic caption prediction
- Zero-shot image understanding
- Easy to modify with your own images and captions
- Uses a state-of-the-art pre-trained CLIP model

---

# 🛠️ Technologies Used

- Python
- Sentence Transformers
- CLIP (ViT-B-32)
- NumPy
- Pillow (PIL)
- Matplotlib
- Google Colab / Jupyter Notebook

---

# 📚 Libraries Used

```python
sentence-transformers
numpy
matplotlib
Pillow
```

---

# 📂 Project Structure

```
Image-Caption/
│
├── Image_Caption.ipynb
├── README.md
├── images/
│   ├── 5.avif
│   ├── 6.avif
│   ├── 7.avif
│   └── 8.jpg
└── requirements.txt
```

---

# ⚙️ Installation

Clone the repository

```bash
git clone https://github.com/your-username/Image-Caption.git
```

Move into the project folder

```bash
cd Image-Caption
```

Install the required packages

```bash
pip install sentence-transformers
pip install pillow
pip install matplotlib
pip install numpy
```

Or install everything using

```bash
pip install -r requirements.txt
```

---

# ▶️ How It Works

### Step 1

Load the CLIP model

```python
model = SentenceTransformer("clip-ViT-B-32")
```

---

### Step 2

Load an image

```python
img = Image.open(image_path)
```

---

### Step 3

Create multiple candidate captions

Example:

```python
[
"Cute puppy",
"A cat on a table",
"Mountain Hill View",
"Sunset View",
"A dog sleeping on a couch"
]
```

---

### Step 4

Convert image and text into embeddings

```python
text_embeddings = model.encode(text_description)

image_embedding = model.encode(image)
```

---

### Step 5

Calculate similarity

```python
np.dot(text_embeddings, image_embedding)
```

---

### Step 6

Find the highest similarity score

The caption with the highest similarity score is selected as the predicted caption.

---

# 📊 Sample Output

Input Image

```
🐶 Dog Image
```

Candidate Captions

```
Cute puppy
A cat on a table
Mountain Hill View
Sunset View
Dog sleeping on a couch
```

Prediction

```
✅ Cute puppy
```

---

# 🧠 Model Used

### CLIP (Contrastive Language–Image Pretraining)

Model Name

```
clip-ViT-B-32
```

Provided by

```
Sentence Transformers
```

CLIP is a multimodal deep learning model developed to understand both images and text in a shared semantic space.

---

# 📈 Applications

- Automatic Image Captioning
- Image Search
- Content Recommendation
- Image Classification
- Image Retrieval
- AI-powered Photo Organization
- Visual Search Engines
- E-commerce Product Search
- Social Media Content Analysis

---

# 📸 Images Tested

The notebook demonstrates predictions using multiple images such as:

- Dog Image
- Nature View
- Sunset Scene
- Moon Image

Each image is compared against multiple candidate captions.

---

# 🔄 Workflow

```
Input Image
      │
      ▼
Load CLIP Model
      │
      ▼
Generate Image Embedding
      │
      ▼
Generate Text Embeddings
      │
      ▼
Calculate Similarity Scores
      │
      ▼
Select Highest Score
      │
      ▼
Display Predicted Caption
```

---

# 📌 Advantages

- No training required
- Fast inference
- Uses powerful pre-trained model
- High-quality semantic understanding
- Supports zero-shot predictions
- Easy to extend
- Beginner-friendly implementation

---

# ⚠️ Limitations

- Works only with the provided candidate captions.
- Does not generate completely new captions.
- Prediction quality depends on the quality of candidate text descriptions.
- Large models require more memory.

---

# 🔮 Future Improvements

- Generate captions automatically using BLIP.
- Build a Streamlit web application.
- Create a Flask or FastAPI REST API.
- Upload images directly from the browser.
- Support batch image captioning.
- Add multilingual caption generation.
- Improve prediction accuracy using larger CLIP models.
- Deploy on Hugging Face Spaces.

---
