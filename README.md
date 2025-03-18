# **Teacher Feedback Actionability Classification**

This repository contains code for a research project focused on classifying teacher feedback as either "actionable" or "vague." The system uses RoBERTa fine-tuning to identify feedback that provides clear, specific, and implementable guidance versus feedback that is vague.

## **Project Overview**
We developed a machine learning system that can automatically identify actionable feedback in classroom observations of teachers. The model achieves strong performance (93% accuracy in cross-validation) and provides insights into the linguistic characteristics that distinguish actionable from vague feedback.

## **Data**

1. ~750 hand-annotated examples of teacher feedback with gold-standard "actionable" or "vague" labels
2. Feedback collected across grades 1-5 in English and math classrooms from Sierra Leone, Liberia and Ghana
3. Additional metadata including grade level, subject, and classroom environment ratings

## **Model**

1. Fine-tuned RoBERTa-base model using 5-fold cross-validation
2. Trained with early stopping and optimized for precision
3. SHAP (SHapley Additive exPlanations) analysis to identify important linguistic features

## **Repository Structure**

1. 'traindata.csv' - Annotated dataset used for model training and evaluation; available upon request (data privacy concerns)
2. 'Actionability_Classification_Teacher_Feedback.ipynb' - Notebook containing model training, evaluation, prediction, and SHAP analysis

## **Limitations**
Our study has several limitations and opportunities for future work. First, with only ~750 hand-annotated instances, our dataset may not capture the full diversity of teacher feedback, potentially leading to overfitting or limited generalizability. Second, our findings may be constrained to the specific educational context studied (Grades 1-5, English and Math) and may not extend to other grade levels, subjects, or settings like higher education or special education. Third, our model was trained on feedback written in English within a specific cultural context, whereas patterns of actionability likely differ across linguistic and cultural settings. Fourth, our feature analyses provide correlational rather than causal insights – we cannot definitively claim that specific linguistic features cause feedback to be more actionable.
Ethics Statement

## **Potential Misuse:** 
1. Our model for classifying teacher feedback could potentially be misused in high-stakes evaluation contexts, leading to automated assessment of teacher performance without appropriate human oversight. We explicitly discourage using this system for formal teacher evaluation or as a sole determinant of professional advancement. The system is designed as a reflective tool for professional development, not an evaluative instrument.
2. The system should supplement rather than replace human judgment in professional development contexts. The model lacks the holistic understanding that experienced educators bring to feedback interpretation. Educational coaches and mentors should use these insights as conversation starters rather than definitive judgments about feedback quality. Maintaining this human-in-the-loop approach ensures that contextual nuances, relationship dynamics, and individual teacher development needs remain central to the feedback improvement process.
