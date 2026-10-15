# MNIST Handwritten Digit Classifier

This project trains a Keras neural network to recognize handwritten digits (0–9) from the MNIST dataset. The notebook prepares the image data, trains and evaluates a fully connected model, visualizes its results, and lets you select a digit image from your computer for prediction.

## Run the notebook

1. Install Python 3.12.
2. Create and activate a virtual environment:

   ```powershell
   py -3.12 -m venv .venv
   .\.venv\Scripts\Activate.ps1
   ```

3. Install dependencies:

   ```powershell
   python -m pip install -r requirements.txt
   ```

4. Open `mnist.ipynb` in VS Code, select the `.venv` Python kernel, and run the notebook from top to bottom.

The MNIST dataset downloads through Keras the first time the data-loading cell runs. After training, run the final section to choose an image with one clearly visible handwritten digit.

## Model overview

Each 28 × 28 grayscale image is flattened into 784 pixel values. The model uses two hidden layers of 128 neurons, dropout, and a 10-class softmax output. Its final notebook cells evaluate test-set performance and inspect misclassified examples.

Predictions on personal images are best-effort: the model was trained on MNIST-style images, so clear, centered, high-contrast digits work best.
