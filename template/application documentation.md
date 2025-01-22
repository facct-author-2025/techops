# Application Documentation Template

## General Information

**Purpose and Intended Use**:
    
   - Description of the AI system's intended purpose, including the sector of deployment.
   - Clearly state the problem the AI application aims to solve.
   - Delineate target users and stakeholders.
   - Set measurable goals and key performance indicators (KPIs).
   - Consider ethical implications and regulatory constraints. 
   - Clear statement on prohibited uses or potential misuse scenarios.
   - **Operational environment:** Describe where and how the AI system will operate, such as on mobile devices, cloud platforms, or embedded systems.


## Risk classification

- High / Limited / Minimal (in accordance with the AI Act)
- reasoning for the above classification
   
## Application Functionality

- **Model Capabilities**:
    
    - What the application can and cannot do (limitations).
    - Supported languages, data types, or scenarios.

- **Input Data Requirements**:
    
    - Format and quality expectations for input data.
    - Examples of valid and invalid inputs.

- **Output Explanation**:
    
    - How to interpret predictions, classifications, or recommendations.
    - Uncertainty or confidence measures, if applicable.

- **System Architecture Overview**:
    
    - Functional description and architecture of the system.
    - Describe the key components of the system (including datasets, algorithms, models, etc.)

- **Data and Model Documentation integration**:
    
    - Logging of necessary data and model documentation and responsible contacts.


## Data Documentation

**Data Collection**:
- Define the orgin of the data (existing databases, APIs, or custom collection methods).
- How does the data represent the real-world context of the application?

<!-- color code here for data documentation elements that must be checked from the responsible stakeholder to avoid duplicates in documentation that are hard to maintain>
- **Data Documentation**:
- Define the types of data the model will process (e.g., images, text, time-series).
- Document the expected size, format, and quality of training datasets.
- Specify any preprocessing steps or feature engineering needed.
   - Clean and preprocess the data (e.g., handling missing values, normalisation).
    - Annotate and label data if required (for supervised learning).
    - Split the dataset into training, validation, and test sets.
   - Training dataset details


   **Data Cleaning**:
    
    - Handling missing values, duplicates, and outliers.
- **Normalisation/Standardisation**:
    
    - Scaling data to a specific range or standard deviation.
- **Encoding**:
    
    - Converting categorical data (e.g., one-hot, label encoding).
- **Transformation**:
    
    - Applying mathematical transformations (e.g., log, square root).
- **Augmentation**:
    
    - Expanding datasets with techniques like flipping images or paraphrasing text.
- **Anonymisation**:
    
    - Masking or pseudonymising sensitive data for privacy compliance.
- **Balancing**:
    
    - Addressing imbalanced datasets (e.g., oversampling, SMOTE).
- **Feature Selection/Removal**:
    
    - Criteria for keeping or removing features.
-->

## Model Development
 **Model Architecture**

- Describe the selected algorithms and architectures  (e.g., supervised, unsupervised, or reinforcement learning).
- **Hyperparameter Tuning Details**: List of chosen hyperparameters and their values, including justification for selection.
- **Training Logs**: Document the training process, including time, resources used, and any issues encountered (e.g., convergence).
- Describe the design and training of the model using the prepared data.
- Results of the  test and validatation the model's performance on separate datasets.
- Include diagrams or descriptions of key components and their interactions.
<!-- color code here for model documentation elements that must be checked from the responsible stakeholder to avoid duplicates in documentation that are hard to maintain>

## Model Validation and Testing
- **Assess the metrics of model performance** 
   - accuracy:
   - precision: 
   - recall:
   - F1 score:

- **Advanced performance metrics**
  - ROC-AUC:
    - trade-off between true positive rate and false positive rate
  - PR- AUC
     - Evaluating precision and recall trade-off
  - Specificity
    - (True Negatives/(True Negatives+False Positives))
  - Log Loss (Cross-Entropy Loss):
    - Penalises incorrect probabilities assigned to classes.


- **Context dependant metrics**: 
  - Regression Metrics: For tasks predicting continuous values
  - Clustering Metrics: for tasks grouping similar data points
  - Ranking Metrics: for tasks predicting rankings (e.g., search engines recommendation systems)
  - NLP processing metrics (e.g., text classification, sequence-to-sequence tasks)


- **Fairness Metrics**:
    
    - Ensure the model treats different groups (e.g., based on gender, race) equitably.
    - Examples: Demographic parity, equal opportunity, and disparate impact.
- **Explainability Metrics**:
    
    - Measure how understandable and interpretable are the model’s decisions.
    - Examples: Feature importance, fidelity (how well explanations match the model), and sparsity (using fewer features for explanations).
    - 
- **Robustness Metrics**:
    
    - Assess how well the model performs under challenging or unexpected conditions.
    - Examples: Adversarial robustness, performance under data drift, and sensitivity to input changes.
 
- Limitations of the performance after the tests
- Simulate deployment scenarios to understand real-world implications.
- Define thresholds for acceptable performance levels.
- Justify the choice of metrics based on the application’s purpose.
   
--> 

## Deployment
    
