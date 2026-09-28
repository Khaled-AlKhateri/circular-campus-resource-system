Khalifa University
Department of Computer Science
Phase 2 Feasibility Study
Intelligent AI Powered Circular Campus Resource Exchange
and Asset Life Cycle Management System
Group 8
COSC 336 Introduction to Software Engineering
Lab Based Running Project
Fall 2026
Phase 2 Deliverable
Khaled AlKhateri - 100064610
Karim Bashar - 100068938
Prepared as a feasibility analysis building on the Phase 1 project plan
Contents
This report evaluates whether the proposed circular campus resource exchange system can be delivered as a semester prototype and whether its design can progress to requirements analysis. The sections follow the feasibility dimensions required for Phase 2.
Section	Focus
Executive Summary	Conditional go decision and principal findings
1 Purpose and Feasibility Decision	Decision boundaries and mandatory conditions
2 Project Foundation from Phase 1	Scope, stakeholders, and success criteria carried forward
3 Feasibility Evaluation Method	Evaluation dimensions, evidence, and limitations
4 Technical Feasibility	Architecture, database, integrations, and security
5 Data and AI Feasibility	Data readiness, AI functions, evaluation, and fallback
6 Financial Feasibility	Cost assumptions, benefits, and production cost gap
7 Operational Feasibility	Workflow, adoption, training, and support
8 Schedule Feasibility	Milestones, critical path, scope tiers, and team allocation
9 Legal Ethical Privacy Security and Policy Constraints	Institutional, legal, and responsible AI controls
10 Risk Assessment	Prioritized risks, mitigations, and triggers
11 Feasible Solution Alternatives	No change, classic, hybrid, and AI first options
12 Consolidated Feasibility Scorecard	Weighted feasibility scores and interpretation
13 Recommendation and Phase 3 Entry Conditions	Actions required before requirements approval
Appendices and References	Assumptions, measures, traceability, and cited sources


Executive Summary
The proposed Intelligent AI Powered Circular Campus Resource Exchange and Asset Life Cycle Management System is feasible as an experimental campus resource management system prototype. The decision recommendation is go with conditions. The team shall proceed to the next phase only with a constrained scope, synthetic or anonymized data set, modular application design, human approval of all transfers and life cycle actions, and deterministic fallback in case of AI services unavailability or ambiguity.
The most robust feature of the proposal is the technical match with a contemporary web application. Asset records, requests, approvals, transfers, maintenance incidents, and audit logs can be handled through well-known application and relational database technologies. AI services provide practical utility for classifications and semantic matching, yet it is also the major source of feasibility limitations. The student team will probably not have access to full institutional data sets; outputs from machine learning models will be inconsistent; usage of the third-party AI services will incur additional cost; privacy regulations will impose certain constraints on the use of actual asset and user data. The last issue does not preclude the development of a prototype if the system does not rely on AI services as a source of autonomy.
The level of operational feasibility is fairly high since the proposed flow is aligned with roles defined in Phase 1. Representatives of departments deliver information about assets; requestors do searches and submit requests; custodians validate the status of assets and their custody; administration approves transfers; maintenance records maintenance activity; while sustainability, procurement, and finance officers evaluate outcomes. Successful implementation requires forms of easy use, permission levels, consistent data input, approval status, and a training manual. It is important that the system does not require all stakeholders to be aware of the AI algorithm.
Financial feasibility is acceptable for the course project prototype since the team may rely on its own and university equipment, Git/GitHub, open source development environment, and a local database. There will be minimal direct cash costs if paying for cloud services and AI services is optional. It is impossible to estimate costs of deployment in the production environment in Phase 2 because hosting requirements, integrations, procurement policies, support, amount of data, and security assessment are still unknown. The report estimates costs using transparent ranges and benefit formulas.
Schedule feasibility is the most immediate management concern. The course allocates one week to Phase 2, two weeks to requirements, three weeks to design, three weeks to implementation, and a final compressed testing and submission period. A two-person team can complete a convincing prototype only if it delivers a narrow end-to-end workflow first. Advanced image classification, predictive demand forecasting, broad integration with university systems, and autonomous recommendations should remain future extensions unless the core workflow is stable ahead of schedule.
Table 1 Executive Feasibility Summary
Dimension	Finding	Decision Condition
Technical	Feasible with a modular web architecture and relational database	Use a modular monolith and isolate AI behind service interfaces
Data and AI	Feasible for demonstration with controlled data and measurable evaluation	Use synthetic or approved anonymized data and retain human review
Financial	Feasible for a prototype with low direct cash cost	Treat production costs and savings as unverified until institutional inputs exist
Operational	Feasible if role workflows remain simple and approvals are explicit	Validate forms and status flows with representative users
Schedule	Feasible only with strict minimum scope	Complete one end-to-end workflow before optional AI extensions
Compliance and security	Feasible for a non-production prototype with safeguards	Do not use restricted data or connect to university systems without approval


