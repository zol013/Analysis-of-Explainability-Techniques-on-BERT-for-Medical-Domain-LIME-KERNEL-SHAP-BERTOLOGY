# Analysis-of-Explainability-Techniques-on-BERT-for-Medical-Domain

In this work, we aim to experiment with variety of interpretability approaches on deep learning models trained for a classification task in the medical domain. We believe such work could contribute significantly to the AI for healthcare industry and increase the trust for usage of these models in high stake industries. We particularly focus on the Post-Hoc analysis of the model and we would like to acknowledge the survey paper [Post-hoc Interpretability for Neural NLP: A Survey](https://dl.acm.org/doi/pdf/10.1145/3546577) for providing key insights into the problem. 

Interpretability approaches can be categorized broadly into two approaches: intrinsic and extrinsic. In intrinsic approaches, the model's own architecture generates explanations. In extrinsic or post-hoc approaches, the model is explained by analyzing its outputs. In this work our focus is exclusively on post-hoc approaches in medical NLP. Post-hoc approaches are often more practical than task-dependent intrinsic approaches because they are model-agnostic, treating the model as a black box and using its outputs to generate explanations. However, post-hoc methods are sometimes criticized for providing misleading explanations of models that are fundamentally unexplainable. In this study, we have worked on diverse set of post-hoc methods using a fine tuned pre-trained BERT based model, and assessed the strengths and weaknesses of each method.

This work was submitted as the final project for the course CSE 256: Statistical NLP at University of California San Diego. 

### Dependency Installation
1. Clone the repo
   ```sh
   git clone https://github.com/PrasannaKumaran/Analysis-of-Explainability-Techniques-on-BERT-for-Medical-Domain.git
   ```
   For accounts that are SSH configured
   ```sh
    git clone git@github.com:PrasannaKumaran/Analysis-of-Explainability-Techniques-on-BERT-for-Medical-Domain.git
   ```
2. Install pip
   ```sh
   python -m pip install --upgrade pip
   ```
3. Create and Activate Virtual Environment (Linux)
   ```sh
   python3 -m venv [environment-name]
   source [environment-name]/bin/activate
   ```
4. Install dependencies
   ```sh
   pip install -r requirements.txt
   ```
## Model and Dataset
- For this work we have used the kaggle medical transcription dataset and we have fine tuned a pre-trained BERT based model. We have used the [BioBERT](https://arxiv.org/abs/1901.08746) and fine tuned it for 100 epochs by freezing last few layers. We have considered using the model state after 16 epochs since the performance of the model begins to drop as shown in Figure 
<p align="center">
  <img src="./images/report data/accuracyPlot.png" width="200">
</p>. 

## Experiments
We implemented multiple methods including SHAP, LIME, Integrated Gradients, Adversarial and Counterfactual examples, Vocabulary and Bertology. The implementation can be found in the corresponding ipynb notebook. 

## Authors 

[Prasannakumaran D](http://github.com/PrasannaKumaran), [Ashwin Muralidharan](https://github.com/ashwinmd), [Zongze Liu](https://github.com/zol013), [Pranav Khanna](https://github.com/kpranav1998)
