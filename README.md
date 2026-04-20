# SoundBreak: A Systematic Study of Audio-Only Adversarial Attacks on Trimodal Models

[![ACL 2026](https://img.shields.io/badge/ACL%202026-Main%20Conference-red)](https://2026.aclweb.org/)
[![arXiv](https://img.shields.io/badge/arXiv-2601.16231-b31b1b.svg)](https://arxiv.org/abs/2601.16231)
[![Website](https://img.shields.io/badge/Website-SoundBreak-blue)](https://aafiya-h.github.io/soundbreak/)

This repository contains the project website for **SoundBreak**, a systematic study of untargeted, audio-only adversarial attacks on trimodal audio–video–language models. Accepted at **ACL 2026 Main Conference**.

## Overview

We study a realistic and underexplored threat model: **untargeted, audio-only adversarial attacks** on trimodal audio–video–language models. We propose six complementary attack objectives targeting different stages of multimodal processing — audio encoder representations, cross-modal attention, hidden states, and output likelihoods.

### Key Results

- Up to **96% attack success rate** using the combined loss on VideoLLAMA2
- Attacks succeed at low perceptual distortion (LPIPS ≤ 0.08, SI-SNR ≥ 0 dB)
- Extended optimization outperforms larger datasets
- Combined attack achieves **97.96% ASR** under physically simulated (RIR) conditions
- Limited cross-model and cross-encoder transferability

### Attack Objectives

| Objective | Target | AVQA ASR (%) |
|-----------|--------|--------------|
| Negative LM Loss | Output likelihood | 10.27 |
| Encoder Cosine Similarity | Audio encoder | 89.12 |
| Vision Attention Suppression | Cross-modal attention | 18.72 |
| Audio Attention Amplification | Audio attention | 56.21 |
| Attention Randomization | Attention structure | 17.24 |
| Hidden-State Similarity | Hidden states | 15.13 |
| **Combined** | All stages | **96.03** |

### Models Evaluated

- **VideoLLAMA2** (primary, white-box)
- **Qwen 2.5 Omni** (black-box transfer)
- **Qwen 3 Omni** (black-box transfer)
- **Video-SALMONN2** (black-box transfer)
- **Whisper Large-v2** (ASR evaluation)

### Benchmarks

- **AVQA** — Multiple-choice audio-visual question answering
- **Music-AVQA** — Short-answer questions on musical performances
- **AVSD** — Video-based textual summarization (LLM-as-a-judge)
- **LibriSpeech** — Speech recognition (WER evaluation)

## Authors

- [Aafiya Shamshad Hussain](https://www.linkedin.com/in/aafiya-hussain-a66870179/) (Virginia Tech)
- [Gaurav Srivastava](https://www.linkedin.com/in/gaurav-srivastava-gk/) (Virginia Tech)
- [Alvi Md Ishmam](https://www.linkedin.com/in/alvi-ishmam) (Virginia Tech)
- [Zaber Ibn Abdul Hakim](https://www.linkedin.com/in/zaber-ibn-abdul-hakim-024010185/) (Virginia Tech)
- [Chris Thomas](https://people.cs.vt.edu/chris/) (Virginia Tech)

## Repository Structure

```
soundbreak/
├── index.html          # Project website
├── static/
│   ├── css/            # Stylesheets
│   ├── js/             # JavaScript
│   └── images/         # Figures from the paper
└── README.md
```

## Citation

```bibtex
@article{hussain2025soundbreak,
  title={SoundBreak: A Systematic Study of Audio-Only Adversarial Attacks on Trimodal Models},
  author={Hussain, Aafiya Shamshad and Srivastava, Gaurav and Ishmam, Alvi Md and Hakim, Zaber Ibn Abdul and Thomas, Chris},
  year={2025}
}
```

## License

This project is licensed under the MIT License — see [LICENSE](LICENSE) for details.