- Infrastructure and environment details (e.g., cloud setup, APIs).
- Integration with external systems or applications.



### Infrastructure and Environment Details

- **Cloud Setup**:
    - Specify cloud provider (e.g., AWS, Azure, GCP) and regions.
    - List required services: compute (e.g., EC2, Kubernetes), storage (e.g., S3, Blob Storage), and databases (e.g., DynamoDB, Firestore).
    - Define resource configurations (e.g., VM sizes, GPU/TPU requirements).
    - Network setup: VPC, subnets, and security groups.

- **APIs**:
    - API endpoints, payload structure, authentication methods (e.g., OAuth, API keys).
    - Latency and scalability expectations.


## Integration with External Systems

- **Systems**:
    - List dependencies 
    - Data flow diagrams showing interactions.
    - Error-handling mechanisms for APIs or webhooks

## Deployment Plan

- **Infrastructure**:
    
    - List environments: development, staging, production.
    - Resource scaling policies (e.g., autoscaling, redundancy).
    - Backup and recovery processes.
  
- **Integration Steps**:
    
    - Order of deployment (e.g., database migrations, model upload, service launch).
    - Dependencies like libraries, frameworks, or APIs.
    - Rollback strategies for each component.

 - **User Information**: where is this under deployment?


 ## Lifecycle Management
    
- Monitoring procedures for performance and ethical compliance.
- Versioning and change logs for model updates.

- **Metrics**:
    
    - Application performance: response time, error rate.
    - Model performance: accuracy, precision, recall.
    - Infrastructure: CPU, memory, network usage.

- **Key Activities**:

    - Monitor performance in real-world usage.
    - Identify and fix drifts, bugs, or failures.
    - Update the model periodically.
  
- **Documentation Needs**:
    - **Monitoring Logs**: Real-time data on accuracy, latency, and uptime.
    - **Incident Reports**: Record of failures, impacts, and resolutions.
    - **Retraining Logs**: Data updates and changes in performance.
    - **Audit Trails**: Comprehensive history of changes to ensure compliance.


### Risk Management System

<!--**Instructions:**  A thorough risk management system is mandated by the AI Act, especially for high-risk AI systems. This section documents the  proactive efforts to ensure the AI system operates safely and ethically.-->


**Risk Assessment Methodology:** Describe the frameworks or standards used to identify and assess risks, such as ISO 31000 or failure mode and effects analysis (FMEA), or NIST Risk Assessment Framework.

**Identified Risks:** 

**Potential Harmful Outcomes:** List possible negative effects, such as biased decisions, privacy breaches, or safety hazards.

**Likelihood and Severity:** Assess how likely each risk is to occur and the potential impact on users or society.

#### Risk Mitigation Measures:

**Preventive Measures:** Detail actions taken to prevent risks, like implementing data validation checks or bias reduction techniques.

**Protective Measures:** Describe contingency plans and safeguards in place to minimize the impact if a risk materializes.

## Testing and Validation (Accuracy, Robustness, Cybersecurity)

**Testing and Validation Procedures (Accuracy):**

**Performance Metrics:** List the metrics used to evaluate the AI system, such as accuracy, precision, recall, F1 score, or mean squared error.

**Validation Results:** Summarize the outcomes of testing, including any benchmarks or thresholds met or exceeded.

**Measures for Accuracy:** High-quality data, algorithm optimisation, evaluation metrics, and real-time performance tracking.

  
#### Accuracy throughout the lifecycle:

**Data Quality and Management:** High-Quality Training Data: Data Preprocessing, techniques like normalisation, outlier removal, and feature scaling to improve data consistency, Data Augmentation, Data Validation

