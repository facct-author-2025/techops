# Home

## TechOps Introduction
Welcome! This is the website contains rendered versions of AI documentation templates and examples
from the paper "TechOps: Technical Documentation Templates for the AI Act", under review for FAccT 2025.
We recommend developing documentation with the help of such rendering as it helps all actors (developers, deployers,
users, etc.) more easily view documentation details while maintaining view of the big picture.

These templates and examples are not to be used before publication and serve, for the moment, only to demonstrate the work described in the paper. All rights reserved.

## Templates
TechOps are three separate templates for sufficiently documenting AI systems for proof of compliance with the AI Act.
The documentation is split into three levels:

* AI System documentation
* Model documentation
* Data documentation

to allow the owners of data, models, and AI systems to each maintain ownership of their own level of documentation.  
Thus, model and dataset owners whom may or may not have curated their models and datasets with a specific AI Systems in 
mind, may still create documentation contributions that the AI System documentation can reference.

These templates are meant to guide responsible stakeholders to document AI systems across various fields. 
Unlike existing lengthy and abstract questionnaires, these templates offer clear guidance for the documentation of the 
relevant processes across the AI lifecycle, translating complex requirements such as fairness and data governance 
into actionable metrics and measurable criteria that can be implemented and tracked. 
This process ensures that the abstract legal requirements of the AI Act are operationalized into concrete actions, 
making them manageable and measurable.

Following the TechOps approach also provides stakeholders comprehensive oversight on the data, model and application lifecycle. These templates track the system’s status over the 
entire AI lifecycle, ensuring traceability, reproducibility, in addition to compliance with the AI Act. 

Clear documentation also promotes discoverability, collaboration, and risk assessment.

## Examples

The templates are tested on real-world scenarios providing examples that further guide their implementation:

|                                                                   | Description | 
|-------------------------------------------------------------------|---|
| [Model Documentation Example](example-data-documentation-voc-skin-tones/) | The model template is followed to document a neural network for segmenting human silhouettes in photos |
| [Data Documentation Example](example-data-documentation-alisnet/) | The data template is followed to document a skin tones dataset created to support fairness evaluations of downstream computer vision models and human centric applications |

## How To Use

The approach is to choose which of the templates need to be filled.  For example, if you are responsible for an
AI System and have trained your own models based on custom datasets that have not been documented, you
may need to work at all three documentation levels (AI System, model, and data).

We, the TechOps developers, advise that documentation authors use the templates as best suites their needs given
documentation standards that already exist in your context. One example of how to use the templates would be,

1. Create a GitHub Repo for your documentation.
2. Take the template(s) markdown file you wish to implement (see [our GitHub Repo](https://github.com/facct-author-2025/techops)) 
   and implement them with the help of the template comments and [examples](#examples).
3. Render your documentation to make it easy to read, similar to how the examples are rendered on this website
   (you can use [our GitHub Repo](https://github.com/facct-author-2025/techops) as an example for how to render using 
   [mkdocs](https://www.mkdocs.org/)).
