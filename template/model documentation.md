# Model Documentation Template
<!-- info: Replace with model name -->

## Overview

### Model Type
**Model Type:** (e.g., Neural Networks, Decision Trees, etc.)

### Model Description
* Description
<!-- info: Brief (max 200 words) description of the model architecture and the task(s) it was trained to solve. -->

### Status
<!-- scope: telescope -->
<!-- info: Select **one:** -->
**Status Date:** YYYY-MM-DD

**Status:** _specify one of_:

* **Under Preparation** -- The model is still under active development and is not yet ready for use due to active "dev" updates.
* **Regularly Updated** -- New versions of the model have been or will continue to be made available.
* **Actively Maintained** -- No new versions will be made available, but this model will be actively maintained.
* **Limited Maintenance** -- The model will not be updated, but any technical issues will be addressed.
* **Deprecated** -- This model is obsolete or is no longer being maintained.

### Relevant Links
<!-- info: User studies show document users find quick access to relevant artefacts like papers, model demos, etc..
very useful. -->

Example references:

- GitHub Repository
- Paper/Documentation Link
- Initiative Demo
- Conference Talk
- API Link

### Developers
- **Name, Team**
- **Name, Team**

### Owner
<!-- info: Remember to reference developers and owners emails. -->
- **Team Name, Contact Person**

## Version Details and Artifacts
<!-- scope: periscope -->
<!-- info: Provide details about the current model version
and which model version the current model card corresponds to.

For models without version number, use "Not currently tracked"
but be sure to track the release date of the model.
-->
**Current Model Version:**

**Model Version Release Date:**

**Model Version at last Model Documentation Update:**

**Artifacts:**


- Model weights (e.g. S3 bucket path)
- Model config (e.g. S3 bucket path)

## Intended and Known Usage
### Intended Use
<!-- info: This section focuses on the initial purpose and/or reasoning
for creating the model.-->

* Description

### Domain(s) of use
* Description

**Specific tasks performed:**

### Out Of Scope Uses
Provide potential applications and/or use cases for which use of the model is not suitable.

### Known Applications
<!-- info: Fill out the following section if the model has any
current known usages.
-->

| **Application**   | **Purpose of Model Usage**                                                 | **[AI Act Risk](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai)** |
|-------------------|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [Application 1]() | Foundation model providing customer embeddings for fraud detection scoring | High                                                                                         |
| [Application 2]() | Customer embeddings used directly as features for recommendation engine    | Limited                                                                                      |

Note, this table may not be exhaustive.  Model users and documentation consumers at large
are highly encouraged to contribute known usages.

## Model Architecture

- Architecture Description

- Key components
    
- Hyperparameters

- Training Methodology

- Training duration
    
- Compute resources used
    

### Data Collection and Preprocessing

<!--check data documentation to avoid duplicates of information-->

- **Steps Involved**:
    - Data collection: Describe how the data was sourced (e.g., databases, APIs, sensors, or publicly available datasets).
    - Data cleaning: Explain techniques used to handle missing values, outliers, or errors.
        
    - Data transformation: Include any scaling or encoding applied.


       
### Data Splitting

* **Subset Definitions**:
    * **Training set**: 
    * **Validation set**: 
    * **Test set**: 
* **Splitting Methodology**:
    * Describe the approach:
        * **Random Sampling**: 
        * **Stratified Sampling**: 
        * **Temporal Splits**: 
* **Proportions**:
    * Example: "70% training, 20% validation, 10% testing."
* **Reproducibility**:
    * Mention how many seeds are being used and how many are needed to prove statistical significance
    
    

**Data Shuffling**:

- Shuffle applied: (Yes/No) 

### Model Training Process

**Details of Processes**:

- **Initialisation**: 
- **Loss Function**:
- **Optimiser**:
- **Hyperparameters**:
        
### Model Validation:
    
- Model predictions on the validation set are evaluated.
- Performance metrics (e.g., accuracy, F1 score, RMSE) are monitored.
- Overfitting is detected using validation loss trends.
    

### Performance Metrics

- Evaluation Metrics Used (e.g., Accuracy, Precision, Recall, AUC-ROC)
- Benchmarking Results
- Validation Process
- Real-World Performance
- Stress testing
- Performance across different environments and populations

**Hyperparameter Tuning**:
    

        
**Regularisation**:
    

    
**Early Stopping**:
    

