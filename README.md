# ISL Fingerspelling Dataset

[![Dataset](https://img.shields.io/badge/Dataset-Hugging%20Face-yellow)](https://huggingface.co/datasets/kirandevraj/ISL-Fingerspelling)
[![Paper](https://img.shields.io/badge/Paper-WSLP%202025-blue)](https://kirandevraj.github.io/ISL-Fingerspelling)
[![License](https://img.shields.io/badge/License-CC%20BY--NC%204.0-green)](https://creativecommons.org/licenses/by-nc/4.0/)

> **Continuous Fingerspelling Dataset for Indian Sign Language**
> WSLP @ AACL-IJCNLP 2025

**[Project Page](https://kirandevraj.github.io/ISL-Fingerspelling)** | **[Dataset (Hugging Face)](https://huggingface.co/datasets/kirandevraj/ISL-Fingerspelling)**

---

## Overview

We introduce the continuous fingerspelling dataset for Indian Sign Language, comprising 1,308 video segments with aligned text annotations. The dataset captures authentic coarticulation patterns from professional signers, supporting research in fingerspelling recognition and sign language processing.

## Statistics

| Segments | Duration | Characters | Videos | Signers | Validation Acc. |
|----------|----------|------------|--------|---------|-----------------|
| 1,308 | 70 min | 14,814 | 499 | 3 | 90.67% |

## Dataset Structure

```
ISL-Fingerspelling/
├── videos/              # 1,308 MP4 video files
├── annotations.csv      # Annotations with video IDs and text
└── README.md
```

### CSV Format

The annotations.csv file contains:
- `uid`: Unique identifier (format: {video_id}_seg{number})
- `text`: Ground truth fingerspelling text

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

---

For more details, visit the [project page](https://kirandevraj.github.io/ISL-Fingerspelling).