1 Purpose and Feasibility Decision
This Phase 2 report determines the viability of the project defined in Phase 1 inside the constraints of the course environment. It reviews the architecture, database, AI services, semantic search, reporting capability, integrations, development resource pool, expected operating model, schedule of the project, readiness of the data, and relevant constraints. It does not replace the comprehensive requirements document that will be created in Phase 3. Rather, it sets the stage for determining what we can responsibly develop, what needs to wait, and what has to be sorted out before we finalize requirements.
1. 1 Feasibility Decision
Decision: Conditional go. This project should go ahead as it allows creating a functional baseline system using standard software engineering tools, and a limited AI matching feature can be shown without letting AI make asset decisions. This is a conditional go, as the team needs to keep the scope under control and clarify some important assumptions. The inability to acquire useful data, establish human approval boundaries, or maintain a non-AI option will turn the project into an unreliable demo.
1. 2 Required Conditions
1. Approve an essential prototype scope that covers authentication, role permissions, asset registration, publication, search, requests, one approval and transfer workflow, maintenance history, and a small sustainability summary.
2. Use synthetic data or data that an authorized university owner has approved and anonymized for the course project.
3. Implement AI classification or semantic matching as a recommendation service with confidence information, explanations, and user override.
4. Keep exact search, filtering, and rule-based workflow logic available when the AI service is unavailable or produces low confidence.
5. Track direct service usage and cost so free-tier assumptions do not hide a future expense.
6. Confirm applicable university IT, data, procurement, and acceptable-use policies before connecting to institutional systems or entering non-public information.

1. 3 Decision Boundaries
Conditional Go refers to a course prototype rather than a production version. This prototype can showcase practical workflows and even measure sample sustainability metrics, but it should not be regarded as the system of record for the university. Deployment to production will call for proper ownership, security testing, support setup, data governance, integration approval, legal review, procurement decisions, and proof of stable AI performance on representative institutional data.
2 Project Foundation from Phase 1
Phase 1 found a campus problem. One department may discard a usable asset while another department buys an equivalent item. Asset records can show ownership, location and status. They do not always allow an internal exchange, resource requests, smart matching, transfer approval, maintenance coordination or complete life‑cycle tracking. The proposed system fills this gap. It offers a shared platform, for publishing surplus items managing requests, transferring assets, recording service history and supporting decisions.
2. 1 Scope Carried Forward
- Register campus assets with ownership, department, location, condition, availability, estimated value, and supporting information.
- Publish surplus or underused resources for authorized campus users.
- Allow departments to submit needs, search and filter records, reserve items, and track requests.
- Control approvals, transfers, custody changes, receipt confirmation, maintenance, repair, donation, recycling, retirement, and disposal events.
- Use AI to assist classification, semantic matching, recommendation ranking, natural language interaction, and report summarization.
- Measure reuse, avoided purchase, asset life extension, maintenance cost, waste diversion, and estimated environmental benefit where the data supports the calculation.
2. 2 Stakeholders Carried Forward
Table 2 Stakeholder Needs Relevant to Feasibility
Stakeholder	Primary Need	Feasibility Implication
Department representatives	Register assets and publish availability	Forms must be short and use controlled categories
Asset custodians	Confirm condition, location, custody, and transfer	Mobile-friendly status updates and audit history are important
Requesters	Find suitable resources and submit needs	Search must work without AI and explain recommended matches
Administrators	Approve requests, releases, transfers, and final actions	Role-based access and separation of duties are required
Procurement and finance officers	Review costs, avoided purchases, and spending evidence	Savings must use traceable formulas and supporting values
Maintenance personnel	Record inspection, repair actions, cost, and condition	The data model needs status history rather than one current value
Sustainability officers	Review reuse, repair, recycling, and impact indicators	Calculations need defined boundaries and uncertainty labels
System administrators	Manage users, roles, configuration, and audit records	Administrative functions must be limited and logged


