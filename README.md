# ISL Fingerspelling Dataset

[![Dataset](https://img.shields.io/badge/Dataset-Hugging%20Face-yellow)](https://huggingface.co/datasets/kirandevraj/ISL-Fingerspelling)
[![Paper](https://img.shields.io/badge/Paper-WSLP%202025-blue)](https://kirandevraj.github.io/ISL-Fingerspelling)
[![License](https://img.shields.io/badge/License-CC%20BY--NC%204.0-green)](https://creativecommons.org/licenses/by-nc/4.0/)

> **Continuous Fingerspelling Dataset for Indian Sign Language**
> WSLP @ AACL-IJCNLP 2025

**[Project Page](https://kirandevraj.github.io/ISL-Fingerspelling)** | **[Dataset (Hugging Face)](https://huggingface.co/datasets/kirandevraj/ISL-Fingerspelling)** | **[Paper (Coming Soon)](#)**

---

## Overview

The first continuous fingerspelling dataset for Indian Sign Language (ISL), extracted from ISH News YouTube videos. The dataset comprises **1,308 segments** from **499 videos**, totaling **70.85 minutes** and **14,814 characters**, capturing authentic coarticulation patterns in naturalistic signing contexts.

### Key Features

- First continuous ISL fingerspelling dataset (previous datasets only provide static images)
- 1,308 video segments with aligned text annotations
- 3 professional signers from ISH News
- 90.67% annotation accuracy validated by ISL interpreter
- Baseline results: 82.91% CER with ByT5-small model

### Statistics

| Segments | Duration | Characters | Videos | Signers |
|----------|----------|------------|--------|---------|
| 1,308 | 70.85 min | 14,814 | 499 | 3 |

## Dataset Structure

```
ISL-Fingerspelling/
├── videos/              # 1,308 MP4 video files
├── train_ytsl25.csv     # Training split (1,104 segments)
├── test_ytsl25.csv      # Test split (204 segments)
└── README.md
```

## Quick Start

### Download from Hugging Face

```python
from datasets import load_dataset

# Load the dataset
dataset = load_dataset("kirandevraj/ISL-Fingerspelling")

# Access splits
train_data = dataset['train']
test_data = dataset['test']
```

### Clone Repository

```bash
git clone https://huggingface.co/datasets/kirandevraj/ISL-Fingerspelling
```

## Baseline Results

| Model | Pre-training | Fine-tuning | Test CER (%) |
|-------|-------------|-------------|--------------|
| ByT5-small | iSign | None | 432.44 |
| ByT5-small | iSign | ISL Fingerspelling | **82.91** |

Fine-tuning on fingerspelling data achieves an 80.8% relative reduction in error rate, demonstrating the necessity of domain-specific adaptation.

## Supported Tasks

1. **Transcription**: Convert continuous fingerspelling videos into character sequences
2. **Temporal Localization**: Identify fingerspelling boundaries in longer videos
3. **Generation**: Produce signing videos from text with realistic handshapes

## Citation

```bibtex
@inproceedings{kirandevraj2025islfingerspelling,
  title={Continuous Fingerspelling Dataset for Indian Sign Language},
  author={Kirandevraj, R and Kurmi, Vinod K and Namboodiri, Vinay P and Jawahar, CV},
  booktitle={Proceedings of the Workshop on Sign Language Processing (WSLP) at AACL-IJCNLP},
  year={2025}
}
```

## Authors

- **R Kirandevraj** (IIIT Hyderabad) - kirandevraj.r@research.iiit.ac.in
- **Vinod K Kurmi** (IISER Bhopal)
- **Vinay P Namboodiri** (University of Bath)
- **CV Jawahar** (IIIT Hyderabad)

## License

This dataset is released under [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/) for research purposes only.

## Acknowledgments

Data sourced from publicly available ISH News YouTube videos. 407 of 499 videos overlap with the iSign dataset (which obtained ISH News permission for research use).

---

For more details, visit the [project page](https://kirandevraj.github.io/ISL-Fingerspelling).
