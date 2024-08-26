# Guide - ML System Design Doc - v1

***Overview:** This guide provides a structured approach to creating high-quality Machine Learning System Design Documents. It's designed to help business leaders, data scientists and engineers, effectively communicate the strategic value, technical implementation details, and practical considerations of an ML project.*

***Purpose:** An ML system design document serves as a blueprint for the entire project, ensuring all stakeholders have a clear understanding of the goals, approach, and implementation details. It facilitates alignment, guides decision-making, and serves as a reference throughout the project lifecycle.*

# **1. Overview: Purpose and Impact**

**Overview:** This section provides a high-level summary of the entire project, including purpose, problem, solution, and desired outcome. It usually takes 3-5 sentences.

Key points:

- Clear problem statement
- Proposed ML solution
- Expected business impact
- High-level implementation timeline

<details>
<summary>Guide</summary>

**Purpose:** To provide a concise summary that captures the essence of the project and its expected outcomes.

**Guiding questions:**

- What specific problem are we addressing?
- Why is this problem important to the business?
- What are the high-level goals of this ML system?
- What key outcomes do we expect?
    - What's our timeline for implementation?

</details>

# **2. ML Product Design**

<aside>
💡 This section discusses how the ML solution will function as a product, helping users and driving business value. It connects technical work to business outcomes.

</aside>