2. 3 Success Criteria Refined for Feasibility
I see that Phase 1 described success using terms. I notice that Phase 2 turns those statements into evidence that can be tested later. The prototype should finish an end‑to‑end asset reuse workflow. The prototype should preserve a history. The prototype should return search and match results. The prototype should stop actions. The prototype should compute sample sustainability indicators, from known inputs. AI quality must be evaluated separately from workflow completion. A successful transfer does not prove that an AI recommendation was accurate. A relevant recommendation does not prove that a transfer was approved or beneficial.
3 Feasibility Evaluation Method
The evaluation is based on six dimensions from the Phase 2 instructions. Each dimension gets a score from one, to five. A score of one means the project cannot move forward under the assumptions. A score of three means the area is possible but has limitations. A score of five means the area is clearly feasible using existing resources and standard methods. These scores wrap up the analysis. They do not replace the detailed conditions and risks explained in the following sections.
Table 3 Feasibility Dimensions and Evidence
Dimension	Weight	Evidence Considered
Technical	20 percent	Architecture complexity, software availability, integration effort, performance, fallback behavior
Data and AI	20 percent	Data availability, completeness, privacy, model suitability, evaluation, explainability
Operational	15 percent	Role fit, workflow adoption, training, ownership, support
Financial	15 percent	Development resources, direct expense, service cost, support cost, measurable benefits
Schedule	15 percent	Course milestones, two-person capacity, dependencies, testing time
Compliance and security	15 percent	Privacy, authorization, auditability, procurement, safety, policy approval


3. 1 Evidence and Limitations
The analysis uses the course project brief, the Phase 1 planning document the Phase 2 lecture slides, the official course schedule and current official public references on UAE data protection and Khalifa University privacy and policy access. The team has not yet provided an institutional asset dataset, integration specification, production hosting standard, procurement quotation or approved university business process. Accordingly all cost ranges are planning assumptions and all AI performance claims remain to be tested. The report deliberately avoids a guaranteed return on investment or model accuracy percentage.
4 Technical Feasibility
Technical feasibility is high for the baseline system. Moderate for the AI extensions. The core workflows resemble information systems: authenticated users create records, search data, request actions approve state changes and review reports. These functions fit a web application backed by a database. The challenge comes from integrating AI without making the system dependent, on expensive services.4 1 Recommended Architecture Approach
I believe a modular monolith is the architecture for the semester prototype. It lets us keep user management assets, requests, approvals, transfers, maintenance, sustainability reporting and AI adapters all inside a deployable application. This way the two of us can. Debug more easily while still keeping each part clear and separate. In contrast microservices would bring network traffic, service discovery, distributed logging, several separate deployments and a lot of integration tests even though the project is not yet ready to scale each part independently.
The application should show the AI functions through a service interface. The classification function takes approved asset fields. Gives back suggested categories, tags, missing metadata, confidence and an explanation. The matching function takes a request and candidate assets. Gives back ranked suggestions. The rest of the application stays in charge of authentication, authorization, workflow status, approvals, audit records and final decisions. This setup lets the team swap a model for a local model or a deterministic rule, without having to rewrite everything.Table 4 Technical Component Feasibility
Component	Feasible Prototype Choice	Assessment and Constraint
User interface	Responsive web interface	High feasibility using standard forms, tables, validation, and dashboards
Application services	Single backend with separated modules	High feasibility and easier integration testing than microservices
Relational data	PostgreSQL or SQLite for local demonstration	High feasibility; PostgreSQL is preferable if multi-user deployment is required
Files and photographs	Controlled local or object storage	Feasible if file type, size, access, and retention rules are enforced
Search and filters	Database queries with indexed fields	High feasibility and mandatory as the non-AI fallback
Semantic search	Text embeddings with a vector index	Moderate feasibility; quality depends on descriptions and domain vocabulary
AI classification	Prompted LLM or small classification model	Moderate feasibility; requires confidence, review, and repeatable evaluation
LLM assistant	Retrieval over approved system data and help content	Moderate feasibility; restrict actions and prevent direct approval decisions
Reports	Database summaries with optional generated narrative	High feasibility if every generated statement traces back to calculated data
External integrations	Mocked interfaces for the prototype	Low to moderate feasibility until university APIs and approvals are known


