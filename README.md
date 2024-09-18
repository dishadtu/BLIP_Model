# Multimodal Image Captioning System

This project implements a multimodal image captioning system using Python and PyTorch, leveraging the BLIP (Bootstrapping Language-Image Pretraining) model to generate descriptive captions for meme images.

## Table of Contents
- [Installation](#installation)
- [Dataset](#dataset)
- [Usage](#usage)
- [Model Training](#model-training)
- [BLEU Score Evaluation](#bleu-score-evaluation)
- [Results](#results)

## Installation

To set up the project, ensure you have the following packages installed:

- `transformers`
- `torch`
- `torchvision`
- `nltk`

## Dataset

The dataset used for this project consists of meme images and their corresponding captions. The images are stored in a specific directory, and metadata is provided in a JSON file (`mlr_captioning_TEST.json`). The project uses the following fields from the dataset:
- **post_id**: Unique identifier for each post.
- **img_fname**: Filename of the image.
- **img_captions**: Ground truth captions for the images.

## Usage

1. Mount your Google Drive to access the dataset.
2. Load the dataset and preprocess the images.
3. Create a custom dataset class and data loader.
4. Initialize the BLIP model.

## Model Training

The model is trained using the provided meme dataset. It utilizes an Adam optimizer and can leverage GPU acceleration if available. 

To generate captions for the images, you can define a function to handle this process.

## BLEU Score Evaluation

The quality of the generated captions is evaluated using the BLEU score metric, which measures the similarity between the generated captions and the ground truth captions.

## Results

The average BLEU score of the generated captions is computed and displayed. A submission file (`TeamYOLO.csv`) containing the generated captions is created in the required format, sorted by `post_id`.


