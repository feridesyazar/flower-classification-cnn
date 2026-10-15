# 🌸 Flower Classification with Deep Learning

A computer vision project that classifies flower photographs into **14 categories** using **MobileNetV2** and CNN-based transfer learning. The notebook covers image exploration, preprocessing, model training, and evaluation.

## 📊 Dataset

- **14 flower classes**
- **13,642 training records** and **98 original validation records**
- CSV files contain image paths and class labels; the JPG image folders are required to run the notebook.

Classes include Carnation, Iris, Bellflower, Golden Trumpet, Rose, Astilbe, Tulip, Marigold, Dandelion, Coreopsis, Black-eyed Susan, Water Lily, Sunflower, and Daisy.

## 🛠️ Technologies

Python · Pandas · NumPy · Matplotlib · TensorFlow / Keras · Scikit-learn · Pillow

## 🤖 Approach

- Explore class distribution and sample flower images.
- Resize images to **160 × 160** and apply light data augmentation.
- Use a **frozen, ImageNet-pretrained MobileNetV2** with a classification head.
- Train on **2,800 images** for up to **5 epochs** to keep resource usage manageable.
- Evaluate on a separate, stratified **2,047-image test set**.

## 📈 Results

| Metric | Test result |
|---|---:|
| Accuracy | **87.4%** |
| Macro F1-score | **0.87** |
| Test images | **2,047** |

Results are from a limited training experiment, not a production-ready classifier. The original validation set is small (98 images).

## 🚀 Run the Notebook

Install the dependencies:

```bash
pip install -r requirements.txt
```

Place `train.csv`, `val.csv`, `classname.txt`, and their matching `train/` and `val/` JPG folders alongside `Flower_Classification_CNN.ipynb`. Open the notebook in Jupyter or VS Code and run the cells in order.

The trained model is saved as `models/flower_classifier.keras` for potential future use in a Streamlit app. MobileNetV2 pretrained weights may be downloaded on first run.

## 🔮 Future Improvements

- Train with more images and evaluate on a larger external validation set.
- Build an interactive Streamlit flower classifier.