> *“…most businesses don’t care about ML metrics unless they can move business metrics”*
Source: [Designing Machine Learning Systems (Chip Huyen 2022)](https://github.com/chiphuyen/dmls-book/blob/main/summary.md#chapter-1-overview-of-machine-learning-systems)

## **2.1 Problem Statement (Motivation)**

Is it the right problem to solve?

Overview: Explain the business problem and its importance to the organization. 

Key points:

- Detailed description of the business problem
- Current approaches and their limitations
- Market or industry context
- Alignment with business strategy

<details>
<summary>Guide</summary>

Purpose: Cearly define the business problem and its relevance to the organization.

Guiding questions:

- Why the problem is important to solve, and why now?
- What are the costs of not solving this problem?
- How does this align with our overall business strategy?

> "A problem well-stated is a problem half-solved." - Charles Kettering

</details>


## 2.2 Customers

Overview: This section identifies all parties involved in or affected by the ML system.

Key points:

- List of key stakeholders and their roles
- Primary end users and their needs
- Potential impact on each group

<details>
<summary>Guide</summary>

Purpose: To ensure all relevant perspectives are considered and to clarify who will be using or impacted by the system.

Guiding questions:

- Who will be directly using the ML system?
- Whose work or processes will be affected by the system?
- Who needs to be involved in the decision-making process?

> "If you want to go fast, go alone. If you want to go far, go together." - African Proverb

</details>

## 2.3 Value Proposition

Overview: This section articulates why AI/ML is the right approach for solving the problem.

Key points:

- Unique advantages of using AI/ML
- Potential improvements over current methods

<details>
<summary>Guide</summary>
    
Purpose: To justify the use of AI/ML over traditional approaches and highlight its unique benefits.

Guiding questions:

- How does AI/ML solve this problem better than traditional methods?
- What new capabilities does AI/ML bring to our business?
- How does this solution position us for future growth?
- Why AI/ML is required?

</details>

## **2.4 Business Metrics (Success)**

Overview: This section defines measurable outcomes that indicate project success. Usually framed as business goals, such as increased customer engagement (e.g., CTR, DAU), revenue, or reduced cost.

Key points:

- Specific, quantifiable business metrics
- Technical performance metrics
- Timeline for achieving key milestones

<details>
<summary>Guide</summary>

Purpose: To establish clear, quantifiable goals that align business objectives with technical performance.

Guiding questions:

- How will we measure the success of this ML system?
- What metrics align with our business objectives?
- How do we balance technical and business performance?

> Guiding Quote: "What gets measured gets managed." - Peter Drucker

</details>


## 2.5 Assumptions  and Constraints

Overview: This section outlines the foundational beliefs and limitations that shape the project. Make explicit your assumptions and understanding of the environment 

Key points:

- Key assumptions about data, users, and processes
- Technical constraints (e.g., computational resources)
- Business constraints (e.g., budget, timeline)

<details>
<summary>Guide</summary>

Purpose: To make explicit the assumptions underlying the project and acknowledge known constraints.

Guiding questions:

- What critical assumptions are we making?
- What technical or business constraints might limit our solution?
- How might our assumptions or constraints impact the project's success?

> "It is better to be roughly right than precisely wrong." - John Maynard Keynes

</details>

## 2.6 Cost Structure & ROI

Overview: This section provides a clear financial picture of the project's costs and expected returns.

Key points:

- Detailed breakdown of costs (development, serving, infrastructure, maintenance)
- Projected financial benefits and timeline
- ROI calculation and sensitivity analysis

<details>
<summary>Guide</summary>

Purpose: To justify the investment in the ML system and set realistic expectations for financial returns.

Guiding questions:

- What are all the costs associated with this project?
- How the costs will change with time?
- When do we expect to see a return on our investment?
- How sensitive is our ROI to changes in key assumptions?
- Consider cost in money and in time spent by dev/ml specialists.

> "Price is what you pay. Value is what you get." - Warren Buffett
> 

> *What are the major cost implications of the model we are building? How much will it cost to train, retrain, and serve the model? Computing the exact cost is hard, but a ballpark estimate is usually enough. 
Source: [**Design documents for ML models](https://medium.com/people-ai-engineering/design-documents-for-ml-models-bbcd30402ff7)*

</details>

# 3. Solution Design

<aside>
💡 This section provides a detailed view of the proposed ML solution, including how it will work and how it will be implemented within the business context.

</aside>

## 3.1 High-Level Solution Overview

Overview: This section provides a bird's-eye view of the proposed ML system. How the predictions should look like for a consumer? Here we don’t care how these predictions are derived, but we write down our expectations on their form/structure.  

Key points:

- Consumable format of prediction for key users
- Key components and their interactions

<details>
<summary>Guide</summary>

Purpose: To give all stakeholders a clear understanding of the overall system architecture and components.

Guiding questions:

- How the predictions should look like for a consumer?
- What are the main components of our ML system?
- How do these components interact with each other?
- How will your system integrate with upstream data (what data we’ll pass to the model) and downstream users (how users will access predictions)?

> "Simplicity is the ultimate sophistication." - Leonardo da Vinci

</details>

## **3.2** User Interface and Experience Design

Overview: This section describes how users will interact with the ML system. 

Key points:

- User interface mockups or wireframes
- User journey maps
- Integration points with existing systems

<details>
<summary>Guide</summary>

Purpose: To ensure the ML system is user-friendly and integrates well with existing workflows.

Guiding questions:

- How will users interact with the ML system?
- What changes to existing workflows are required?
- How can we make the system intuitive and user-friendly?
- How will you incorporate human intervention into your ML system (e.g., product/customer exclusion lists)?

> "Design is not just what it looks like and feels like. Design is how it works." - Steve Jobs

</details>

## 3.3 Performance Metrics

Overview: This section defines how the system's performance will be measured.

Key points:

- Technical metrics (e.g., accuracy, latency)
- Metrics we calculate for model predictions (offline). This means the case when predictions doesn’t affect real users. E.g. if we deploy the ML system in shadow mode and it gives us recommendation/decision/etc, how we will be measuring the quality of those predictions.
- Business metrics (online). This means the case when predictions affect the real users.

<details>
<summary>Guide</summary>

Purpose: To establish clear criteria for evaluating the system's technical performance and business impact. 

- How will we know that the solution is successful?

> "Not everything that can be counted counts, and not everything that counts can be counted." - Albert Einstein

</details>

## 3.4 Validation Strategy and Pilot Project Plan

Overview: This section outlines the approach for testing and validating the ML system.

Key points:

- Validation methodology
- Pilot project scope and timeline
- Success criteria for moving to full implementation

<details>
<summary>Guide</summary>

Purpose: To ensure the system performs as expected and delivers value before full-scale deployment.

Guiding questions:

- How will we validate the ML system's performance? How to validate the solution works in production process (system)?
- What does a successful pilot look like? Regardless of ML model used under the hood.
- How will we incorporate learnings from the pilot?
- If you're A/B testing, how will you assign treatment and control (e.g., customer vs. session-based) and what metrics will you measure? What are the success and [guardrail](https://medium.com/airbnb-engineering/designing-experimentation-guardrails-ed6a976ec669) metrics?

> "In God we trust. All others must bring data." - W. Edwards Deming

</details>

## **3.4 Requirements & Constraints**

Overview: This section specifies what the system must do and how well it must perform. Include functional and non-functional Requirements. 

Key points:

- Detailed functional requirements
- Non-functional requirements (e.g., scalability, security, type of inference: batch, real-time, stream)
- Constraints (hardware, model)
- Compliance and regulatory requirements
- Corner cases
- Scope of the solution
- Risks

<details>
<summary>Guide</summary>

Purpose: To clearly define the system's capabilities and performance standards. 

Guiding questions:

- What specific functions must the system perform?
- What are the performance, security, and scalability requirements?
- What regulatory standards must we adhere to?
- What's in-scope & out-of-scope? Some problems are too big to solve all at once. Be clear about what's out of scope.
- Corner cases: What’s the worst that can happen if the model is wrong only once but for a very important data point? Are all data points equally important?
- Risks: What are the major risks you are facing? What are you doing to mitigate them? Are you doing some bleeding-edge research? Do you depend on a major infrastructure component that is yet to be built?

> "Quality is never an accident; it is always the result of intelligent effort." - John Ruskin

**Requirements**

- Functional requirements are those that should be met to ship the project. They should be described in terms of the customer perspective and benefit. (See [this](https://eugeneyan.com/writing/ml-design-docs/#the-why-and-what-of-design-docs) for more details.)
- Non-functional/technical requirements are those that define system quality and how the system should be implemented. These include performance (throughput, latency, error rates), cost (infra cost, ops effort), security, data privacy, etc.
- Type of inference: batch, real-time, stream

**Constraints (hardware, model)**

- Constraints can come in the form of non-functional requirements (e.g., cost below $`x` a month, p99 latency < `y`ms)

</details>
    

# **4. Data Science Methodology**

<aside>
💡 This section covers the methodology for developing the ML model, from problem framing to model validation.

</aside>

## **4.1.** Problem Framing and Approach

Overview: This section explains how the business problem translates into a data science problem. How will you frame the problem? For example, fraud detection can be framed as an unsupervised (outlier detection, graph cluster) or supervised problem (e.g., classification).

Key points:

- ML problem type (e.g., classification, regression)
- Approach selection rationale
- Potential alternative approaches
- Baseline solution (without ML)

<details>
<summary>Guide</summary>

Purpose: To ensure the ML approach aligns with the business problem and leverages appropriate techniques.

Guiding questions:

- How do we frame this as a machine learning problem?
- What ML metric we should optimize?
- Why is this approach the most suitable?
- What is the simplest solution? Can we solve the problem without ML?
- What is a feasible baseline solution?

> "If I had an hour to solve a problem, I'd spend 55 minutes thinking about the problem and 5 minutes thinking about solutions." - Albert Einstein

</details>

## **4.2.** Data and Feature Engineering

Overview: This section outlines the plan for data acquisition, processing, and management.

Key points:

- Data sources and collection methods
- Data preprocessing and feature engineering
- Data quality assurance processes
- Data Labeling

<details>
<summary>Guide</summary>

Purpose: To ensure the ML system has access to high-quality, relevant data.

Guiding questions:

- What data will you use to train your model?
- What input data is needed during serving?
- How will we ensure data quality and relevance?
- **Data Processing Techniques:** What machine learning techniques will you use? How will you clean and prepare the data (e.g., excluding outliers)
- **Feature Engineering**: How will you create features?

> "Data is the new oil. It's valuable, but if unrefined it cannot really be used." - Clive Humby

</details>

## 4.3 Modeling Techniques and Algorithms

Overview: This section describes the specific ML techniques and algorithms to be used.

Key points:

- Selected algorithms and rationale
- Model architecture details
- Hyperparameter tuning strategy

<details>
<summary>Guide</summary>

Purpose: To provide a clear understanding of the technical approach and its rationale

Guiding questions:

- Which ML algorithms are most suitable for our problem?
- How will we optimize model performance?
- What are the trade-offs between different modeling approaches?

> "All models are wrong, but some are useful." - George Box

</details>

## **4.4.** Model Validation and Evaluation Framework

Overview: This section explains how model performance will be evaluated and validated.

Key points:

- **Techniques**: Cross-validation (e.g., k-fold cross-validation), holdout validation, stratified sampling.
- **Data Splits**: Training set, validation set, and test set.
- **Metrics**: Performance metrics specific to the validation and test phases. Evaluation metrics should be relevant to business metrics.

<details>
<summary>Guide</summary>
    
> "Trust, but verify." - Ronald Reagan
> 

**Purpose:** To ensure the model's performance can be reliably measured and meets business requirements.

**Guiding questions:**

- How will we split our data to validate the model effectively?
- What techniques will we use to validate the model?
- How will we interpret the validation metrics to improve the model?
- How will we measure model performance?
- How will we ensure the evaluation process is unbiased and thorough?
- How will we interpret and report the evaluation results to stakeholders?

Summary on model Validation & Evaluation

|  | **Model Validation** | **Model Evaluation**  |
| --- | --- | --- |
| **Purpose** | Assess generalization to unseen data | Comprehensive assessment before deployment |
| **Focus** | Tuning and improving model performance | Final performance metrics and business impact |
| **Timing** | During the model development phase | After model training and validation |
| **Techniques** | Cross-validation, holdout validation | Confusion matrix, ROC/AUC, MAE, MSE |
| **Data Used** | Training set, validation set | Test set |
| **Metrics** | Validation accuracy, validation loss | Precision, recall, F1-score, RMSE, business metrics |
| **Outcome** | Model refinement and selection | Final decision on model readiness for production |

</details>

# **5.** Production ML System Design

<aside>
💡 This section outlines the design for deploying and operationalizing the ML system in a production environment.

</aside>

## **5.1. High-level design**

**Overview:** This section provides a detailed view of the system's technical architecture. Start by providing a big-picture view. [System-context diagrams](https://en.wikipedia.org/wiki/System_context_diagram) and [data-flow diagrams](https://en.wikipedia.org/wiki/Data-flow_diagram) work well.

**Key points:**

- Detailed system architecture diagram
- Data flow and processing pipeline
- Integration with existing infrastructure

<details>
<summary>Guide</summary>

Purpose: To ensure all technical stakeholders understand how the system will be built and how data will flow through it.

Guiding questions:

- How will the ML system integrate with our current infrastructure?
- What are the key components of our data processing pipeline?
- How will we ensure efficient data flow through the system?

> "Simplicity is a prerequisite for reliability." - Edsger Dijkstra

</details>

## 5.2 Deployment and Serving

Overview: This section outlines the plan for deploying and serving the ML model.

Key points:

- Type of inference (batch, real-time)
- Requirements for CI/CD.
- Deployment methodology (e.g., blue-green, canary)
- Serving infrastructure details

<details>
<summary>Guide</summary>

Purpose: To ensure smooth deployment and reliable serving of model predictions.

Guiding questions:

- Do we want to perform batch (offline) or real-time (online) inference?  What tools should we use?
- How will we deploy the model with minimal disruption? Do we need human checks? How do we test the models before deployment to be sure they doesn’t break prod?
- Do we need to support online A/B testing, canary deployment, etc?
- What infrastructure is needed to serve model predictions?

> "Hope is not a strategy." - Vince Lombardi

</details>
    

## **5.3** Data Engineering

Overview: 

This section describes the data infrastructure supporting the ML system.

Key points:

- Data ingestion and storage solutions
- ETL processes (data pipelines)
- Data versioning and lineage tracking
- Feature Stores (Data Marts)

<details>
<summary>Guide</summary>

Purpose: To ensure reliable, efficient data processing and feature engineering in production.

Guiding questions:

- How will we handle data ingestion and storage?
- What ETL processes are needed to prepare data for the model?
- How will we track data versions and lineage?

> "Data is the foundation of all machine learning systems." - Andrew Ng

</details>

## **5.4** Model Development Lifecycle

Overview: 

This section explains the process for ongoing model development and deployment.

Key points:

- Requirements for automation, reproducibility, reliability
- Model versioning strategy.
- Model updating and retraining process
- Model Registry

<details>
<summary>Guide</summary>

Purpose: To ensure continuous improvement and reliable updates to the ML system.

Guiding questions:

- How to train the model?
- How often to re-train?
- How will we manage model versions?
- What is our CI/CD pipeline for model deployment?
- How and when will we retrain our models?

> "Continuous improvement is better than delayed perfection." - Mark Twain

</details>

## 5.5. **Testing and Monitoring**

Overview: This section outlines the approach for ensuring ongoing system quality and performance.

Key points:

- Monitoring system design
- Testing strategy (unit, integration, system tests)
- Quality assurance processes
- Biases and misuses of your model.
- Performance Drop
- Data Drift

<details>
<summary>Guide</summary>

Purpose: To maintain system reliability and catch issues before they impact business operations.

Guiding questions:

- How will we monitor the system's performance in production?
- What testing procedures will ensure system reliability?
- How will we maintain quality as the system evolves?
- How we understand the model performs well?
- How will you log events in your system? What metrics will you monitor and how? Will you have alarms if a metric breaches a threshold or something else goes wrong?
- What are model and data metrics to track?

> "Quality is not an act, it is a habit." - Aristotle

</details>

## **5.6**  Scalability and Infrastructure Planning

Overview: This section describes how the system will scale to meet future demands.

Key points:

- Scalability requirements and approach
- Infrastructure growth plan
- Performance optimization strategies
- Infrastructure costs

<details>
<summary>Guide</summary>

Purpose: To ensure the system can grow with the business and handle increased load.

Guiding questions:

- How will you host your system? On-premise, cloud, or hybrid?
- How will our system handle increased load?
- What infrastructure changes are needed for future growth?
- How can we optimize system performance at scale?
- How much will it cost to build and operate your system? Share estimated monthly costs (e.g., EC2 instances, Lambda, etc.)

> "Scalability is not a feature; it's an architectural characteristic." - Martin L. Abbott

</details>

## **5.7 Requirements & Constraints**

Overview: 

This section addresses critical security, privacy, regulatory, and other requirements and constraints.

Key points:

- Data security measures
- System security
- Data Privacy. Compliance with relevant regulations (e.g., GDPR, CCPA)
- Risks & Uncertainties
- Ethical considerations
- Additional requirements and constraints

<details>
<summary>Guide</summary>

Purpose: To ensure the ML system protects sensitive data and complies with relevant regulations.

Guiding questions:

- How will your system/application authenticate users and incoming requests? If it's publicly accessible, will it be behind a firewall?
- How will we protect sensitive data?
- What measures ensure user privacy?
- How do we maintain regulatory compliance?
- Data Privacy. How will you ensure the privacy of customer data? Will your system be compliant with data retention and deletion policies (e.g., [GDPR](https://gdpr.eu/what-is-gdpr/))?
- What worries you and you would like others to review? Risks are the known unknowns; uncertainties are the unknown unknows.

> "Security is always excessive until it's not enough." - Robbie Sinclair

</details>


# Resources

**Templates** 

- [ML System Design doc template - eugeneyan](https://github.com/eugeneyan)/[ml-design-docs](https://github.com/eugeneyan/ml-design-docs)
- [ML DESIGN TEMPLATE (machinelearninginterviews.com)](https://www.machinelearninginterviews.com/ml-design-template/)
- [Postmortem / Correction of Error (CoE) template](https://medium.com/@josh_70523/postmortem-correction-of-error-coe-template-db69481da31d)

**Posts & Guides** 

- [How to Write Design Docs for Machine Learning Systems](https://eugeneyan.com/writing/ml-design-docs/)
- [The Undeniable Importance of Design Docs to Data Scientists](https://towardsdatascience.com/the-undeniable-importance-of-design-docs-to-data-scientists-421132561f3c)
- [Understanding Design Docs Principles**](https://towardsdatascience.com/understanding-design-docs-principles-for-achieving-data-scientists-53e6d5ad6f7e)
- [Machine Learning Product Design (Made With ML)](https://madewithml.com/courses/mlops/product-design/)
- [Machine Learning System Design (Made With ML)](https://madewithml.com/courses/mlops/systems-design/)
- [The Undeniable Importance of Design Docs to Data Scientists](https://towardsdatascience.com/the-undeniable-importance-of-design-docs-to-data-scientists-421132561f3c) (Vincent Tatan)
- [Understanding Design Docs Principles (Vincent Tatan)](https://towardsdatascience.com/understanding-design-docs-principles-for-achieving-data-scientists-53e6d5ad6f7e)
- [Design documents for ML models (Olexiy Oryeshko, People.ai)](https://medium.com/people-ai-engineering/design-documents-for-ml-models-bbcd30402ff7)

**Examples**  

- [The Quickest Analytics to Build Your Instagram Business](https://towardsdatascience.com/the-quickest-analytics-to-build-your-instagram-business-b7b3c5d68056)
- Video of the [Demo Day for the class CS 329S: Machine Learning Systems Deign at Stanford (Winter 2022)](https://www.youtube.com/live/AZNTqytOhXk?feature=shared) and [project reports](https://stanford-cs329s.github.io/reports/)
- Stanford, CS 329S - Machine Learning Systems Design: [Student project - Tender Matching People to Recipes”](https://stanford-cs329s.github.io/reports/tender-recipe-recommendations/)   (Recipes recommendation + Streamlit)
- Stanford, CS 329S - Machine Learning Systems Design: [](https://stanford-cs329s.github.io/reports/tender-recipe-recommendations/)[Student project - ML Production System For Detecting Covid-19 From Coughs](https://stanford-cs329s.github.io/reports/ml-production-system-for-covid-detection/)** (Audio + tabular features + GCP)
- Stanford, CS 329S - Machine Learning Systems Design: Student project - [Building a Context Graph Generator](https://stanford-cs329s.github.io/reports/context-graph-generator/) (Graph DB + BERT + Streamlit)
- Stanford, CS 329S - Machine Learning Systems Design: Student project - [An active data valuation system for dashcam data crowdsourcing](https://stanford-cs329s.github.io/reports/dashcam-data-valuation/) (Technical ML for ML focus + AWS)
- Stanford, CS 329S - Machine Learning Systems Design: Student project - [Stylify](https://stanford-cs329s.github.io/reports/stylify/) (GAN + AWS)
- Stanford, CS 329S - Machine Learning Systems Design: Student project - [Fact-Checking Tool for Public Health Claims](https://stanford-cs329s.github.io/reports/Fact-Checking-Tool-for-Public-Health-Claims/) (Streamlit + Docker + GCP)

**Books** 

- [Designing Machine Learning Systems book (Chip Huyen, O'Reilly 2022)](https://github.com/chiphuyen/dmls-book/blob/main/summary.md#chapter-1-overview-of-machine-learning-systems)
- 

**Courses**

- [CS 329S: Machine Learning Systems Design](https://stanford-cs329s.github.io/)