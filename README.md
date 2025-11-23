# Bannerlord Troop Classification

This repository contains a dataset and an experiment notebook for a convolutional classification model trained to recognize six basic troop types from Mount & Blade II: Bannerlord. The project was completed as part of the "Neural Networks and Deep Learning" course at the Faculty of Informatics Pula. The dataset was collected and labeled by the project author.

**What you'll find here**
- `Bannerlord1.2.ipynb`: Jupyter notebook with the experimental code for data loading, training, validation, and basic evaluation/visualizations.
- `Dataset/`: image dataset split into `training/`, `validation/`, and `test/` folders. Each split contains class subfolders.
- `Documentation.pdf`: additional notes and documentation produced for the project.

**Dataset structure**
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

**Quickstart — dependencies & run (Windows PowerShell)**
1. Create and activate a virtual environment:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

2. Install the project's dependencies from `requirements.txt`:

```powershell
pip install --upgrade pip
pip install -r requirements.txt
```

3. Start the notebook server and open the experiment:

```powershell
jupyter notebook Bannerlord1.2.ipynb
```

Note: The notebook contains the code to load the images from `Dataset/`, define a model, train, and evaluate. Open it and run cells in order.

**How the notebook is organized**
- Data loading and augmentation: reads `Dataset/` and prepares training/validation/test pipelines.
- Model definition: lightweight convolutional model used for experiments (can be swapped for larger architectures).
- Training loop and checkpoints: trains the model and saves best weights.
- Evaluation and visualization: shows accuracy, confusion matrix, and sample predictions.

**License & data notes**
- This repository is licensed under the MIT License — see the `LICENSE` file for the full text.
- The dataset was collected by the repository author for educational purposes. Redistribution and reuse are subject to the terms of the MIT License

**Contact / citation**
If you use or extend this project, please acknowledge the author (see repository metadata) where appropriate.