4. 2 Database and Life Cycle Tracking
I see that the data model is doable because the main concepts are organized and related. Users belong to departments. Are given roles. Assets belong to departments and categories. They collect inspections, maintenance records, transfers, documents and life cycle events. Requests explain a need. May get several possible matches. Approvals refer to a requested action. Keep the approver, time, decision and reason. Audit records capture changes. This model supports relational rules and transactions which are more reliable than storing the operational state only in AI‑generated text.
4. 3 Performance. Reliability
I think the prototype will not need transactions so one application instance and one relational database will be enough for the course. The team still needs to index fields that are often filtered such, as category, department, condition, status, location and availability. Large photographs and documents should stay outside database rows. AI operations should use timeouts, retries and run asynchronously when a request might take several seconds. If a classification fails it should not stop an user from saving an asset manually.
4. 4 Security Engineering Feasibility
Authentication and role-based authorization are feasible with established frameworks. Every sensitive operation must check permission in the backend, even if the interface hides unavailable actions. Passwords should use framework-provided secure hashing. Sessions or tokens require expiration and secure storage. Transfer approval, ownership change, disposal, user administration, and configuration changes should create immutable audit entries. The prototype should avoid storing identity documents, personal phone numbers, or unrelated personal details because they are not needed to demonstrate the workflow.
5 Data and AI Feasibility
I think Data and AI feasibility looks moderate. The AI functions that are being proposed are realistic.. The usefulness of the AI functions depends more on data quality and evaluation discipline than, on having a powerful model.
Asset descriptions might be incomplete. Departments may call the item by different names. Condition ratings can be subjective. Historic transfer and maintenance records might not exist in a form.
The prototype should therefore show the workflow with a controlled dataset. The prototype should also report the limitations clearly.
5. 1 Data Readiness
Table 5 Data Readiness and Prototype Strategy
Data Domain	Likely Readiness	Prototype Strategy	Quality Check
Asset inventory	Partial or unknown	Create representative synthetic records across key categories	Required fields, unique identifiers, valid status and department
Department requests	Limited historic data	Generate sample requests with different vocabulary and urgency	Complete purpose, quantity, required date, and specifications
Transfers and approvals	May be distributed across documents	Simulate state transitions and approval records	Valid sequence, authorized actor, timestamp, reason
Maintenance history	Variable detail	Use sample inspections and repairs linked to assets	Cost units, dates, before and after condition
Procurement values	Sensitive and access controlled	Use clearly labeled sample reference values	Currency, date, source, and approval for use
Sustainability factors	Methodology dependent	Use documented sample factors with uncertainty labels	Unit, source, boundary, version, and calculation trace
Images and documents	Potential privacy and copyright limits	Use team-created or approved sample files	File type, malware screening, ownership, retention


