# LMM-Track4D

<p align="center">
  <strong>Eliciting 4D Dynamic Reasoning in Large Multimodal Models via Trajectory-Grounded Dialogue</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Task-4D%20Dynamic%20Reasoning-6A5ACD" alt="Task badge" />
  <img src="https://img.shields.io/badge/Benchmark-526%20clips-0A84FF" alt="Benchmark badge" />
  <img src="https://img.shields.io/badge/Code-Coming%20Soon-F5A623" alt="Code badge" />
  <img src="https://img.shields.io/badge/Dataset-Coming%20Soon-F5A623" alt="Dataset badge" />
  <a href="./assets/demo.mp4"><img src="https://img.shields.io/badge/Demo-Available-2EA44F" alt="Demo badge" /></a>
  <img src="https://img.shields.io/badge/arXiv-Coming%20Soon-B1B5C0" alt="arXiv badge" />
</p>

<p align="center">
  <a href="#abstract">Abstract</a> •
  <a href="#overview">Overview</a> •
  <a href="#at-a-glance">At a Glance</a> •
  <a href="#highlights">Highlights</a> •
  <a href="#task-overview">Task</a> •
  <a href="#architecture">Architecture</a> •
  <a href="#demo">Demo</a> •
  <a href="#release-status">Release Status</a> •
  <a href="#citation">Citation</a>
</p>

## Abstract

Recent large multimodal models (LMMs) have become increasingly capable on image and video understanding, yet still struggle to sustain 4D continuous spatiotemporal dynamic reasoning. To study this capability gap, we formulate **trajectory-grounded multi-turn spatiotemporal dialogue**, a task in which a model must answer spatiotemporal queries while returning structured 3D target trajectories over an entire short clip or a specified segment of a longer clip. We further introduce **Track4D-Bench**, a benchmark with 526 clip-level dialogue samples spanning 23.5k frames and 7.5k object annotations, and propose **LMM-Track4D**, which combines **RTGE** (Ray-Time Geometry Encoding), a dedicated streaming state token **TRK** for long-horizon dynamic propagation, and **OSK-RA** decoding for stable 3D state estimation under occlusion and viewpoint variation. Experiments on Track4D-Bench show consistent improvements over strong baselines, suggesting that explicit dynamic state modeling is a useful design principle for eliciting 4D dynamic reasoning in LMMs.

## Overview

LMM-Track4D studies a central capability gap in current large multimodal models: although they can describe images and videos well, they remain weak at maintaining coherent dynamic scene state across time, viewpoints, and multi-turn interaction. The project targets **dialogue-grounded 4D dynamic reasoning**, where a model must answer spatiotemporal questions while preserving a physically consistent account of how the scene evolves.

To address this setting, we introduce **trajectory-grounded multi-turn spatiotemporal dialogue**, a task in which the model answers spatiotemporal queries and, when required, predicts structured 3D target trajectories. We further introduce **Track4D-Bench**, a benchmark for training and evaluating this capability, and **LMM-Track4D**, a model that combines geometry-aware encoding, persistent state propagation, and structured trajectory decoding.

## At a Glance

| Component | Description |
| --- | --- |
| **Task** | Trajectory-grounded multi-turn spatiotemporal dialogue |
| **Benchmark** | 526 clip-level dialogue samples, 23.5k frames, and 7.5k object annotations |
| **Model** | RTGE + persistent TRK state propagation + OSK-RA decoding |
| **Focus** | Long-horizon, geometry-grounded 4D dynamic reasoning |

## Highlights

- **Task formulation**: A dialogue-grounded setting that couples language responses with explicit 3D dynamic-state prediction.
- **Benchmark**: Track4D-Bench is designed to train and evaluate sustained 4D dynamic reasoning under multi-turn interaction.
- **Model design**: LMM-Track4D combines RTGE, persistent TRK state propagation, and OSK-RA decoding.
- **Capability emphasis**: The project focuses on dynamic scene continuity, identity preservation, and structured trajectory reasoning.

## Task Overview

<p align="center">
  <img src="./assets/task.png" alt="Task overview for LMM-Track4D" width="96%" />
</p>

Trajectory-grounded multi-turn spatiotemporal dialogue requires the model to answer spatiotemporal queries while maintaining and updating explicit dynamic scene state throughout the interaction.

## Architecture

<p align="center">
  <img src="./assets/method.png" alt="Method overview for LMM-Track4D" width="96%" />
</p>

LMM-Track4D combines **RTGE** for ray-time geometric encoding, a persistent **TRK** token for cross-turn state propagation, and **OSK-RA** for structured query-conditioned 3D trajectory decoding.

## Demo

<p align="center">
  <a href="./assets/demo.mp4">
    <img src="./assets/demo.gif" alt="Animated demo for LMM-Track4D" width="96%" />
  </a>
</p>

<p align="center">
  <a href="./assets/demo.mp4"><strong>Open full demo.mp4</strong></a>
</p>

The preview above is provided as a GIF for GitHub compatibility. Click it to open the original MP4 demo showing dialogue-grounded reasoning over evolving dynamic scene state together with structured trajectory prediction.

## Release Status

> [!NOTE]
> This repository currently hosts the project overview and visual assets. The public release of code, data, checkpoints, and reproduction materials is in preparation.

| Asset | Status |
| --- | --- |
| **Code** | Coming soon |
| **Track4D-Bench dataset** | Coming soon |
| **Model checkpoints** | Coming soon |
| **Training and evaluation scripts** | Coming soon |
| **Reproducibility documentation** | Coming soon |

## Citation

If you find this project useful, please cite the arXiv version:

```bibtex
@article{lmmtrack4d2026,
  title={LMM-Track4D: Eliciting 4D Dynamic Reasoning in Large Multimodal Models via Trajectory-Grounded Dialogue},
  author={Author List},
  journal={arXiv preprint arXiv:XXXX.XXXXX},
  year={2026}
}
```

Please replace `Author List` and `XXXX.XXXXX` with the final public arXiv metadata once the preprint is available.
