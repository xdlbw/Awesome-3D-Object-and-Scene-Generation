[![Awesome Logo](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)
[![arXiv](https://img.shields.io/badge/arXiv-2504.11734-b31b1b.svg)](https://arxiv.org/abs/2504.11734)

# Overview

A curated list of awesome 3D object and scene generation papers. 

## Table of Contents

- [3D Object Generation Methods](#methods-a-hierarchical-taxonomy)
  - [Shape](#Shape)
    - [VAE](#variational-autoencoders)
    - [AR](#optimization-based-generation)
    - [GAN](#llm-based-generation)
    - [DM](#llm-based-generation)
  - [Texture](#neural-3d-generation)
  - [Both](#image-based-generation)
    - [GAN](#holistic-generation)
    - [DM](#iterative-generation)
  - [Structure](#video-based-generation)
- [3D Scene Generation methods](#datasets)
  - [Layout-guided](#indoor-datasets)
  - [2D-prior based](#natural-datasets)
    - [iteratiive](#natural-datasets)
    - [全景图](#natural-datasets)
    - [组合式](#natural-datasets)
    - [前馈式](#natural-datasets)
  - [Rule-driven](#urban-datasets)

## 3D Object Generation Methods

### Shape

#### Variational Autoencoders

|                   Preview                   | Title                                                        | Year | Pub. |                            Links                             |
| :-----------------------------------------: | :----------------------------------------------------------- | ---- | :--: | :----------------------------------------------------------: |
| <img src="Preview/deepsdf.png" width="300"> | [DeepSDF: Learning Continuous Signed Distance Functions for Shape Representation](https://arxiv.org/abs/1901.05103) | 2019 | CVPR | [![GitHub](https://img.shields.io/github/stars/facebookresearch/DeepSDF)](https://github.com/facebookresearch/DeepSDF) |
| <img src="Preview/setvae.png" width="300">  | [SetVAE: Learning Hierarchical Composition for Generative Modeling of Set-Structured Data](https://arxiv.org/abs/2103.15619) | 2021 | CVPR | [![GitHub](https://img.shields.io/github/stars/jw9730/setvae)](https://github.com/jw9730/setvae) |

#### Generative Adversarial Networks

|                   Preview                   | Title                                                        | Year | Pub. |                            Links                             |
| :-----------------------------------------: | :----------------------------------------------------------- | ---- | :--: | :----------------------------------------------------------: |
| <img src="Preview/wuetal.png" width="300">  | [Learning a Probabilistic Latent Space of Object Shapes via 3D Generative-Adversarial Modeling](https://arxiv.org/abs/1610.07584) | 2016 | NIPS | [![GitHub](https://img.shields.io/github/stars/black0017/3D-GAN-pytorch)](https://github.com/black0017/3D-GAN-pytorch) |
| <img src="Preview/surfgen.png" width="300"> | [SurfGen: Adversarial 3D Shape Synthesis with Explicit Surface Discriminators](https://arxiv.org/abs/2201.00112) | 2022 | ICCV | [![GitHub](https://img.shields.io/github/stars/aluo-x/NeuralRaycaster)](https://github.com/aluo-x/NeuralRaycaster) |

#### Autoregressive Models

|                      Preview                      | Title                                                        | Year | Pub. |                            Links                             |
| :-----------------------------------------------: | :----------------------------------------------------------- | ---- | :--: | :----------------------------------------------------------: |
|   <img src="Preview/pointgrow.png" width="300">   | [PointGrow: Autoregressively Learned Point Cloud Generation with Self-Attention](https://arxiv.org/abs/1810.05591) | 2018 | WACV | [![GitHub](https://img.shields.io/github/stars/syb7573330/PointGrow)](https://github.com/syb7573330/PointGrow)[![link](https://img.shields.io/badge/Website-cf)](https://liuziwei7.github.io/projects/PointGrow) |
|    <img src="Preview/polygen.png" width="300">    | [PolyGen: An Autoregressive Generative Model of 3D Meshes](https://arxiv.org/abs/2002.10880) | 2020 | ICML | [![GitHub](https://img.shields.io/github/stars/google-deepmind/deepmind-research)](https://github.com/google-deepmind/deepmind-research) |
|  <img src="Preview/shapeformer.png" width="300">  | [ShapeFormer: Transformer-based Shape Completion via Sparse Representation](https://arxiv.org/abs/2201.10326) | 2022 | CVPR | [![GitHub](https://img.shields.io/github/stars/qheldiv/shapeformer)](https://github.com/qheldiv/shapeformer)[![link](https://img.shields.io/badge/Website-cf)](https://shapeformer.github.io/) |
|    <img src="Preview/autosdf.png" width="300">    | [AutoSDF: Shape Priors for 3D Completion, Reconstruction and Generation](https://arxiv.org/abs/2203.09516) | 2022 | CVPR | [![GitHub](https://img.shields.io/github/stars/yccyenchicheng/AutoSDF)](https://github.com/yccyenchicheng/AutoSDF)[![link](https://img.shields.io/badge/Website-cf)](https://yccyenchicheng.github.io/AutoSDF/) |
| <img src="Preview/shapecrafter.png" width="300">  | [ShapeCrafter: A Recursive Text-Conditioned 3D Shape Generation Model](https://arxiv.org/abs/2207.09446) | 2022 | NIPS | [![GitHub](https://img.shields.io/github/stars/FreddieRao/ShapeCrafter)](https://github.com/FreddieRao/ShapeCrafter)[![link](https://img.shields.io/badge/Website-cf)](https://ivl.cs.brown.edu/research/shapecrafter.html) |
| <img src="Preview/clip-sculptor.png" width="300"> | [CLIP-Sculptor: Zero-Shot Generation of High-Fidelity and Diverse Shapes from Natural Language](https://arxiv.org/abs/2211.01427) | 2022 | CVPR | [![link](https://img.shields.io/badge/Website-cf)](https://ivl.cs.brown.edu/research/clip-sculptor.html) |
|    <img src="Preview/meshxl.png" width="300">     | [MeshXL: Neural Coordinate Field for Generative 3D Foundation Models](https://arxiv.org/abs/2405.20853) | 2024 | NIPS | [![GitHub](https://img.shields.io/github/stars/OpenMeshLab/MeshXL)](https://github.com/OpenMeshLab/MeshXL)[![link](https://img.shields.io/badge/Website-cf)](https://meshxl.github.io/) |

#### Diffusion Models

|                     Preview                      | Title                                                        | Year | Pub.  |                            Links                             |
| :----------------------------------------------: | ------------------------------------------------------------ | ---- | :---: | :----------------------------------------------------------: |
|     <img src="Preview/pvd.png" width="300">      | [3D Shape Generation and Completion through Point-Voxel Diffusion](https://arxiv.org/abs/2104.03670) | 2021 | ICCV  | [![GitHub](https://img.shields.io/github/stars/alexzhou907/PVD)](https://github.com/alexzhou907/PVD)[![link](https://img.shields.io/badge/Website-cf)](https://alexzhou907.github.io/pvd) |
|   <img src="Preview/sdfusion.png" width="300">   | [SDFusion: Multimodal 3D Shape Completion, Reconstruction, and Generation](https://arxiv.org/abs/2212.04493) | 2022 | CVPR  | [![GitHub](https://img.shields.io/github/stars/yccyenchicheng/SDFusion)](https://github.com/yccyenchicheng/SDFusion)[![link](https://img.shields.io/badge/Website-cf)](https://yccyenchicheng.github.io/SDFusion/) |
| <img src="Preview/michelangelo.png" width="300"> | [Michelangelo: Conditional 3D Shape Generation based on Shape-Image-Text Aligned Latent Representation](https://arxiv.org/abs/2306.17115) | 2023 | NIPS  | [![GitHub](https://img.shields.io/github/stars/NeuralCarver/Michelangelo)](https://github.com/NeuralCarver/Michelangelo)[![link](https://img.shields.io/badge/Website-cf)](https://neuralcarver.github.io/michelangelo/) |
|   <img src="Preview/hi3dgen.png" width="300">    | [Hi3DGen: High-fidelity 3D Geometry Generation from Images via Normal Bridging](https://arxiv.org/abs/2503.22236) | 2025 | ICCV  | [![GitHub](https://img.shields.io/github/stars/bytedance/Hi3DGen)](https://stable-x.github.io/Hi3DGen/)[![link](https://img.shields.io/badge/Website-cf)](https://stable-x.github.io/Hi3DGen/) |
|   <img src="Preview/direct3d.png" width="300">   | [Direct3D-S2: Gigascale 3D Generation Made Easy with Spatial Sparse Attention](https://arxiv.org/abs/2505.17412) | 2025 | NIPS  | [![GitHub](https://img.shields.io/github/stars/DreamTechAI/Direct3D-S2)](https://github.com/DreamTechAI/Direct3D-S2)[![link](https://img.shields.io/badge/Website-cf)](https://www.neural4d.com/research-page/direct3d-s2/index.html) |
|   <img src="Preview/ultra3d.png" width="300">    | [Ultra3D: Efficient and High-Fidelity 3D Generation with Part Attention](https://arxiv.org/abs/2507.17745) | 2025 | Arxiv | [![link](https://img.shields.io/badge/Website-cf)](https://buaacyw.github.io/ultra3d/) |