5. 2 AI Assisted Classification
Classification can work well as a help tool. A person can type an asset title, description, specifications. Optionally add a picture. The AI service might propose a Classification, subcategory, material tag or a missing field. The interface should display the Classification suggestion of quietly changing the person’s own input. To judge the AI use a labeled test set that the model did not see during creation. The team can track Classification accuracy, top‑k accuracy, invalid Classification rate and the share of Classification proposals that people accept or change.
5. 3 Semantic Matching and Ranking
Semantic Matching gives the AI help because a person asking for something may describe it in a different way than the owner of the item. An embedding model can find items that have a meaning then simple rules can drop items that are not available or that have not enough quantity. A clear Ranking formula can mix Semantic Matching similarity with condition, location, urgency, required date transfer cost and repair need. The Ranking formula and its weights should be saved by version so the team can explain why one Semantic Matching candidate comes before another. The team should check match relevance with a set of requests and candidate items that experts have reviewed. Good checks include how many of the Ranking results are correct whether at least one suitable item is in the top five the average relevance from reviewers, how useful the explanation is and the override rate. A small sample cannot prove that the Semantic Matching model is fair or accurate for all campus items. The evaluation must say its sample size and the categories used.
5. 4 Sustainable Action Recommendations
Recommendations about repair, transfer, donation, recycling or disposal can change safety, ownership and cost. The prototype should use decision rules for hard limits, such as unavailable status, required inspection, hazardous material handling or missing approval. AI can sum up the factors and rank the allowed options but a user, with permission must make the final choice. Disposal must stay a controlled step and must never happen just because a language model gave a convincing explanation.
5. 5 LLM Assistant and Generated Reports
LLM Assistant can work if it only pulls records that the user is allowed to view. The LLM Assistant may help people search explain a status draft a request or find a policy page. It should not carry out transfers approve disposal change ownership or expose departments’ restricted data. Generated Reports should start from verified totals made by database queries. The model can rewrite those totals into text but the Generated Report must show the raw numbers and point out any uncertain estimates
5. 6 AI Failure and Fallback
- If classification fails, users select a category and tags manually.
- If semantic search fails, exact keyword, category, condition, department, location, and status filters remain available.
- If the model returns low confidence, the system labels the result for review and does not treat it as a completed decision.
- If an external service is unavailable, the application records the failure without losing the asset or request transaction.
- If generated text conflicts with calculated data, the calculated totals and source records take priority.
6 Financial Feasibility
Financial feasibility is acceptable, for a student prototype. Phase 1 already identified the resources as the two team members, personal or university computers, Git and GitHub development tools, a database, modeling tools, testing tools and AI libraries or services. Most can be used without payment. The main uncertain costs are hosting external AI calls, file storage, backups and any future integration or security work.
6. 1 Prototype Cost Assumptions
Table 6 Illustrative Direct Cost Range for the Course Prototype
Cost Area	Planning Range in AED	Basis and Control
Source control and collaboration	0	Use Git and GitHub within available educational or free access
Development and modeling tools	0 to 500	Prefer open source or university-provided tools
Database and local storage	0	Use local PostgreSQL or SQLite during development
Prototype hosting	0 to 1500	Free or low-cost hosting only if remote demonstration is required
AI service usage	0 to 2500	Cap requests, cache results, and preserve a local or manual fallback
Backup and test storage	0 to 500	Keep only approved sample files and limit retention
Contingency	0 to 1000	Do not commit until a specific need and owner are identified
Total direct cash range	0 to 5500	Excludes student labor and any production deployment


These values are feasibility assumptions, not quotations. The project should be designed so the lower end remains possible. Any paid service should have a spending cap, an owner, usage logging, and a replacement path. Student labor is excluded from the direct cash total because it is course work, but the schedule section treats team time as the main scarce resource.
6. 2 Potential Benefits
The financial benefits expected from the system come from avoiding or delaying purchases extending the life of assets reducing duplicate inventory and making better maintenance decisions based on accurate information. These benefits can only be claimed after the prototype has recorded reference prices, repair costs, transfer costs, approved quantities and proof that a purchase was truly avoided. The system must calculate the gross value of avoided purchases and then subtract the costs of repair, refurbishment, transfer and any extra operating expenses. Benefits should be reported separately for each time period. It is important not to mix sample data with savings from the university.
6. 3 Production Cost Gap
The production budget has not been set yet. Key factors that will affect the budget include hosting and availability needs, integration, with identity management systems, backup and recovery goals, monitoring requirements, security assessments, data migration plans, user support, service ownership, vendor agreements, expected transaction volume, model usage and data retention rules. Phase 3 should list these items as dependencies instead of trying to estimate final costs. This gap does not stop the prototype work. It means the team cannot decide to move into production without a full cost picture.
7 Operational Feasibility
Operational feasibility is moderate to high because the proposed system follows recognizable university responsibilities. The workflow becomes difficult only if the application requires duplicate data entry, unclear ownership, or too many approval steps. The prototype should prove that each role can complete its part without seeing or changing unrelated information.
7. 1 Proposed Operating Workflow
1. A department representative registers an asset or updates an approved record.
2. An asset custodian verifies condition, location, custody, and whether the item can be published.
3. A requester searches available records or submits a structured need.
4. The system returns rule-based results and optional AI-ranked recommendations with explanations.
5. Authorized staff review the request, confirm availability, and approve or reject the proposed release and transfer.
6. The system records collection or delivery, custody change, new location, and receipt confirmation.
7. Maintenance and sustainability events update the life cycle history and reporting measures.

7. 2 Adoption Conditions
Table 7 Operational Adoption Conditions
Condition	Why It Matters
Clear ownership	Users need to know who may publish, approve, transfer, and close records
Low entry burden	Long forms will produce incomplete or outdated records
Visible status	Departments need to know whether a request is waiting, approved, rejected, or completed
Reliable search	Users will abandon the exchange if relevant assets are hard to find
Human accountability	AI suggestions cannot replace approval or safety review
Training and help	Different roles will use the system at different frequencies
Support path	Incorrect records and access problems need an owner


