# WiDS-Datathon-2025
Unraveling the Mysteries of the Female Brain: Sex Patterns in ADHD

# Exploratory Data Analysis (EDA)
---
The first and most crucial step in approaching predictive modeling is conducting exploratory data analysis (EDA) to gain a clear understanding of the dataset. EDA helps reveal patterns, relationships, and potential issues in the data, guiding the entire modeling process. The structure and complexity of an EDA pipeline can vary depending on the specific problem and dataset, with differences in the number of steps and the depth of analysis required. By tailoring the EDA approach to the problem at hand, we can ensure more accurate and effective predictive models.

### 1. Understanding the Problem and Data

### Research Question: 
Can we build a model that predicts an individual's sex and ADHD diagnosis using functional brain imaging data of children and adolescents and their socio-demographic, emotions, and parenting information? 

### Data
The training folder train_tsv consists of three types of information about the 1,200+ subjects:

a) the targets (ADHD diagnosis and sex)
b) functional MRI connectome matrices
c) socio-demographic information, e.g., subject’s “handedness” or “parent’s education level”, emotions (“Strength and Difficulties Questionnaire”), and parenting information (“Alabama Parenting Questionnaire”). These include both quantitative and categorical metadata.

The test folder test_tsv consists of unseen data frames for 300+ subjects. These data frames are as follows:

a) functional MRI connectome matrices
b) socio-demographic, emotions, and parenting information

