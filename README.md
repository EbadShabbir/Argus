# Argus: Can Argus Judge Them All? Comparing VLMs Across Domains

**Argus** is a lightweight Mixture-of-Experts (MoE) Vision-Language Model (VLM) framework designed for intelligent workload prediction and dynamic resource allocation on edge AI devices. By combining the strengths of state-of-the-art VLMs—**CLIP**, **BLIP**, and **LXMERT**—Argus enables efficient, accurate, and real-time decision-making in resource-constrained environments.

---

## 📚 Supported Datasets

Argus supports a diverse set of multimodal datasets. Prepare each dataset in the `data/` directory as described in the provided notebooks.

- **COCO**  
  Large-scale object detection, segmentation, and captioning dataset.

- **Flickr30k**  
  Image captioning dataset with diverse real-world scenes.

- **CLEVR**  
  Diagnostic dataset for compositional language and elementary visual reasoning.

- **VCR**  
  Visual Commonsense Reasoning dataset for understanding images and associated questions.

- **Visual Genome**  
  Dense annotations of objects, attributes, and relationships within images.

---

## 🧠 Mixture-of-Experts VLMs

Argus integrates the following state-of-the-art vision-language models:

- **CLIP** (OpenAI)  
  Contrastive Language–Image Pretraining for zero-shot image classification.

- **BLIP** (Bootstrapped Language Image Pretraining)  
  Flexible vision-language model for a variety of multimodal tasks.

- **LXMERT**  
  Transformer-based model for learning vision-and-language cross-modal representations.

Each model can be used individually or as part of Argus's Mixture-of-Experts architecture for improved prediction and efficiency.

---

## 🛠️ Usage

### 1. Installation

Install dependencies:

pip install -r requirements.txt

**Core dependencies:**  
- Python 3.8+  
- PyTorch  
- Transformers  
- OpenAI CLIP  
- Additional packages as listed in `requirements.txt`

---

### 2. Embedding Extraction

Extract image-text embeddings for your dataset:

python blip_embedding_extractor.py --input data/coco/ --output embeddings/blip_coco.pkl
python clip_embedding_extractor.py --input data/coco/ --output embeddings/clip_coco.pkl

---

### 3. Training and Evaluation

Use the provided Jupyter notebooks for model training and evaluation:

- `blip-model.py` — BLIP experiments
- `clip-model.py` — CLIP experiments
- `vcr-blip-model.py` — BLIP on VCR dataset

For custom model wrappers:

- `Clever_blip_model.py` — BLIP-based workload prediction
- `Clever_clip_model.py` — CLIP-based workload prediction

---

## 🧩 File Structure

| File/Folder                | Description                                                  |
|---------------------------|--------------------------------------------------------------|
| `Clever_clip&blip/`       | CLEVR dataset experiments with CLIP & BLIP                   |
| `Coco_vlip&clip/`         | COCO dataset experiments with CLIP & CLIP                    |
| `Flickr30k_clip&blip/`    | Flickr30k dataset with CLIP & BLIP                           |
| `VCR_clip&blip/`          | VCR dataset experiments with CLIP & BLIP                     |
| `vgenome_blip&clip/`      | Visual Genome dataset with BLIP & CLIP                       |
| `README.md`               | Project documentation                                        |

---

## ⚡ Experiments

- Compare **Argus (MoE)** with individual VLMs on prediction accuracy, efficiency, and resource usage.
- Evaluate across both structured and unstructured datasets.
- Benchmark on edge hardware (Jetson Nano, Raspberry Pi, ARM CPUs).

---

## 🤝 Contributing

Contributions are welcome!  
Open issues or submit pull requests for improvements, bug fixes, or new features.

---

## 📄 License

This project is licensed under the MIT License.

---

**Contact:**  
For questions or collaboration, please open an issue or contact the maintainer.
