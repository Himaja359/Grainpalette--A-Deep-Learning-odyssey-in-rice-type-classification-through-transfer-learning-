# 🌾Grainpalette -A Deep learning Odyssey -in -rice-type classification -through -transfer-learning

GrainPalette is a deep learning-powered web application that classifies rice grain types using **transfer learning**. It allows users to upload a rice image and instantly receive predictions via a clean and modern web interface built with **Flask**.

---

## 📸 Project Preview

- **Home Page**
- **Prediction Page**
- **Detail Page**

> 🎥 **[Live Demo Video – GrainPalette in Action](#)**  
(*Replace the `#` with your actual video URL*)

---

## 🚀 Features

- 🔍 **Classifies 5 Rice Types**:
  - Basmati  
  - Jasmine  
  - Arborio  
  - Ipsala  
  - Karacadag  
- 🧠 Built using **Transfer Learning** (Keras + TensorFlow)
- 🖼 Upload an image and get **real-time predictions**
- 📊 Displays prediction **confidence scores**
- 💾 Model training and evaluation available in `model.ipynb`

---

## 🧪 Project Development Process

### 📁 1. Dataset Collection & Preparation

- Dataset structure with one folder per rice type:
```
dataset/
├── Basmati/
├── Jasmine/
├── Arborio/
├── Ipsala/
└── Karacadag/
```

- Each folder contains rice grain images captured under similar conditions.
- Used for automatic labeling with tools like `ImageDataGenerator` or `os.walk()`.

### 🧼 2. Data Preprocessing

- All images resized to `224x224` pixels.
- Pixel values normalized (divided by 255.0).
- Dataset split into training and validation sets (80-20 ratio).
- Optional augmentations: rotation, zoom, flipping for better generalization.

### 🧠 3. Model Building Using Transfer Learning

- Pre-trained CNN (like VGG16, MobileNet, etc.) used as base model.
- Top layers customized for 5-class classification.
- Compiled with:
  - `Adam` optimizer
  - `categorical_crossentropy` loss
  - `accuracy` as evaluation metric
- Trained using:
  - `model.fit()`
  - EarlyStopping callback

### 📈 4. Model Evaluation

- Training vs Validation accuracy/loss graphs plotted.
- Classification report generated (precision, recall, F1-score).
- Confusion matrix & sample predictions visualized.

### 💾 5. Model Saving

```python
model.save("rice_model.h5")
```

---

## ⚙ Installation & Run Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/GrainPalette.git
cd GrainPalette
```

### 2. Create Virtual Environment & Install Dependencies

Using conda:
```bash
conda create -n grainpalette python=3.9
conda activate grainpalette
pip install -r requirements.txt
```

Or using pip:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
```

### 3. Run the Flask App

```bash
python app.py
```

## 📁 Project Structure

```
GrainPalette/
├── app.py
├── rice_model.h5
├── model.ipynb
├── templates/
│   ├── index.html
│   ├── predict.html
│   └── result.html
├── static/
│   └── styles.css
├── uploads/
├── requirements.txt
└── README.md
```

---

## 🤝 Contributing

Feel free to fork the repository, create a branch, make improvements, and submit a pull request. All kinds of contributions are welcome!

---

## 📜 License

This project is licensed under the [MIT License](LICENSE).

---

## 👨‍💻 Developed by

**Your Name**  
[GitHub](https://github.com/Himaja359) 
