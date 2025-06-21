Here’s the **refined and professionally edited README file**, including the updated project structure with the folder `gait_recognition_using_samples_ofDifferentLength/`:

---

# 🧠 Hybrid CNN-LSTM Gait Recognition Model with SE Block

This project introduces a hybrid deep learning architecture for **gait recognition** using wearable sensor data. The model integrates two parallel branches:

* 🔁 **LSTM Branch**: Captures **temporal dependencies** from time-series data.
* 🧩 **CNN Branch**: Extracts **spatial features** from each time step via convolutional layers.

A **Squeeze-and-Excitation (SE) block** is embedded in the CNN branch to dynamically recalibrate channel-wise feature maps, helping the model focus on **important spatial channels**.

---

## 💡 Motivation

* **LSTM** captures the sequential nature of gait signals.
* **CNN** extracts meaningful local patterns from the data.
* **SE Block** improves CNN focus by emphasizing informative channels.

By combining these components, the model leverages both **temporal and spatial representations**, enhancing gait recognition performance.

---

## 🏗️ Project Structure

```
gait_recognition_using_samples_ofDifferentLength/
│
├── gait_recognition_using_ou-isir_data.ipynb  # main notebook
│
├── data_preparation.ipynb       # Load data, preprocess, and split into train/test sets
├── se_block.ipynb               # Squeeze-and-Excitation block definition
├── model_branches.ipynb         # CNN and LSTM branch architectures with SE and pooling
├── train_and_evaluate.ipynb     # Model assembly, training, and accuracy plotting
└── README.md                 # Project documentation (this file)
```

---

## 📊 Dataset

* **Source**: `AutomaticExtractionData_IMUZCenter/` (from OU-ISIR)
* **Format**: Each file contains multivariate sensor readings, one row per time step.
* **Labeling**: Person IDs are extracted from filenames for classification.

🛠️ **Note**: Set the correct `csv_directory` path in `train_and_evaluate.py`.

---

## 🧪 Training & Evaluation

To train the model and visualize performance:

```bash
python train_and_evaluate.py
```

This will train the hybrid model and generate an **accuracy plot** comparing training and validation performance.

---

## 📈 Accuracy Visualization

Training includes **real-time accuracy plots** to help identify overfitting or underfitting.

---

## 🔧 Requirements

* Python ≥ 3.8
* TensorFlow
* NumPy
* Matplotlib
* scikit-learn
* pandas

---

## 👩‍💻 Author

**Abeer Saleh**
PhD in Communication Engineering — Specializing in Computer Vision
📍 Dubai, UAE
📫 Contact: \[GitHub Profile] | \[LinkedIn Profile]

---

## 📜 License

This project is intended for academic and research purposes only.
