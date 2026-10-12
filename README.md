# Self-MAR: Self-Supervised Multi-Stage Autoregressive Model for Water-Related Optical Image Enhancement

> **Publication venue:** IEEE Transactions on Pattern Analysis and Machine Intelligence (TPAMI)
> **Status:** Code release coming soon 🚧

Official implementation of **Self-MAR** (a.k.a. elf-MAR), a self-supervised paradigm for water-related optical image enhancement that enables **input-only restoration** via a VAR-inspired **M**ulti-stage **A**uto**R**egressive model, in which each restoration stage is conditioned on the preceding restored state.

---

## Abstract

We propose Self-MAR, a self-supervised paradigm for water-related optical image enhancement that enables input-only restoration via the proposed VAR-inspired Multi-stage AutoRegressive model, in which each restoration stage is conditioned on the preceding restored state. The intricate interactions between light and the water medium introduce residual degradations that are difficult to model explicitly, thereby limiting the effectiveness of existing methods that rely heavily on synthetic data or sparse annotations. Furthermore, acquiring paired ground-truth data in real underwater environments remains challenging, giving rise to the triangular dilemma in underwater image enhancement (UIE). To address these issues, Self-MAR incorporates three key components: (1) a multi-stage, coarse-to-fine reconstruction architecture that progressively recovers image structure and suppresses content-coupled underwater object residuals (ORs) at different resolutions, transforming OR removal into structure-aware controllable image generation; (2) an asymmetric phase-amplitude interaction that combines the structural phase of the current observation with the corrected spectral-energy distribution of the preceding restoration estimate; and (3) a Churning constraint mechanism that preserves the original perceptual features of the input image and prevents semantic drift during self-supervised training. Self-MAR derives supervision targets from the inputs themselves: underwater inputs generate OR-removal targets, while in-air inputs generate structural self-reconstruction targets from their own content. Extensive experiments demonstrate competitive full-reference restoration quality, leading performance across complementary no-reference metrics (UIQM, UCIQE, NIQE, and URANKER), efficient inference, and consistent performance across UIEB C60, UCCS, U45, and Z700. Downstream evaluation on SeaThru-D1 further shows the lowest combined depth-consistency error among the compared state-of-the-art enhancement methods.

---

## Key Highlights

- **Input-only, self-supervised restoration.** No paired GT is required: underwater inputs supervise OR removal, in-air inputs supervise structural self-reconstruction.
- **Multi-stage autoregressive design.** A VAR-inspired coarse-to-fine pipeline where each stage is conditioned on the preceding restored state, progressively recovering structure while suppressing content-coupled object residuals (ORs) across resolutions.
- **Asymmetric phase-amplitude interaction.** The structural *phase* of the current observation is combined with the *corrected spectral-energy distribution* of the previous estimate, preserving spatial organization during stage-wise upsampling and propagating color-energy statistics from coarse to fine.
- **Churning constraint.** Regularizes training to keep the original perceptual features of the input and prevent semantic drift.
- **State-of-the-art performance.** Leading no-reference metrics (UIQM, UCIQE, NIQE, URANKER), competitive full-reference quality, and consistent results on UIEB C60, UCCS, U45, Z700; lowest combined depth-consistency error on downstream SeaThru-D1 evaluation.
- **Efficient inference.** Fast restoration suitable for practical deployment.

---

## News

- **[2026-10]** Code and pretrained models are being prepared for release.

---

## Getting Started

Instructions for installation, dataset preparation, training, inference, and evaluation will be available soon.

| Section | Status |
| --- | --- |
| Installation | Coming soon |
| Dataset preparation | Coming soon |
| Training | Coming soon |
| Inference | Coming soon |
| Evaluation | Coming soon |
| Pretrained models | Coming soon |

---

## Citation

If you find this work useful, please cite:

```bibtex
@article{selfmar2026,
  title   = {Self-MAR: Self-Supervised Multi-Stage Autoregressive Model for Water-Related Optical Image Enhancement},
  journal = {IEEE Transactions on Pattern Analysis and Machine Intelligence},
  year    = {2026},
}
```

---

## License

Code is released for research purposes only. Please refer to `LICENSE` for details.

## Acknowledgements

Thanks to the authors of UIEB, UCCS, U45, Z700, and SeaThru-D1 for publicly releasing their datasets.
