**Teacher Feedback Actionability Classification**

This repository contains code and resources for a research project focused on classifying teacher feedback as either "actionable" or "vague" using machine learning. The system uses RoBERTa fine-tuning to identify feedback that provides clear, specific, and implementable guidance versus feedback that is general and less directed.

**Project Overview**
We developed a machine learning system that can automatically identify actionable feedback in classroom observations of teachers. The model achieves strong performance (93% accuracy in cross-validation) and provides insights into the linguistic characteristics that distinguish actionable from vague feedback.
Data

~750 hand-annotated examples of teacher feedback with gold-standard "actionable" or "vague" labels
Feedback collected across grades 1-5 in English and math classrooms
Additional metadata including grade level, subject, and classroom environment ratings

Model

Fine-tuned RoBERTa-base model using 5-fold cross-validation
Trained with early stopping and optimized for F1 score
SHAP (SHapley Additive exPlanations) analysis to identify important linguistic features

Repository Structure

traindata.csv - Annotated dataset used for model training and evaluation
Actionability_Classification_Teacher_Feedback.ipynb - Notebook containing model training, evaluation, prediction, and SHAP analysis

Results
Our model achieves:

93% accuracy across 5-fold cross-validation
Strong performance across different grades and subjects
Robust identification of linguistic features that mark actionable feedback

Key Findings
SHAP analysis revealed several distinctive linguistic patterns:

Actionable feedback tends to contain more specific directives, numbers, and action verbs
Vague feedback is characterized by more general descriptions and fewer concrete suggestions
Feedback length and linguistic complexity are significantly different between the two classes

Getting Started
Prerequisites
Copytorch
transformers
datasets
sklearn
numpy
pandas
matplotlib
seaborn
shap
tqdm
Using the Notebook
The Actionability_Classification_Teacher_Feedback.ipynb notebook contains multiple sections:

Data Preprocessing & Exploration: Prepare and explore the dataset
Model Training: Fine-tune RoBERTa using 5-fold cross-validation
Model Evaluation: Evaluate performance and visualize results
Prediction: Apply the trained model to new data
SHAP Analysis: Interpret model predictions using SHAP values

Limitations
Our study has several limitations and opportunities for future work. First, with only ~750 hand-annotated instances, our dataset may not capture the full diversity of teacher feedback, potentially leading to overfitting or limited generalizability. Second, our findings may be constrained to the specific educational context studied (Grades 1-5, English and Math) and may not extend to other grade levels, subjects, or settings like higher education or special education. Third, our model was trained on feedback written in English within a specific cultural context, whereas patterns of actionability likely differ across linguistic and cultural settings. Fourth, our feature analyses provide correlational rather than causal insights – we cannot definitively claim that specific linguistic features cause feedback to be more actionable.
Ethics Statement

Potential Misuse: Our model for classifying teacher feedback could potentially be misused in high-stakes evaluation contexts, leading to automated assessment of teacher performance without appropriate human oversight. We explicitly discourage using this system for formal teacher evaluation or as a sole determinant of professional advancement. The system is designed as a reflective tool for professional development, not an evaluative instrument.
Human in the Loop: The system should supplement rather than replace human judgment in professional development contexts. The model lacks the holistic understanding that experienced educators bring to feedback interpretation. Educational coaches and mentors should use these insights as conversation starters rather than definitive judgments about feedback quality. Maintaining this human-in-the-loop approach ensures that contextual nuances, relationship dynamics, and individual teacher development needs remain central to the feedback improvement process.
