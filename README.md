# Shakespeare Text Generator

## Project Overview
The Shakespeare Text Generator is a Python-based project utilizing neural networks to generate text in the style of William Shakespeare. This project leverages TensorFlow, Keras, and Numpy to build and train a model on a subset of Shakespeare's works. The model predicts the next character in a sequence, generating text that mimics Shakespeare's unique style.

## Features
- Text generation using a GRU-based neural network.
- Character-level prediction for generating text.
- Customizable text generation based on input length and temperature parameter.
- Utilizes LSTM and Dense layers from TensorFlow's Keras API.

## Installation
To run this project, ensure that Python is installed on your system. Additionally, the following Python packages are required:
- TensorFlow
- NumPy
- Random

Insall these packages using pip:
```bash
pip install tensorflow numpy
```

## Usage
1. **Training the Model:** The script automatically downloads a subset of Shakespeare's texts and trains the neural network. The model is saved as 'textgenerator.model'.
2. **Generating Text:**
   - Load the trained model (or use the code to train your own model)
   - Use the generate_text function, specifying the desired length of the text and the temperature parameter, which controls the randomness of character generation.
   Example:
   ```python
   print(generate_text(300, 0.2))
   ```

## How it Works
- **Data Preparation:** The text is converted into character-level sequences, which are used to train the model to predict the next character in a sequence.
- **Model Architecture:** The model uses a GRU (Gated Recurrent Unit) layer, followed by a Dense layer with a softmax activation. It's compiled with an RMSprop optimizer.
- **Training:** The model is trained for 10 epochs, but this can be adjusted as needed.
- **Text Generation:** The generate_text function generates text by predicting the next character in a sequence, updating the sequence, and repeating the process.

## Customization
- **Training Data:** Modify the subset of the text used for training by changing the text variable slicing.
- **Model Parameters:** Adjust the GRU layer size, learning rate, batch size, and epochs for different results.
- **Generation Settings:** Change the length and temperature in the generate_text function for varied output.

*Note: The performance and quality of the generated text are highly dependent on the model's training. Longer training with more data may yield more coherent results.*


