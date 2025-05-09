# ADHD Diagnosis and Sex Prediction

## Project Overview
This project aims to predict ADHD diagnosis and sex using functional brain imaging and sociodemographic data. Through techniques such as graphic neural networks for fMRI data and boosting or random forest for tabular sociodemographic data, we seek to provide insight into the human brain and change how ADHD is diagnosed. The refined model is an XGNN model–an ensemble of XGBoost and GNN. 

## Prerequisites
```
pip3 install -r requirements.txt
```

## Dataset
The dataset folder can be downloaded directly from the Datathon's kaggle [here](https://www.kaggle.com/competitions/widsdatathon2025/data) (/data).

This challenge uses data provided by the Healthy Brain Network (HBN), a scientific initiative of the Child Mind Institute, and the Reproducible Brain Charts Project (RBC). The data was collected by encouraging the participation of families who have concerns about mental health or learning challenges in their children. As previously mentioned, one concern here is that there may not be enough data from patients who do not present any abnormal brain activity–this will be addressed later. 
The WiDS challenge provides a training folder (/data/TRAIN_NEW) that holds information regarding over 1,200 individuals. It includes the target information we wish to predict, which are the ADHD diagnosis and sex, functional MRI connectome matrices, and socio-demographic information. The latter includes the subject’s “handedness” or the parent’s education level, emotions, and other parenting information. All of the data consists of both quantitative and categorical metadata. 

## Model training and evaluation
The refined models, XGBoost and XGNN, are located in the notebooks "xgboost.ipynb", "xgnn_final_model.ipynb", respectively. The examples for training and the evaluation results are in it. To comprehensively evaluate our model’s performance, we used the following: Weighted F1 Score, AUC-ROC, and accuracy.

The baseline models are the GNN model and the Random Forest model located in the notebooks "gnn_notebook_pt3.ipynb" and "random_forest.ipynb", respectively.

# License
This project is licensed under the MIT License.

# References
1. I. Robertson, "8th Annual WiDS Datathon Challenges: Unraveling the Mysteries of the Female Brain," WiDS Worldwide, Jan. 7, 2025. Available: https://www.widsworldwide.org/get-inspired/blog/8th-annual-wids-datathon-challenges-unraveling-the-mysteries-of-the-female-brain/.
2. L. Wang, K. Li, and X. P. Hu, "Graph Convolutional Network for fMRI Analysis Based on Connectivity Neighborhood," Network Neuroscience, vol. 5, no. 1, pp. 83–95, 2021. DOI: https://doi.org/10.1162/netn_a_00171.
3. B. Allen, "Why Tree-Based Models Beat Deep Learning on Tabular Data," Geek Culture, Medium, Dec. 2023. Available: https://medium.com/geekculture/why-tree-based-models-beat-deep-learning-on-tabular-data-fcad692b1456.
4. M. P. Milham et al., "The ADHD-200 Consortium: A Model to Advance the Translational Potential of Neuroimaging in Clinical Neuroscience," Frontiers in Systems Neuroscience, vol. 6, 2012. Available: https://pmc.ncbi.nlm.nih.gov/articles/PMC4004765/.
5. N. L. Nussbaum, "ADHD and female-specific concerns: A review of the literature and clinical implications," J. Attention Disord., vol. 16, no. 2, pp. 87-100, 2011, doi: 10.1177/1087054711416909.
6. "ADHD in women: Misunderstood symptoms and treatment," ADDitude Magazine, Apr. 26, 2022. [Online]. Available: https://www.additudemag.com/adhd-in-women-misunderstood-symptoms-treatment
7. "ADHD in women: Why it's often misdiagnosed," Relational Psych, Sep. 7, 2023. [Online]. Available: https://www.relationalpsych.group/articles/adhd-in-women-why-its-often-misdiagnosed
8. Paul L. Morgan et al., "Sociodemographic Disparities in Attention-Deficit/Hyperactivity Disorder Overdiagnosis and Overtreatment During Elementary School," Journal of Learning Disabilities, vol. 56, no. 5, pp. 359-370, 2023. [Online]. Available: https://www.sciencedirect.com/science/article/abs/pii/S0165178123003438
9. Matthew Leming, John Suckling, “Deep learning for sex classification in resting-state and task functional brain networks from the UK Biobank” NeuroImage, Volume 241, 2021, https://doi.org/10.1016/j.neuroimage.2021.118409.
10. M. Leming, J. M. Górriz, and J. Suckling, "Ensemble deep learning on large, mixed-site fMRI datasets in autism and other tasks," International Journal of Neural Systems, vol. 30, no. 07, p. 2050012, Jan. 31, 2020. Available: https://doi.org/10.1142/S0129065720500124.