7. 3 Change Management
The pilot should begin with a small number of categories and departments rather than attempting university-wide adoption. A narrow pilot makes it possible to align category names, test approval responsibilities, observe where users stop, and correct the workflow before more data accumulates. The team should collect feedback after asset registration, request submission, recommendation review, and transfer confirmation. The most useful operational metrics are task completion, time to complete, error rate, support requests, abandoned requests, and the reasons users override recommendations.
8 Schedule Feasibility
The project schedule remains feasible only if scope is reduced early and milestone dependencies are controlled. Phase 2 is due on 21 September 2026. Requirements are due on 5 October, design on 26 October, draft implementation on 16 November, and testing and final delivery on 23 November. The final period is compressed because testing and final delivery share the same deadline, so feature development must stop early enough to protect correction and documentation time.
<img src="media/image1.png" title="Timeline of project delivery milestones from Phase 1 on 14 September through Phases 7 and 8 on 23 November 2026" style="width:6.65in;height:2.70156in" alt="Timeline of project delivery milestones from Phase 1 on 14 September through Phases 7 and 8 on 23 November 2026" />

Figure 1 Project delivery milestones
8. 1 Development Priorities and Dependencies
Development should begin with a stable data model and clearly defined user roles because the system’s main functions depend on consistent asset and request information. After these the team can start to develop search, AI-supported matching, approval, and transfer. The required data and role responsibilities should be defined during the requirements phase and confirmed during the design phase before optional features are developed. Integration work should begin as soon as the data structures and communication rules are finalized so that technical problems can be identified and corrected before final testing. Priority should remain on completing and testing the core workflow before adding secondary features.
8. 2 Scope Tiers
Table 8 Scope Priorities
Tier	Functions	Schedule Decision
Essential	Authentication, roles, departments, asset registration, publication, search, request, approval, transfer confirmation, maintenance history, audit log	Must work end to end before optional features
Essential - AI	One classification or semantic matching service, confidence, explanation, user review, evaluation set, deterministic fallback	Implement one function well rather than several untested functions
Desirable extension	Second AI function, basic assistant, generated narrative report, notification improvement	Add only after the essential workflow and tests pass
Future enhancement	Image recognition, predictive demand, full university integrations, advanced carbon model, autonomous workflow actions	Exclude from the semester minimum scope


8. 3 Two Person Work Allocation
One team member can lead the user interface, application workflow, and baseline search while the other leads the database, AI adapter, and deployment. Both members should review the requirements, data model, integration, tests, and documentation. The team should not divide the project into isolated halves that meet only at the end.
9 Legal Ethical Privacy Security and Policy Constraints
The project involves asset ownership, user identities, procurement values, maintenance history, photographs, documents, and AI service providers. These create legal and policy questions even in a prototype. UAE data protection law establishes requirements for maintaining the confidentiality of personal data, controlling how it is collected and processed, protecting individual rights, and managing cross-border data transfers. Khalifa University's public privacy page states that the institution uses security measures for personal information and limits disclosure to trusted parties and other permitted situations. This does not make a legal compliance determination. It identifies controls and approvals needed before real data or institutional systems are used.
Table 9 Constraint and Control Matrix
Constraint	Project Exposure	Required Control
Personal data	Names, accounts, activity history, contact information	Collect only necessary fields, control access, define purpose and retention, use approved data
Cross-border AI processing	Prompts or records may be sent to an external provider	Do not send restricted data without review of provider location, terms, retention, and approval
Asset ownership and transfer authorization	A recommendation could be mistaken for authority to transfer	Require authorized approval and receipt confirmation and preserve ownership history
Procurement and finance	Prices, budgets, savings, and supplier data may be confidential	Limit access, document data source, and separate sample values from actual records
Safety and hazardous assets	Some equipment may require inspection, certification, or specialist disposal	Flag restricted categories and prevent automated release or disposal
Intellectual property	Uploaded documents, images, model outputs, and code may have usage limits	Use approved content and licenses and record source and ownership
Security and audit	Unauthorized edits could change ownership, status, or decisions	Backend authorization, protected logs, secure sessions, validation, and access review
University policy	Internal acceptable-use, identity, data, network, and procurement rules apply	Consult current policy owners before integration or pilot deployment


