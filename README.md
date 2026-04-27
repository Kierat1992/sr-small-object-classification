# SR-Enhanced Small Object Classification

> Improving shape-based classification of small aerial objects using GAN super-resolution and Hu moment descriptors.

## Overview

Small objects in drone imagery (under 32x32 pixels) lose critical shape
information, making classification unreliable. This project investigates
whether GAN-based super-resolution can recover enough geometric detail
to improve classification using classical shape descriptors (Hu moments).

Pipeline: VisDrone crops → Real-ESRGAN 4x upscale → contour extraction
→ Hu moments feature vectors → Random Forest / SVM classifier.

## Key Experiment

Comparison of classification accuracy using Hu moments extracted from:
- **Low-resolution** crops (original small objects)
- **Super-resolved** crops (Real-ESRGAN pretrained)
- **Super-resolved** crops (Real-ESRGAN finetuned on aerial data)

## Tech Stack

| Tool | Purpose |
|------|---------|
| Python 3.12 | Core language |
| OpenCV | Image processing |
| PyTorch | Deep learning framework |
| Real-ESRGAN | GAN-based super-resolution |
| scikit-learn | Classical ML classifiers |
| matplotlib | Data visualization |

## Project Structure

```
sr-small-object-classification/
├── src/                # Source code - processing, training, evaluation
│   └── __init__.py
├── notebooks/          # Jupyter notebooks - EDA, experiments, demos
├── data/               # Dataset files (not tracked by Git)
├── models/             # Saved model weights (not tracked by Git)
├── outputs/            # Generated results, figures, metrics
├── configs/            # Configuration files
├── docs/               # Documentation and architecture diagrams
├── .gitignore
├── README.md
└── requirements.txt
```

## Setup

```bash
git clone https://github.com/Kierat1992/sr-small-object-classification.git
cd sr-small-object-classification
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
```

## Results

> Experiments in progress.

## Dataset

TODO

## References

TODO