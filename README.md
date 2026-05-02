# ISL Fingerspelling Dataset

[![Dataset](https://img.shields.io/badge/Dataset-Hugging%20Face-yellow)](https://huggingface.co/datasets/kirandevraj/ISL-Fingerspelling)
[![WSLP 2025](https://img.shields.io/badge/Paper-WSLP%202025-blue)](https://kirandevraj.github.io/ISL-Fingerspelling)
[![ICPR 2026](https://img.shields.io/badge/Paper-ICPR%202026-blue)](https://kirandevraj.github.io/ISL-Fingerspelling)
[![License](https://img.shields.io/badge/License-CC%20BY--NC%204.0-green)](https://creativecommons.org/licenses/by-nc/4.0/)

> **Continuous Fingerspelling Dataset for Indian Sign Language**
> WSLP @ AACL-IJCNLP 2025 | ICPR 2026

**[Project Page](https://kirandevraj.github.io/ISL-Fingerspelling)** | **[Dataset (Hugging Face)](https://huggingface.co/datasets/kirandevraj/ISL-Fingerspelling)**

---

## Overview

A continuous fingerspelling resource for Indian Sign Language. The project hosts two complementary releases:

- **ISL-FS** (WSLP @ AACL-IJCNLP 2025) — 1,308 video segments from 499 ISH News videos with aligned word-level text.
- **ISL-FS-Dense** (ICPR 2026) — adds character-level frame boundaries for every letter (99.1% expert-validated) and 11,700+ auto-discovered segments from the iSign corpus. Dataset link coming soon.

## Statistics

### ISL-FS (word-level)

| Segments | Duration | Characters | Videos | Signers | Validation Acc. |
|----------|----------|------------|--------|---------|-----------------|
| 1,308    | 70 min   | 14,814     | 499    | 3       | 90.67%          |

### ISL-FS-Dense (frame-level + auto-discovered)

| Annotated Frames | Character Instances | Unique Chars | Expert Validation | Auto-Discovered | Recognition CER | Detection F1 |
|------------------|---------------------|--------------|-------------------|-----------------|-----------------|--------------|
| 125,661          | 14,682              | 38           | 99.1%             | 11,700+         | 4.87%           | 84.6%        |

## Dataset Structure

```
ISL-Fingerspelling/
├── videos/                        # 1,308 MP4 video files
├── fingerspelling_annotations.csv # Segment annotations
├── localization_timestamps.csv    # Temporal localization in source videos
└── README.md
```

### CSV Format

`fingerspelling_annotations.csv`
- `uid`: Unique identifier (format: `{video_id}_seg{number}`)
- `text`: Ground truth fingerspelling text

`localization_timestamps.csv`
- `video_id`, `segment_index`
- `start_time` / `start_sec`, `end_time` / `end_sec`
- `duration_str` / `duration_sec`
- `transcript`

ISL-FS-Dense will add character-level frame boundaries for every letter and the 11,700+ auto-discovered segments. Link will be added here once published.

## Citation

If you use either release, please cite the relevant paper(s):

```bibtex
@inproceedings{r-etal-2025-continuous,
  title     = {Continuous Fingerspelling Dataset for {I}ndian {S}ign {L}anguage},
  author    = {R, Kirandevraj and Kurmi, Vinod K. and Namboodiri, Vinay P. and Jawahar, C.V.},
  booktitle = {Proceedings of the Workshop on Sign Language Processing (WSLP)},
  publisher = {Association for Computational Linguistics},
  year      = {2025},
  pages     = {33--38},
  url       = {https://aclanthology.org/2025.wslp-main.6/},
  doi       = {10.18653/v1/2025.wslp-main.6}
}
```

```bibtex
@inproceedings{kirandevraj2026denseisl,
  title     = {Dense Frame Annotations for Low-Resource ISL Fingerspelling Recognition},
  author    = {Kirandevraj, R and Kurmi, Vinod K and Namboodiri, Vinay P and Jawahar, CV},
  booktitle = {Proceedings of the International Conference on Pattern Recognition (ICPR)},
  year      = {2026}
}
```

## Authors

- **R Kirandevraj** (IIIT Hyderabad) — kirandevraj.r@research.iiit.ac.in
- **Vinod K Kurmi** (IISER Bhopal)
- **Vinay P Namboodiri** (University of Bath)
- **CV Jawahar** (IIIT Hyderabad)

## License

Released under [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/) for research purposes only.

---

For more details, visit the [project page](https://kirandevraj.github.io/ISL-Fingerspelling).