9. 1 Ethical Use of AI
The ethical boundary is straightforward: AI may help people find, classify, compare, and explain resources, but accountable users make consequential decisions. Every recommendation should show the main factors, confidence or uncertainty, and the model or rule version. Users must be able to reject the recommendation and provide a reason.
9. 2 Privacy by Design
The prototype should avoid unnecessary personal fields. Access tests should verify that a requester cannot view another user's restricted activity, a department representative cannot approve an action outside the assigned role, and an external AI request does not include information that the model does not need. Logs should record relevant actions without copying full prompts or sensitive documents by default.
10 Risk Assessment
The risk assessment combines the concerns raised in Phase 1 with the additional data, AI, privacy, and policy risks. Likelihood and impact use a five-point scale. The score is likelihood multiplied by impact. Values from 15 to 25 require immediate treatment, values from 8 to 14 require planned mitigation and monitoring, and lower values remain in the register for review.
Table 10 Risk Register
Risk	L	I	Score	Mitigation
Scope exceeds two-person capacity	4	5	20	Finalize the essential scope and postpone optional features that could delay the core workflow.
Usable institutional data is unavailable	4	4	16	Use synthetic or approved anonymized data
AI matches are irrelevant or unstable	3	4	12	Create labeled evaluation set, store versions, retain filters and manual selection
External AI cost exceeds the plan	3	3	9	Cut back on AI functions
Privacy or policy violation	2	5	10	Minimize collected data, review service terms and obtain approval before real data
Unauthorized ownership or status change	2	5	10	Apply backend authorization, separate approval responsibilities and maintain protected audit records.
Integration work begins too late	4	4	16	Define interfaces during design and complete an early end-to-end demonstration
Sustainability figures are misleading	3	4	12	Note assumptions and possibilities and increase storage units
Safety restricted asset is released	2	5	10	Flag restricted asset categories and require inspection and authorized approval.
Final testing time is compressed	4	4	16	Test throughout development, automate repeatable checks and reserve the final week for corrections.


10. 1 Highest Priority Responses
The highest risks are schedule and data related. The team should respond before development by approving the minimum scope, generating a representative synthetic dataset, defining interfaces between application and AI modules, and preparing a working environment that either member can run. These controls reduce several risks at once because they make parallel work possible and prevent late discovery that the AI or workflow depends on missing information.
11 Consolidated Feasibility Scorecard
The weighted score is 3.65 out of 5. This result indicates that a prototype is feasible, but it does not remove the unresolved data, policy, and schedule gates. Technical feasibility raises the score because the baseline system uses established technologies. Data and compliance scores remain lower because institutional access and approval are not yet confirmed.
<img src="media/image2.png" title="Horizontal bar chart of preliminary feasibility scores showing technical 4.2, operational 3.8, financial 3.7, schedule 3.4, data and AI 3.3, and compliance and security 3.3 out of 5" style="width:6.25in;height:3.51563in" alt="Horizontal bar chart of preliminary feasibility scores showing technical 4.2, operational 3.8, financial 3.7, schedule 3.4, data and AI 3.3, and compliance and security 3.3 out of 5" />

Figure 2 Preliminary feasibility scores
Table 12 Weighted Feasibility Calculation
Dimension	Weight	Score	Weighted Contribution	Reason
Technical	20 percent	4.2	0.84	Established web and database approach and manageable architecture
Data and AI	20 percent	3.3	0.66	Feasible with controlled data but real data and model evidence remain uncertain
Operational	15 percent	3.8	0.57	Roles align with workflow but adoption and ownership need validation
Financial	15 percent	3.7	0.56	Low cash needed and production costs and realized benefits unknown
Schedule	15 percent	3.4	0.51	Feasible with strict scope and testing and final milestones are compressed
Compliance and security	15 percent	3.3	0.50	Prototype controls are feasible with institutional approval remains external
Total	100 percent		3.65	Conditional go for a controlled course prototype


11. 1 Interpretation
The scorecard supports progress to requirements analysis. Any unresolved high-impact gate can override the numerical score. The project should pause or reduce scope if the team cannot produce approved data, if an essential workflow depends completely on an external AI service, if authorization boundaries remain unclear, or if the baseline end-to-end workflow is not demonstrated before optional features consume the remaining schedule.
