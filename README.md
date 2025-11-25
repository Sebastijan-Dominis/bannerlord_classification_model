# Bannerlord Troop Classification

This repository contains a dataset and an experiment notebook for a convolutional classification model trained to recognize six basic troop types from Mount & Blade II: Bannerlord. The project was completed as part of the "Neural Networks and Deep Learning" course at the Faculty of Informatics Pula. The dataset was collected and labeled by the project author.

## Table of Contents
- [What you'll find here](#what-youll-find-here)
- [Dataset Structure](#dataset-structure)
- [Installation](#installation)
- [License](#license--data-notes)
- [Author & Contact](#author--contact)

## What you'll find here
- `Bannerlord.ipynb`: Jupyter notebook with the experimental code for data loading, training, validation, and basic evaluation/visualizations.
- `Dataset/`: image dataset split into `training/`, `validation/`, and `test/` folders. Each split contains class subfolders.
- `Documentation.pdf`: additional notes and documentation produced for the project.

## Dataset structure
The repo follows a standard image-classification layout:

```
Dataset/
	training/
		Aserai Recruit/
		Battanian Volunteer/
		Imperial Recruit/
		Khuzait Nomad/
		Sturgian Recruit/
		Vlandian Recruit/
	validation/
		(same class subfolders)
	test/
		(same class subfolders)
```

Each class folder holds images for that troop type. This structure is compatible with common PyTorch `ImageFolder` and TensorFlow `image_dataset_from_directory` utilities.

## Installation

1. Clone the repository

```bash
git clone https://github.com/Sebastijan-Dominis/bannerlord_classification_model
cd bannerlord_classification_model
```

2. Create and activate a virtual environment:

If using Anaconda:
```bash
conda create -n "bannerlord_classification_model" python=3.11
conda activate bannerlord_classification_model
```

3. Install the project's dependencies from `requirements.txt`:

```bash
pip install -r requirements.txt
```

4. Use the provided Jupyter notebook:

> The notebook contains the code to load the images from `Dataset/`, define a model, train, and evaluate.

## License & data notes

- The dataset was collected by the repository author for educational purposes. Redistribution and reuse are subject to the terms of the MIT License.
- See the `LICENSE` file for the full text.

## Author & Contact

- Author: Sebastijan Dominis
- Contact: sebastijan.dominis99@gmail.com