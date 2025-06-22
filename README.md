# 🏥 Synthetic EHR Generation and Evaluation using EMR-WGAN

## 📌 Overview
This repository presents a tutorial for generating and evaluating **synthetic electronic health record (EHR)** data using the **MIMIC-IV V2.0 dataset** and the **EMR-WGAN** model.  
It is based on the paper:

**Yan C, Zhang Z, Nyemba S, Li Z.**  
*Generating synthetic electronic health record data using generative adversarial networks: A tutorial.*

> ✅ Project implemented and adapted by **Mushkan Narayan**

---

## 💻 System Requirements

### 🖥️ OS
- **Linux (tested on Ubuntu 20.04)**

### 🐍 Python (3.7.16) Dependencies
- `tensorflow`
- `pandas`
- `numpy`
- `argparse`
- `matplotlib`
- `scipy`
- `sklearn`
- `lightgbm`
- `joblib`
- `shap`
- `requests`

### 📦 Install all dependencies
```bash
pip install -r requirement.txt

**📂 Project Components**

📁 Data Preprocessing

Before starting, download the MIMIC-IV V2.0 dataset from
🔗 https://physionet.org/content/mimiciv/2.0/
(by completing the required credentialing and training).

To prepare the dataset:

Run dataset_preprocess.ipynb step by step.

** GAN Training**
To train the EMR-WGAN model:
python GAN_training.py --gpu_id <gpu_id> --model_id <model_id>

🧬 Synthetic Data Generation
To generate synthetic data from a trained model:
python GAN_generation.py --gpu_id <gpu_id> --model_id <model_id> --load_checkpoint <checkpoint_id>

📊 Utility Evaluation
Run utility_evaluation.ipynb to evaluate the utility of generated synthetic datasets.
Multiple utility metrics are included.
The notebook demonstrates evaluation for 5 different EMR-WGAN models.

🔐 Privacy Evaluation
Run privacy_evaluation.ipynb to assess the privacy risk of the generated datasets.
Includes multiple privacy metrics.
Also evaluates 5 different EMR-WGAN models.

🏆 Selecting the Best Dataset
Run rank_datasets.ipynb to rank and select the optimal synthetic dataset.
You’ll provide weights for each metric based on the importance to your use case.

📖 References to Cite
Yan C, Yan Y, Wan Z, Zhang Z, Omberg L, Guinney J, Mooney SD, Malin BA.
A multifaceted benchmarking of synthetic electronic health record generation models.
Nature Communications, 2022; 13(1): 7609.

Zhang Z, Yan C, Mesa DA, Sun J, Malin BA.
Ensuring electronic medical record simulation through better training, modeling, and evaluation.
Journal of the American Medical Informatics Association, 2020; 27(1): 99–108.
