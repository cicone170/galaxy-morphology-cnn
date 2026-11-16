<h1 align="center">🌌 Galaxy Morphology Classification with CNNs</h1>

<p align="center">
  <b>Can a neural network tell a spiral galaxy from an elliptical one?</b><br>
  My MSc dissertation project at the University of Hull.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white&style=for-the-badge" alt="Python">
  <img src="https://img.shields.io/badge/PyTorch-EE4C2C?logo=pytorch&logoColor=white&style=for-the-badge" alt="PyTorch">
  <img src="https://img.shields.io/badge/scikit--learn-F7931E?logo=scikitlearn&logoColor=white&style=for-the-badge" alt="scikit-learn">
  <img src="https://img.shields.io/badge/Jupyter-F37626?logo=jupyter&logoColor=white&style=for-the-badge" alt="Jupyter">
</p>

<p align="center">
  <img src="results/sample_galaxies.png" width="70%" alt="Sample galaxies">
</p>

---

## 🏆 Results

| Model | Test accuracy | AUC |
|---|---|---|
| Baseline CNN | 84.6% | 0.923 |
| **ResNet18 (transfer learning)** | **86.8%** | **0.943** |

Transfer learning beat the baseline by 2.2 percentage points.

<p align="center">
  <img src="results/roc_comparison.png" width="45%" alt="ROC comparison">
  <img src="results/resnet18_confusion.png" width="45%" alt="ResNet18 confusion matrix">
</p>

---

## 💡 Key findings

- **Humans and the model struggle on the same galaxies.** Accuracy is about 62% on galaxies where labellers disagree. It rises to about 95.8% where they agree.
- **A fair comparison needed a fix.** I found a data normalisation problem and corrected it, so the two models are compared on equal terms.
- **Results match the literature.** I compared them with Barchi et al. (2020) and Dieleman et al. (2015).

<p align="center">
  <img src="results/agreement_accuracy.png" width="55%" alt="Accuracy by label agreement">
</p>

---

## 🛠️ What I did

1. Used Galaxy Zoo 2 images with the Hart et al. (2016) debiased labels.
2. Built a baseline CNN from scratch.
3. Fine-tuned a pre-trained ResNet18.
4. Trained the models on the University of Hull's Viper HPC cluster.
5. Studied how accuracy changes with label agreement, and looked at the mistakes.

<details>
<summary>👀 See examples the model got wrong</summary>
<br>
<p align="center">
  <img src="results/misclassified_examples.png" width="80%" alt="Misclassified examples">
</p>
</details>

---

## 🔒 Code

The code and trained model are private for now.
Available on request: yacine.touatitliba@gmail.com

## 📚 References

- Hart et al. (2016), Galaxy Zoo 2 debiased labels
- Barchi et al. (2020)
- Dieleman et al. (2015)

---

<p align="center">Made by <a href="https://github.com/cicone170">Yacine</a> 🔭</p>