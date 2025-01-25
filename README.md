# Transfer Learning and Self Tuning

## Overview
This project implements a simple encoder-decoder model for sentiment classification on the IMDb dataset using a fine-tuned BERT model. The model leverages transfer learning, allowing for efficient training on text classification tasks with minimal labeled data. Custom layers are added to the BERT model to enhance its representation and adapt it to the specific task.

## Features
* **Pretrained BERT Integration**: Utilizes the bert-base-uncased model from Hugging Face's Transformers library.
* **Custom Layers**: Adds a fully connected layer with dropout and ReLU activation for better feature extraction.
* **Efficient Training**: Supports mixed precision (fp16), gradient accumulation, and linear learning rate scheduling.
* **Flexible Data Handling**: Includes tokenization, padding, and truncation for input preprocessing.
* **Trainer API Integration**: Simplifies training and evaluation using Hugging Face's Trainer API.

## Dataset
* The dataset used for training consists IMDB Movie Reviews dataset(loaded via the Hugging Face Datasets library).
* Reviews are tokenized, padded, and truncated to fit the input requirements of BERT. The dataset is shuffled for robust training.

## Architecture
The model consists of the following components:

**1. Base Model**: Pretrained BERT model (bert-base-uncased) for sequence classification.

**2. Custom Layers**:
* Fully connected layer with 1024 units.
* ReLU activation for non-linearity.
* Dropout for regularization.

**3. Classifier Head**: Final linear layer with two output units for binary classification.

## Contributions
Feel free to fork the repository and submit a pull request for improvements.

## License
This project is licensed under the MIT License.
