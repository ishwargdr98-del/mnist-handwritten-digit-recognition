# MNIST Handwritten Digit Recognition

A beginner-friendly neural-network project that classifies handwritten digits from **0 to 9** using TensorFlow/Keras and the MNIST dataset.

## Results
- **Test accuracy:** 97.42%
- **Test loss:** 0.0836
- **Training:** 5 epochs, batch size 32, with 10% of the training data used for validation

These metrics are from the notebook's recorded evaluation output. Results can vary if the model is retrained with different settings or environments.

## Tech Stack
- Python
- TensorFlow / Keras
- NumPy
- Matplotlib

## Dataset
The notebook loads MNIST through `tf.keras.datasets.mnist`. It contains 60,000 training images and 10,000 test images. Each image is a 28×28 grayscale image.

## Workflow
1. Import the required libraries.
2. Load and visualize MNIST images.
3. Normalize pixel values from 0–255 to 0–1.
4. Build a neural network with `Flatten`, `Dense (ReLU)`, `Dropout`, and `Dense (Softmax)` layers.
5. Train for five epochs and validate on a held-out portion of the training data.
6. Evaluate on the test dataset.
7. Plot training progress and inspect predictions.
8. Save the trained model as `mnist_digit_recognition.keras` when the notebook is run.

## Run the Project

### Option 1: Google Colab
1. Open Google Colab.
2. Upload `mnist_digit_recognition.ipynb`.
3. Run the notebook cells from top to bottom.

### Option 2: Local Python environment
Use Python 3.10–3.12 in a virtual environment, then install dependencies:

```bash
python -m venv .venv
```

Windows:
```bash
.venv\Scripts\activate
```

macOS/Linux:
```bash
source .venv/bin/activate
```

Install packages:
```bash
pip install -r requirements.txt
```

Open the notebook:
```bash
jupyter notebook mnist_digit_recognition.ipynb
```

## Model Architecture
- Input: 28×28 grayscale image
- Flatten: converts image pixels into a 784-value vector
- Dense: 128 neurons with ReLU activation
- Dropout: 0.2 to help reduce overfitting
- Output: 10 neurons with Softmax, one per digit class

## What I Learned
- Loading and preparing a dataset
- Normalizing image pixel values
- Building and training a neural network
- Evaluating performance on unseen test data
- Visualizing model performance and predictions
- Saving a trained Keras model

## Future Improvements
- Compare results across different epoch counts and layer sizes
- Add a confusion matrix and per-class metrics
- Experiment with a Convolutional Neural Network (CNN)

## Author
Ishwar Bhardwaj
- GitHub: https://github.com/ishwargdr98-del