**Model Selection and Optimisation:** Algorithm selection suited for the problem, Hyperparameter Tuning (grid search, random search, Bayesian optimization), Performance Validation( cross-validation by splitting data into training and testing sets, using k-fold or stratified cross-validation), Evaluation Metrics (precision,recall, F1 score, accuracy, mean squared error (MSE), or area under the curve (AUC).

**Feedback Mechanisms:** Real-Time Error Tracking, Incorporate mechanisms to iteratively label and include challenging or misclassified examples for retraining.

#### Robustness 

**Robustness Measures:**
- Adversarial training, stress testing, redundancy, error handling, and domain adaptation.

**Scenario-Based Testing:**
- Plan for adversarial conditions, edge cases, and unusual input scenarios.
    
- Design the system to degrade gracefully when encountering unexpected inputs.
    

**Redundancy and Fail-Safes:**
    
- Introduce fallback systems (e.g., rule-based or simpler models) to handle situations where the main AI system fails.
    
**Uncertainty Estimation:**
    
- Include mechanisms to quantify uncertainty in the model’s predictions (e.g., Bayesian networks or confidence scores).
    

#### Cybersecurity 

**Data Security:**

**Access Control:**

**Incident Response :**


These measures include threat modelling, data security, adversarial robustness, secure development practices, access control, and incident response mechanisms.

Post-deployment monitoring, patch management, and forensic logging are crucial to maintaining ongoing cybersecurity compliance.

Documentation of all cybersecurity processes and incidents is mandatory to ensure accountability and regulatory conformity.

  

## Human Oversight 

**Human-in-the-Loop Mechanisms:**  Explain how human judgment is incorporated into the AI system’s decision-making process, such as requiring human approval before action.

**Override and Intervention Procedures:** Describe how users or operators can intervene or disable the AI system in case of errors or emergencies.

**User Instructions and Training:** Provide guidelines and training materials to help users understand how to operate the AI system safely and effectively.

**Limitations and Constraints of the System:** Clearly state what the AI system cannot do, including any known weaknesses or scenarios where performance may degrade.



## Incident Management
<!-- what happens when things go wrong -->
- **Common Issues**:
    
    - List common errors and their solutions.
    - Logs or debugging tips for advanced troubleshooting.

- **Support Contact**:
    
    - How to reach technical support or community forums.


### Troubleshooting AI Application Deployment

This section outlines potential issues that can arise during the deployment of an AI application, along with their causes, resolutions, and best practices for mitigation.


#### Infrastructure-Level Issues

##### Insufficient Resources
- **Problem**: Inaccurate resource estimation for production workloads.
  - Unexpected spikes in user traffic can lead to insufficient resources such as compute, memory or storage that can lead to crashes and bad performance

- **Mitigation Strategy**:
<!-- describe here the resolution strategy such as:
-  Enable autoscaling (e.g., Kubernetes Horizontal Pod Autoscaler).
  - Monitor usage metrics and adjust resource allocation dynamically.
  - Implement rate-limiting for traffic spikes. -->


##### Network Failures
- **Problem**:  network bottlenecks  can lead to inaccessible or experiences latency of the application.

- **Mitigation Strategy**:
<!-- 
  - Test network connectivity 
  - Use content delivery networks (CDNs) or regional load balancers.
  - Ensure proper failover mechanisms.-->


##### Deployment Pipeline Failures
- **Problem**: pipeline fails to build, test, or deploy because of issues of compatibility between application code and infrastructure, environment variables or credentials misconfiguration.

- **Mitigation Strategy**: 
<!--:
  - Roll back to the last stable build.
  - Fix pipeline scripts and use containerisation for environment consistency.
  - Enable verbose logging for error diagnostics.-->


#### Integration Problems

##### API Failures
- **Problem**: External APIs or internal services are unreachable due to network errors or authentication failures.

- **Mitigation Strategy**:
<!--:
  - Implement retries with exponential backoff.
  - Validate API keys or tokens and refresh as needed.
  - Log and monitor API responses for debugging. -->

##### Data Format Mismatches
- **Problem**: Crashes or errors due to unexpected data formats such as changes in the schema of external data sources or missing data validation steps.

- **Mitigation Strategy**: 

<!-->
  - Use schema validation tools (e.g., JSON schema validators).
  - Add versioning to APIs and validate inputs before processing.-->

#### Data Quality Problems
- **Problem**: Inaccurate or corrupt data leads to poor predictions.
- **Causes**:
  - No data validation or cleaning processes.
  - Inconsistent labelling in training datasets.

- **Mitigation Strategy**: 
<!--
- **Resolution**:
  - Automate data quality checks (e.g., Great Expectations framework).
  - Regularly audit and clean production data.-->


#### Model-Level Issues

#####  Performance or Deployment Issues
- **Problem**: Incorrect or inconsistent results due to data drift or inadequate training data for the real world deployment domain. 

- **Mitigation Strategy**:

<!--
- **Resolution**:
  - Monitoring for data drift and retraining of the model as needed.
  - Regularly update the model -->


#### Safety and Security Issues

##### Unauthorised Access
- **Problem**: Sensitive data or APIs are exposed due to misconfigured authentication and authorization.

##### Data Breaches
- **Problem**: User or model data is compromised due to insecure storage or lack of monitoring and logging of data access. 

- **Mitigation Strategy**: 
<!--
- **Resolution**:
  - Use secure storage services (e.g., AWS KMS).
  - Implement auditing for data access and alerts for unusual activity.
  6.1. Delayed or Missing Data-->


#### Monitoring and Logging Failures

##### Missing or Incomplete Logs
- **Problem**: Lack of information to debug issues due to inefficient logging. Critical issues go unnoticed, or too many false positives occur by lack of implementation ofactionable information in alerts. 

- **Mitigation Strategy**: 


<!--
- **Resolution**:
  - Fine-tune alerting thresholds and prioritise critical alerts.
  - Use tools like Prometheus Alertmanager to manage and group alerts. -->


#### Recovery and Rollback

##### Rollback Mechanisms
- **Problem**: New deployment introduces critical errors.

- **Mitigation Strategy**: 

<!--
- **Resolution**:
  - Use blue-green or canary deployments to minimise impact.
  - Maintain backups of previous versions and configurations. -->

##### Disaster Recovery
- **Problem**: Complete system outage or data loss.

- **Mitigation Strategy**:

<!--
- **Resolution**:
  - Test and document disaster recovery plans.
  - Use automated backups and verify restore procedures.-->