## Model Testing

### Technical Processes

 **Performance Metrics**:
    
 - Compute metrics on the test set:
     - Accuracy, precision, recall, F1 score for classification.
    - MSE, RMSE, MAE for regression.

 **Confusion Matrix**:
    
- Generate a confusion matrix to evaluate classification results.

 **ROC Curve and AUC**:
    
- For binary classifiers, compute the ROC curve and Area Under the Curve (AUC).

 **Feature Importance**:
    
- Analyse feature contributions (for explainability).

 **Robustness Testing**:

- Test the model on edge cases or adversarial examples.

 **Comparison to Baselines**:
    
- Compare the model’s performance to a simple baseline (e.g., random guess, mean prediction).

### Model Bias and Fairness Analysis

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXclauxwg1nWuPj2z0TcgUK9y69AqHzk_-jQ5BJwYeDkjPSOLVddFcHJ6-oOiuZ2p4Rk3VpqyKw9CvU7N1LOqYtpdjN6CV_hhTxTtpNj4auLmqhsaIQ5fRLIPnVpZOnhtR63YNELlg?key=Lv0_1kRp5_LSkJabUJ8gjQ)Implicit Bias, Measurement Bias, Temporal Bias, Selection Bias, Confounding Bias

#### Bias Detection Methods Used
    

**Pre-processing:** Resampling, Reweighting,Transformation (data imputation, changing order of data); Relabeling, Blinding
    
**In-processing:** Transfer learning, Reweighting, Constraint optimization, Adversarial Learning, Regularization, Bandits
    
**Post-processing:** Transformation, Calibration, Thresholding
    


**Results of Bias Testing:**
    

#### Mitigation Measures
    

**Fairness adjustments:** Introduce fairness criteria (like demographic parity, equal opportunity, or equalized odds) into the model training process. 
    
**Adversarial Debiasing:** Use adversarial networks to remove biased information during training. The main model tries to make accurate predictions, while an adversary network tries to predict sensitive attributes from the model's predictions.
    

#### Retraining approaches

**Fairness Regularization:** Modify the model's objective function to penalize bias. This introduces regularization terms that discourage the model from making predictions that disproportionately affect certain groups.
    
**Fair Representation Learning:** Learn latent representations of the input data that remove sensitive attributes, ensuring that downstream models trained on these representations are fair.
    
### Post-Processing Techniques

**Fairness-Aware Recalibration:** After the model is trained, adjust decision thresholds separately for different demographic groups to reduce disparities in false positive/false negative rates.
    
**Output Perturbation:** Introduce randomness or noise to model predictions to make outcomes more equitable across groups.
    
**Fairness Impact Statement:** Explain trade-offs made to satisfy certain fairness criterias
    

## Model Interpretability and Explainability

**Explainability Techniques Used:**
    

- Shapley values, LIME, etc.
    
**Post-hoc Explanation Models**

- Feature Importance, Permutation Importance, SHAP (SHapley Additive exPlanations), LIME (Local Interpretable Model-agnostic Explanations):
- Partial Dependence Plots (PDP) 
- Counterfactual Explanations
- Surrogate Models
- Attention Mechanisms (for Deep Learning)
    

**Model-Specific Explanation Techniques**

- Grad-CAM (Gradient-weighted Class Activation Mapping)
- Layer-wise Relevance Propagation (LRP)
- TreeSHAP (SHAP for Decision Trees)
    

How interpretable is the model’s decision-making process?

Some technical tools that can aid transparency include:

- Data Lineage Tools: Track the flow and transformation of data (e.g., Apache Atlas, Pachyderm).
- Explainability Libraries: SHAP, LIME, Captum, TensorFlow Explain.
- Model Debugging Tools: What-If Tool, IBM AI Explainability 360.
- Version Control Systems: Git, DVC (Data Version Control) for datasets and models.

## Documentation Metadata
### Version
<!-- info: provide version of this document, if applicable (dates might also be useful) -->

### Template Version
<!-- info: link to model documentation template (i.e. could be a GitHub link) -->

### Documentation Authors
<!-- info: Give documentation authors credit

Select one or more roles per author and reference author's
emails to ease communication and add transparency. -->

- **Name, Team:** (Owner / Contributor / Manager)
- **Name, Team:** (Owner / Contributor / Manager)
- **Name, Team:** (Owner / Contributor / Manager)