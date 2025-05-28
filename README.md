# 🐶 Dog Breed Classification 

This project focuses on classifying dog breeds from images using TensorFlow and TensorFlow Hub. It uses transfer learning and a pretrained image feature extractor to identify 120 different dog breeds from the Stanford Dogs dataset (Kaggle's Dog Breed Identification challenge).

## 📂 Dataset

The dataset includes:
- `train/`: Images of dogs for training
- `test/`: Images for final testing
- `labels.csv`: Mapping of image IDs to breed labels

You can find and unzip the dataset into your working directory. The dataset used is available on [Kaggle](https://www.kaggle.com/c/dog-breed-identification/data).

## 🚀 Project Workflow

### 1. 📥 Data Preparation
- Load image filenames and corresponding breed labels.
- Check for data integrity and consistency.
- Visualize label distribution using bar plots.

### 2. 🧼 Data Preprocessing
- Define preprocessing functions to:
  - Read and decode image files.
  - Convert to float tensors and resize to 224x224 pixels.
- Create batched datasets using `tf.data.Dataset` for training and validation.

### 3. 🧠 Model Building
- Use a pretrained model from TensorFlow Hub (e.g., `mobilenet_v2`, `efficientnet`, etc.).
- Add a classification layer with 120 output nodes (softmax activation).
- Compile the model with:
  - Loss: `CategoricalCrossentropy`
  - Optimizer: `Adam`
  - Metrics: `accuracy`

### 4. 🏋️ Model Training
- Train using batched datasets.
- Include callbacks like:
  - TensorBoard logging
  - Early stopping for performance monitoring

### 5. 📈 Evaluation & Prediction
- Evaluate model performance on validation data.
- Visualize:
  - Predictions vs. Actual labels
  - Prediction confidence

### 6. 💾 Saving and Loading the Model
- Save the trained model (`.h5` format).
- Load the saved model using TensorFlow Hub-compatible loading.

### 7. 🔎 Final Testing
- Load test image filenames.
- Preprocess and run predictions on test data.

## 📊 Visualizations

### 🐕 Distribution of Dog Breeds
A horizontal bar chart showing the number of images available for each dog breed in the dataset.

## 📬 Contact

For any queries or suggestions, feel free to reach out:

- 📧 Email: [abineshbalasubramaniyam@example.com](mailto:abineshbalasubramaniyam@example.com)
- 💼 LinkedIn: [linkedin.com/in/abinesh-b-1b14a1290/](https://www.linkedin.com/in/abinesh-b-1b14a1290/)
