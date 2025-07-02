# Argus: Lightweight VLM for Intelligent Workload Prediction and Resource Allocation in Edge AI

**Argus** is a lightweight Mixture-of-Experts (MoE) Vision-Language Model (VLM) framework for intelligent workload prediction and dynamic resource allocation on edge AI devices. By combining the strengths of state-of-the-art VLMs (CLIP, BLIP, LXMERT), Argus enables efficient, accurate, and real-time decision-making for resource-constrained environments.

---

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [File Structure](#file-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Datasets Supported](#datasets-supported)
- [Experiments](#experiments)
- [Contributing](#contributing)
- [License](#license)

---

## Overview

Edge AI devices are limited in compute, memory, and power. **Argus** predicts the computational workload of upcoming multimodal (image + text) tasks and allocates resources dynamically. It leverages a Mixture-of-Experts approach, integrating multiple VLMs to maximize prediction accuracy and efficiency.

---

## Features

- **Mixture-of-Experts VLM architecture** (CLIP, BLIP, LXMERT)
- **Dynamic workload prediction** for AI tasks
- **Efficient resource allocation** on edge devices
- **Support for multiple datasets:** COCO, Flickr30k, CLEVR, VCR, Visual Genome
- **Lightweight and modular codebase**
- **Ready-to-use embedding extractors and model notebooks**

---

## File Structure

| File/Folder                | Description                                                  |
|---------------------------|--------------------------------------------------------------|
| `Clever_clip&blip/`       | Folder for Clever dataset experiments with CLIP & BLIP models|
| `Coco_vlip&clip/`         | Folder for COCO dataset experiments with CLIP & CLIP models  |
| `Flickr30k_clip&blip/`    | Folder for Flickr30k dataset with CLIP & BLIP models         |
| `VCR_clip&blip/`          | Folder for VCR dataset experiments with CLIP & BLIP models   |
| `vgenome_blip&clip/`      | Folder for Visual Genome dataset with BLIP & CLIP models     |
| `README.md`               | Project documentation                                        |


---

## Installation

git clone https://github.com/yourusername/argus-edge-ai.git
cd argus-edge-ai
pip install -r requirements.txt

**Dependencies:**  
- Python 3.8+
- PyTorch
- Transformers
- OpenAI CLIP
- Other dependencies as listed in `requirements.txt`

---

## Usage

### 1. Extract Embeddings

python blip_embedding_extractor.py --input data/coco/ --output embeddings/blip_coco.pkl
python clip_embedding_extractor.py --input data/coco/ --output embeddings/clip_coco.pkl

### 2. Train/Evaluate Models

Use the provided notebooks:

- `blip-model.ipynb`: BLIP experiments
- `clip-model.ipynb`: CLIP experiments
- `vcr-blip-model.ipynb`: BLIP on VCR dataset

### 3. Custom Model Wrappers

- `Clever_blip_model.py`: Import and use for BLIP-based workload prediction
- `Clever_clip_model.py`: Import and use for CLIP-based workload prediction

---

## Datasets Supported

- COCO
- Flickr30k
- CLEVR
- VCR
- Visual Genome

Prepare datasets in the `data/` folder as per instructions in the notebooks.

---

## Experiments

- Compare Argus (MoE) with individual VLMs on prediction accuracy, efficiency, and resource usage.
- Evaluate on both structured and unstructured datasets.
- Test on edge hardware (Jetson Nano, Raspberry Pi, ARM CPUs).

---

## Contributing

Contributions are welcome! Please open issues or submit pull requests for improvements, bug fixes, or new features.

---

## License

This project is licensed under the MIT License.

---

**Contact:**  
For questions or collaboration, please open an issue or contact the maintainer.
