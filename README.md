````
# BCFusion
Codes for ***BCFusion: A BiomedCLIP Semantic-Guided Mamba Enhanced Network for Multi-modal Medical Image Fusion***

## Abstract
Multimodal Medical Image Fusion (MMIF) aims to synthesize complementary information from diverse imaging modalities into a unified representation, facilitating clinical auxiliary analysis. While deep learning-based approaches have shown promise, they are primarily constrained by three fundamental limitations : (1) fixed-scale convolutions lack the adaptability required to handle the complex anatomical morphologies of medical images; (2) the prevalent reliance on deep-stacked architectures leads to the indiscriminate propagation of local details and global context, compromising both feature discriminability and computational efficiency ; and (3) conventional pixel-level loss functions lack explicit guidance from high-level medical semantics, often resulting in critical lesion regions being obscured by irrelevant pixel intensities. To address these challenges, we propose BCFusion, a lightweight collaborative fusion network that synergizes CNN and Mamba with BiomedCLIP-based semantic guidance. Instead of exhaustive block stacking, BCFusion utilizes an Adaptive Feature Selection Module (AFSM) to dynamically calibrate the effective receptive field and compress redundant channels at an early stage. We further design a Redundancy-suppressed Mamba (R-Mamba) module, which balances local detail enhancement with long-range dependency modeling while utilizing spatial-channel reconstruction to filter non-discriminative features. Finally, a BiomedCLIP-guided semantic loss is introduced to enforce clinical meaningfulness via textual constraints. Extensive experiments demonstrate that BCFusion, with only 0.18M parameters, achieves state-of-the-art visual quality and quantitative performance across multiple datasets.
## Update

## Citation

```

## 🌐 Usage

### 🏊 Training
**1. Data Preparation**

Harvard medical website,  http://www.med.harvard.edu/AANLIB/home.html

**2. Commence Training**

```
python train.py
``` 

### 🏄 Testing

**1. Pretrained models**

Pretrained models are available in ``./models/model_300.pth``, which are the models trained on Harvard datasets.

**2. Test cases**

Running 
```
python test.py
``` 
will fuse these cases, and the fusion results will be saved in the 'output' folder.

````
