🚀 GDG ML Wing — Commit Role Classification






This project explores the use of machine learning for commit role classification, where software commits are automatically categorized as Frontend, Backend, or Fullstack.


The motivation for this work is that in real-world development teams, commit histories are massive, and manually identifying the role of a contribution is inefficient. Automating this classification can support developer analytics, task allocation, and contribution tracking.


We evaluated three different machine learning models — K-Nearest Neighbors (KNN), Support Vector Machine (SVM), and Logistic Regression (LR) — to determine the best-performing approach.


📂 Dataset


The dataset used consists of 1,500 commits. Each entry includes:


Commit Message — natural language description of changes


File Extensions Modified — e.g., .js, .css, .html


Commit Type — feature, bugfix, refactor, etc.


Lines Added/Deleted — numerical features capturing code changes


Time of Commit — contextual metadata


Role Label — Frontend, Backend, or Fullstack (target variable)


This combination of textual, structural, and numerical features provided a rich foundation for training classification models.


🤖 Model Development


Baseline: KNN (48% accuracy)


Chosen for simplicity and as a starting point.


Failed to capture patterns due to high-dimensional space and noise sensitivity.


Intermediate: SVM (85% accuracy)


Selected for its margin-based decision boundary and robustness in feature space.


Showed strong generalization, though computationally heavier.


Final: Logistic Regression (96% accuracy)


Despite its simplicity, it outperformed others with excellent accuracy.


Provided interpretability (weights for features) and strong convergence.


Best balance of accuracy, interpretability, and efficiency.


📊 Results & Interpretation


Model	Accuracy	Notes


KNN (Baseline)	48%	Struggled with noisy neighbors and overlapping classes.


SVM (Middle Model)	85%	Strong separation but slightly weaker on rare cases.


Logistic Regression	96% ✅	Best performance, interpretable, and production-ready.



Key Takeaways:


Accuracy alone is not the only factor: LR was also the most computationally efficient.


KNN proved unsuitable for this dataset size and structure.


SVM was strong but less interpretable compared to LR.


📘Deliverables


This repository provides the following outputs:


Evaluation Report (≤ 2 pages)


Summarizes model performance, error analysis, and lessons learned.


Annotated Examples


Ten real commits from the dataset are annotated in plain language with clear justifications for their labels.


Reflection (≤ 300 words)


Explains the most important design decisions made in model selection and evaluation.


🌱 Lessons Learned


Starting with a baseline model helps in quantifying improvements.


Feature scaling had a strong effect on SVM and LR.


Sometimes simpler models (like LR) can outperform more complex ones.


Error analysis highlighted issues with minority class misclassifications.


🔮 Future Work


Extend dataset to include larger commit histories across diverse projects.


Apply ensemble models (Random Forest, XGBoost) to test improvements.


Explore deep learning approaches (e.g., BERT on commit messages).


Handle class imbalance using resampling or cost-sensitive learning.


Build a deployment pipeline (e.g., Flask/FastAPI) for real-time commit role classification.

