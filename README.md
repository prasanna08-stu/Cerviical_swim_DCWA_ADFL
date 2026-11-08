# Cerviical_swim_DCWA_ADFL
A leakage-free, five-class cervical cell classification system using a Swin Transformer with Dynamic Cross-Window Attention (DCWA), Adaptive Dynamic Focal Loss (ADFL), and quantitative Grad-CAM explainability on the SIPaKMeD dataset.
Leakage-Free Cervical Cell Classification Using Swin Transformer

Dynamic Cross-Window Attention (DCWA) and Adaptive Dynamic Focal Loss (ADFL)

📌 Project Overview

This project presents a deep learning approach for automated cervical cell classification using the Swin Transformer architecture. It introduces Dynamic Cross-Window Attention (DCWA) to improve information exchange between image windows and Adaptive Dynamic Focal Loss (ADFL) to adapt to class difficulty during training.

The system is developed using the SIPaKMeD dataset and focuses on leakage-free evaluation, classification performance, and quantitative explainability.

The objective is to support cytologists by providing an AI-based second-reader system for cervical cell assessment.

🎯 Objectives

- Develop a five-class cervical cell classification model.
- Implement Dynamic Cross-Window Attention (DCWA).
- Introduce Adaptive Dynamic Focal Loss (ADFL).
- Prevent data leakage through cluster-wise dataset splitting.
- Evaluate model performance using standard classification metrics.
- Analyse model explanations using Grad-CAM, deletion and insertion curves.

📂 Dataset

Dataset: SIPaKMeD

- Total images: 5,015
- Number of classes: 5
- Held-out test images: 734

Classification Categories

1. Dyskeratotic
2. Koilocytotic
3. Metaplastic
4. Parabasal
5. Superficial-Intermediate

🧠 Proposed Methodology

1. Swin Transformer

A hierarchical vision transformer is used as the backbone to extract morphological features from cervical cell images through local and shifted-window attention.

2. Dynamic Cross-Window Attention (DCWA)

DCWA introduces content-dependent connectivity between image windows. It calculates window affinities and gathers contextual information, which is integrated into individual tokens through a learned gate.

3. Adaptive Dynamic Focal Loss (ADFL)

ADFL dynamically adjusts class weights and focusing parameters based on the estimated difficulty of each class during training.

4. Quantitative Explainable AI

Grad-CAM is evaluated using:

- Deletion curves
- Insertion curves
- Random-order baseline comparison
- Paired Wilcoxon signed-rank statistical testing

⚙️ Technologies Used

- Python
- PyTorch
- Swin Transformer
- NumPy
- OpenCV
- Albumentations
- Matplotlib
- Scikit-learn
- Explainable AI (Grad-CAM)

📊 Experimental Results

The long-schedule model achieved the following results on 734 held-out test images:

Evaluation Metric| Performance
Accuracy| 90.87%
Macro F1-score| 91.24%
Sensitivity| 91.21%
Specificity| 97.69%

Ablation Study

- DCWA produced a small, statistically inconclusive improvement under the 16-epoch evaluation.
- ADFL reduced accuracy under the short training schedule.
- The contribution of both components requires further evaluation under matched long training schedules.

Explainability Results

Grad-CAM achieved better deletion AUC than random ordering:

- Grad-CAM deletion AUC: 0.466
- Random deletion AUC: 0.546
- Wilcoxon p-value: 4.6 × 10⁻¹⁶

Insertion evaluation showed weaker performance than random ordering, highlighting the importance of evaluating explainability through multiple metrics.

🔬 Key Contributions

- Content-dependent cross-window information exchange.
- Difficulty-aware adaptive loss function.
- Leakage-free cluster-wise dataset splitting.
- Quantitative evaluation of Grad-CAM against random explanations.
- Reproducible experimental evaluation.

🚀 Future Improvements

- Evaluate the model on additional cervical cytology datasets.
- Explore SHAP, LRP and Attention Rollout.
- Conduct experiments with longer, matched training schedules.
- Improve the schedule independence of ADFL.
- Perform external and clinical validation.

⚠️ Disclaimer

This project is intended for academic research and educational purposes. It is not a clinically validated diagnostic system and should not replace professional medical evaluation.

👩‍💻 Project Authors
- Lakshmi Prasanna Padala
- Malladi lasya sri priya

Department of Computer Science and Engineering
Sri Padmavati Mahila Visvavidyalayam (SPMVV), Tirupati, Andhra Pradesh, India.

---

Research Area: Artificial Intelligence | Machine Learning | Deep Learning | Medical Image Analysis | Explain
