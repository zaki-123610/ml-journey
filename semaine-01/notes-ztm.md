# ML Framework (ZTM) — 6 steps

## 1. Problem definition
What exactly do we want to predict? Do we even need ML, or would a simple rule work?
- Supervised learning: we have examples with the right answer
  - Classification: predict a category (heart disease: yes / no)
  - Regression: predict a number (the price of a house)
- Unsupervised learning: no answers, we look for groups (cluster customers by behavior)

Example: predict if a patient has heart disease → supervised, classification.

## 2. Data
What data do we have?
- Structured: tables with rows and columns (a CSV of patients: age, cholesterol...)
- Unstructured: text, images, audio (DocuMind documents, X-ray images)

Example: a table of 300 patients → structured data.

## 3. Evaluation
Before training, define a metric and a target number, so we know when the model is good enough.
- No model is perfect: the goal is "good enough for the use case", not 100%.
- Choose the right metric: accuracy is misleading when classes are unbalanced (1% fraud).

Example: "If we reach 95% accuracy on patients the model has never seen, we continue the project."

## 4. Features
Features are the input information (the columns) we give the model.
The target is what we want to predict. The model finds the patterns between features and target.
- Numerical: age, cholesterol
- Categorical: sex, type of chest pain
- Derived (feature engineering): a new column built from others (BMI from weight and height)

Example: features = age, sex, cholesterol, blood pressure → target = heart disease (yes / no).

## 5. Modelling
Choose a model adapted to the problem and the data, then train it.
- Split the data: training (~70-80%), validation (~10-15%), test (~10-15%)
- Training score much higher than test score = overfitting

Example: train a classification model on the patient data and check its score on the test set.

## 6. Experimentation
A loop: change one thing, measure again, keep what improves the result.
We can go back to any previous step (more data, new features, another model).

Example: DocuMind — switching from ChromaDB to pgvector raised the retrieval hit rate from 87.5% to 93.8%.
