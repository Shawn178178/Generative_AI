# HW3 - GAN-Based Data Augmentation

This assignment explores the use of Generative Adversarial Networks (GANs) for text-based data augmentation, including model implementation, environment setup, and training evaluation.

## 🧰 Environment Setup

- **CUDA Version**: Switched manually according to TA’s instructions
- **TensorFlow Installation**:
  - Extracted `.whl` files using 7-Zip
  - Verified installation via test script

## 🧠 Models Used

### 1. SeqGAN
- Run with:  
  `python main.py -g Seqgan -t real -d data/image_coco.txt`
- Required code completion in:
  - `Seqgan.py`
  - `SeqganGenerator.py`
  - `SeqganReward.py`
- Output: `experiment-log-seqgan-real.csv`

### 2. RankGAN
- Modified `RankganDiscriminator.py`:
  - Imported `linear` and `highway` methods from this repo:  
    [tf-lstm-char-cnn](https://github.com/mkroutikov/tf-lstm-char-cnn)
- Updated DataLoader to complete the workflow

### 3. MaliGAN
- Similar DataLoader modifications required
- Completed all missing function stubs before training

## 📈 Data Augmentation Experiment

- **Custom Dataset**: `dog.txt` from [DNA Sequence Dataset on Kaggle](https://www.kaggle.com/datasets/nageshsingh/dna-sequence-dataset)
- **Result File**: `experiment-log-seqgan-real.csv`
- **Metric**: Negative Log-Likelihood (NLL)
  - NLL steadily decreased over epochs, indicating improved generation quality

## 📁 Code Location
All code and logs are stored in this folder.  
GitHub Repo: [https://github.com/Shawn178178/Generative_AI.git](https://github.com/Shawn178178/Generative_AI.git)

## 🧾 Author
**Student ID**: n96131281  
**Institution**: NCKUES  
**Course**: Generative Artificial Intelligence
