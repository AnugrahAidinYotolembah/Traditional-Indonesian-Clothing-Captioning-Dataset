# Traditional-Indonesian-Clothing-Captioning-Dataset
A cultural heritage vision-language dataset containing 3,800 expert-annotated images of Indonesian traditional clothing from 38 provinces for zero-shot image captioning and retrieval-augmented multimodal research.

---

## Overview

This repository contains the **Traditional Indonesian Clothing Captioning Dataset**, a culturally grounded image-caption dataset designed for:

- Zero-shot image captioning
- Vision-language learning
- Cultural heritage understanding
- Retrieval-augmented caption generation
- Low-resource AI research

The dataset was developed for the research paper:

> **Custom ZeroCLIP: Retrieval-Augmented Vision-Language Framework for Zero-Shot Captioning of Traditional Indonesian Clothing**

The dataset includes **3,800 expert-annotated images** representing traditional clothing from **all 38 provinces of Indonesia**.

---

## Dataset Highlights

- 3,800 traditional clothing images
- 38 Indonesian provinces
- Expert-written cultural captions
- Province-level zero-shot split
- Designed for vision-language and captioning tasks

### Suitable Research Areas

- Image captioning
- Zero-shot learning
- Cross-cultural AI
- Retrieval-augmented generation (RAG)
- CLIP-based research
- Multimodal learning

---

## Zero-Shot Evaluation Protocol

To ensure strict generalization evaluation, the dataset follows a **province-level inductive zero-shot protocol**.

| Split | Provinces | Description |
|---|---|---|
| Training | 24 provinces | Used for model training |
| Validation | 6 provinces | Used for hyperparameter tuning |
| Testing | 8 unseen provinces | Completely unseen during training |

### Important Constraints

During testing:

- No unseen-province images are used during training
- No unseen-province captions are used
- No unseen-province labels are available
- Retrieval bank only contains captions from training provinces

This setting evaluates the model’s ability to generalize cultural understanding to entirely unseen regional clothing traditions.

---

## Framework Overview

The proposed framework combines:

- CLIP ViT-B/32 Image Encoder
- CLIP Text Encoder
- BERT Text Encoder
- LSTM Caption Decoder
- Retrieval-Augmented Caption Generation

The framework is designed for culturally grounded caption generation under low-resource heritage scenarios.

---

## Benchmark Results

| Metric | Score |
|---|---|
| CLIPScore | 0.8536 |
| BLEU-4 | 0.3342 |
| METEOR | 0.4859 |

### Key Findings

- Retrieval augmentation improves cultural vocabulary recovery
- METEOR improves by **19.3%** through retrieval integration
- Human evaluation confirms:
  - Better cultural accuracy
  - Improved fluency
  - More descriptive captions

---

## Dataset Structure

```text
Traditional-Indonesian-Clothing-Captioning-Dataset/
│
├── images/
│   ├── Aceh/
│   ├── Bali/
│   ├── Papua/
│   └── ...
│
├── annotations/
│   ├── train_captions.json
│   ├── val_captions.json
│   ├── test_captions.json
│   └── metadata.csv
│
├── splits/
│   ├── train_provinces.txt
│   ├── val_provinces.txt
│   └── unseen_test_provinces.txt
│
├── examples/
│
├── README.md
└── LICENSE
```

---

## Example Caption

### Input

Traditional attire image from an unseen Indonesian province.

### Generated Caption

> “A person wearing traditional ceremonial clothing with intricate woven patterns, cultural ornaments, and regional heritage accessories.”

---

## Applications

This dataset can support research in:

- Zero-shot image captioning
- Cultural heritage AI
- Vision-language alignment
- Retrieval-augmented generation
- Cross-domain generalization
- Low-resource language technology
- Multimodal learning

---

## Citation

If you use this dataset in your research, please cite:

```bibtex
@article{customzeroclip2026,
  title={Custom ZeroCLIP: Retrieval-Augmented Vision-Language Framework for Zero-Shot Captioning of Traditional Indonesian Clothing},
  author={Author Names},
  journal={Conference/Journal Name},
  year={2026}
}
```

---

## License

This dataset is provided for:

- Research purposes
- Educational purposes
- Non-commercial use

Please ensure proper citation when using the dataset.

---

## Acknowledgements

We thank cultural experts and annotators who contributed to the preservation and documentation of Indonesian traditional clothing heritage across all provinces.

---

## Contact

For questions, collaborations, or dataset access requests, please open an issue or contact the repository maintainer.
