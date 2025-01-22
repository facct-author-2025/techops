# Data Documentation Template
<!-- info: Replace with dataset name -->

## Overview

### Dataset Description
Write a short summary describing your dataset (limit
200 words). Include information about the content
and topic of the data, sources and motivations for the
dataset, benefits and the problems or use cases it is
suitable for. For readers that only take 10 seconds to look
at this data card, adding one good overview image might also
make the difference between this data being discovered
and going unnoticed.

For more tips on describing data, see Zalando Data Foundation's
[Quality of Data Descriptions](https://docs.google.com/document/d/1njN1HMnNUl2J3aaY99FMwdJrSp0eMPsTY_cgOSsh46U)!<!-- info: Brief (max 200 words) description of the model architecture and the task(s) it was trained to solve. -->

### Status
<!-- scope: telescope -->
<!-- info: Select **one:** -->
**Status Date:** YYYY-MM-DD

**Status:** _specify one of_:

* **Under Preparation** -- The dataset is still under active curation and is not yet ready for use due to active "dev" updates.
* **Regularly Updated** -- New versions of the dataset have been or will continue to be made available.
* **Actively Maintained** -- No new versions will be made available, but this dataset will be actively maintained, including but not limited to updates to the data.
* **Limited Maintenance** -- The data will not be updated, but any technical issues will be addressed.
* **Deprecated** -- This dataset is obsolete or is no longer being maintained.

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

## Dataset Characteristics
**Data Types:** (e.g., images, text, audio, structured, unstructured data)
**Size/Volume:**
**Number of Instances/Records:**
**Primary Use Case(s):** Description of the main AI use cases that the dataset was designed for or is typically used in.
**Associated AI System(s):** List known AI system(s) that this dataset is or has been used in.
**Number of Features/Attributes (if applicable):**
**Label Information (if applicable):**
**Geographical Scope:** Geographic location(s) where the data was collected.
**Date of Collection:** Start and end date of data collection.

## Data Origin and Source
**Source(s):** Provide information about where the data was sourced from (e.g., sensors, surveys, web scraping, public databases).
**Third-Party Data:** Indicate if any part of the dataset was obtained from third parties, and if so, detail the legal agreements in place (license, usage rights, etc.).
**Ethical Sourcing:** (Ghana issues) Provide information on the ethical and legal compliance of the data collection process (e.g., informed consent, transparency to data subjects, and compliance with GDPR or other regulations).

## Provenance
_Describe the history and origin of the data._
### Collection
#### Method(s) Used
<!-- scope: telescope -->
<!-- info: Select **all applicable** methods used to collect data.

Note on crowdsourcing, this covers the case where a crowd labels data
(make sure the reference the [Annotations and Labeling](#annotations-and-labeling)
section), or the case where a crowd is responsible for collecting and
submitting data independently to form a collective dataset.
-->
_Specify one or more of:_
- API
- Artificially generated
- Crowdsourced - Internal Employee
- Crowdsourced - External Paid
- Crowdsourced - Volunteer
- Vendor collection efforts
- Scraped or crawled
- Survey, forms, or polls
- Interviews, focus groups
- Scientific experiment
- Taken from other existing datasets
- Unknown
- To be determined
- Others (please specify)

#### Methodology Detail(s)
<!-- scope: periscope -->
<!-- info: Provide a description of each collection method used.

Use additional notes to capture any other relevant information or
considerations.

(Usage Note: Duplicate and complete the following for collection method
type.) -->
**Collection Type**

**Source:** Describe here. Include links where available.

**Platform:** [Platform Name], Describe platform here. Include links where relevant.

**Is this source considered sensitive or high-risk?** [Yes/No]

**Dates of Collection:** [YYYY-MM -- YYYY-MM]

**Update Frequency for collected data:**

*Select one for this collection type:* yearly, quarterly, monthly, on demand, no changes, others, ....

**Additional Links for this collection:**

See section on [Access, Rention, and Deletion](#access-retention-and-deletion)

**Additional Notes:** Add here

#### Source Description(s)
<!-- scope: microscope -->
<!-- info: Provide a description of each upstream source of data.

Use additional notes to capture any other relevant information or
considerations. -->
- **Source:** Describe here. Include links, data examples, metrics, visualizations where relevant.
- **Source:** Describe here. Include links, data examples, metrics, visualizations where relevant.
- **Source:** Describe here. Include links, data examples, metrics, visualizations where relevant.

**Additional Notes:** Add here

#### Collection Cadence
<!-- scope: telescope -->
<!-- info: Select **all applicable**: -->
**Static:** Data was collected once from single or multiple sources.

**Streamed:** Data is continuously acquired from single or multiple sources.

**Dynamic:** Data is updated regularly from single or multiple sources.

**Others:** Please specify
    
## Data Pre-Processing
_Note: not all below sections are relevant for each data set._

### Data Cleaning
- Handling missing data: (e.g., removal, imputation method used)
- Outlier treatment: (e.g., detection and removal technique)
- Duplicates removal: (Yes/No)
- Error correction: (Manual/Automated, if applicable)

### Data Transformation
- Normalization/Standardization: (Method used, e.g., min-max scaling)
- Encoding categorical data: (e.g., one-hot encoding, label encoding)
- Text/tokenization: (Applicable for NLP tasks)

### Feature Engineering
- Feature selection: (e.g., methods used to select features)
- Feature extraction: (e.g., PCA, interaction terms)
- Newly created features: (List any)

### Dimensionality Reduction
- Technique(s) used: (e.g., PCA, t-SNE)
- Number of dimensions after reduction: (Specify)

### Data Augmentation
- Augmentation technique(s): (e.g., rotation, flipping for images)

## Data Annotation and Labeling 
- Annotation Process: Describe the process used to label or annotate the data (e.g., human labelers, automated, crowdsourcing).
- Quality Assurance: Explain any quality control mechanisms applied to ensure accurate labeling or annotation.
- Inter-Annotator Agreement: If applicable, mention how disagreements in labeling were resolved.
    
## Dataset Distribution and Licensing
- Availability:
- Open/public or private dataset
- Dataset Documentation Link: (Link to further details if available)
- User Rights and Limitations:

## Data Versioning
**Data Version Control Tools:**
- DVC (Data Version Control): Tracks datasets, connects them to model versions, and integrates with Git.
- Git-LFS (Large File Storage): Stores large data files outside the Git repository.
- Delta Lake: Tracks changes in structured data (e.g., data lakes).
- Pachyderm: Offers data pipelines with built-in versioning.

### Maintainance of Metadata and Schema Versioning
    
 Why: Data formats, schema, and other metadata changes can impact downstream processes. Tracking these ensures transparency.

#### How:

Create a data dictionary:
- Document dataset structure, column descriptions, data types, and relationships.

Track schema changes:
- Use tools like dbt or Great Expectations to log schema evolution.
- Record changes as part of version control or data pipelines.

 Save metadata alongside datasets:
- Include details like source, timestamp, description, version, and quality metrics.
    
  

### Incorporate Data Lineage Tools
    
 Why: Data lineage tools provide end-to-end visibility of data transformations and dependencies.

#### How:

- Integrate tools like OpenLineage, Talend, or Alation.
    
- Track data movement: From ingestion to transformation to storage.
    
-  Visualise: Lineage graphs showing how different dataset versions relate.

## Known Usages
<!-- info: Fill out the following section if the dataset has any
current known usages.
-->
### Model(s)
<!-- scope: telescope -->
<!-- info: Provide a table of known models
that use this dataset.
-->

| **Model**           | **Model Task**       | **Purpose of Dataset Usage** |
|---------------------|----------------------|------------------------------|
| [Example Model 1]() | Image Segmentation   | Fairness evaluation          |
| [Example Model 2]() | Skin Tone Classifier | Training and validation      |

Note, this table does not have to be exhaustive. Dataset users and documentation consumers at large
are highly encouraged to contribute known usages.

### Application(s)
<!-- scope: telescope -->
<!-- info: Provide a table of known AI/ML systems
that use this dataset.
-->

| **Application**           | **Brief Description**        | **Purpose of Dataset Usage**                           | 
|---------------------------|------------------------------|--------------------------------------------------------|
| [Example Application 1]() | Size and Fit Recommendations | Fairness Evaluation of end-to-end application pipeline |

## Access, Retention, and Deletion
<!-- info: NEEDS INPUT FROM PRIV-GOV! -->
### Access
#### Relevant Links
* [Link to filestore]
* [Link to governance processes for data access]
* ...

#### Data Security Classification 
<!-- scope: telescope -->
<!-- info: Select **one**: Use your companies data access classification
standards (replace the classifications below accordingly) -->


#### Prerequisite(s)
<!-- scope: microscope -->
<!-- info: Please describe any required training or prerequisites to access
this dataset. -->
For example:

This dataset requires membership in [specific] database groups:

- Complete the [Mandatory Training]
- Read [Data Usage Policy]
- Initiate a [Data Processing Request]
- Get AWS IAM role with S3 bucket access
- Add Databricks cluster or other technical users to correct roles

### Retention
#### Duration
<!-- scope: periscope -->
<!-- info: Specify the duration for which this dataset can be retained: -->
Specify duration in days, months, or years.

#### Reasons for Duration
<!-- scope: periscope -->
<!-- info: Specify the reason for duration for which this dataset can be retained: -->
...

#### Policy Summary
<!-- scope: microscope -->
<!-- info: Summarize the retention policy for this dataset. -->
**Policy:** Add a link to the policy if it's standardized at your company (e.g., S3 bucket standard retention policies).

  
## Data Risk Assessment
**Describe the assessment of data risks**:
- Foreseeable unintended outcomes or biases arising from dataset use.
- Sources of potential discrimination or harm.


## Cybersecurity Measures


### Data Security Measures

#### Data Storage

- **Encryption**: Use AES-256; detail key management (e.g., HSM, key rotation).
- **Access Control**: Implement role-based access and MFA.
- **Backup**: Document backup frequency, encryption, and recovery testing.
- **Integrity Monitoring**: Use hashes, checksums, or blockchain.
- **Security**: Describe server protections (e.g., restricted access).

#### Data Transfer

- **Encryption in Transit**: Specify TLS 1.3, IPsec configurations.
- **Endpoint Security**: Detail device verification and certificate pinning.
- **API Security**: Document authentication, rate-limiting, and channel encryption.
- **Data Masking**: Use pseudonymisation for sensitive data in transit.

#### Data Processing

- **Secure Environments**: Use containers, VMs, or trusted execution (e.g., Intel SGX).
- **Audit Logs**: Specify logging standards, retention, and tamper protection.
- **Data Minimisation**: Anonymise or limit collected data.


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