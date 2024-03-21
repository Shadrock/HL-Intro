# Digital Library Fields
Documents in the Digital Library have extensive metadata that may be useful for document retrieval and for use by a generative AI model to better target specific information. The format for the metadata is the [MARC 21 Format](https://www.loc.gov/marc/bibliographic/) for Bibliographic Data, which carries bibliographic information about printed and manuscript textual materials, computer files, maps, music, continuing resources, etc.  

There are more than 66 MARC fields in use, including 472 sub categories of field `908__a`, which is intended as alternative to Collection Guides. This particular field contains a variety of categories of document that could be extremely helpful for vector searches and often differentiates various types of programming documents (e.g. case studies, M&E, lessons learned, management, proposal development, etc.). These sub categories could also be useful for identifying documents specific to particular humanitarian sectors, education, food Security, water and sanitation and hygiene, health, shelter, etc. 

Below is a subset of fields that the Digital Librarian suspects will be the most useful in a beta version of the chatbot. Below this are long lists of all fields. Some contextual and additional information has been left out of these lists for ease of reading and comprehension. For full documentation contact the digital librarian at `mcdlibrarian@mercycorps.org`. 

## Potentially Useful Fields
Below are those fields  thought to have the greatest utility for filtering and retrieving documents for the chatbot; whether via API or a data factory job. 

- `245__a`: Title
- `269__a`: Date (date authored or last revised)
- `336__a`: Document Type. Key Document Types (if it can influence how Chatbot prioritizes documents) are
    - Policy
    - Procedure
    - Guidance
    - Approach
    - Strategy Paper
    - Lessons Learned
    - Research Paper
    - Case Study
- `546__a`: Language

### Collections: 
Include documents with the field `980` 
Except:
- `980__a`: S2
- `980__a`: Waiting for enhancements

Ignore documents with the fields 991, 981 and 907.
- `991__a`: Restricted
- `981__a`: Archive Collections
- `907__a`: Archive Status (“Archived”)

## Field lists
Below are full lists of MARC fields and sub-fields.  

### Full list of MARC Fields
| MARC | Field name | Definition | Usage Notes |
| -------- |  --------  |  --------  | --------  |
| 245__a | Title | | 144 character limit |
| 246__a   | Variant Title | Alternate title | Use multiple fields for different type of info|
| 925__a   | Search BOOST | Pushes this record to the top of search results for this query | |
| 269__a   | Date | Authored date | Date on document - the date the document was authored or last revised. Exceptions: Proposals - submission date Reports - last date covered by report Policy - version date (if no version date, use effective date)|
| 906__a-1 | Last Reviewed Date | Tells users when the document was last reviewed by owner. | Apply when a document has been OK'd to remain in Library for another year. Use the date of approval by owner. If translations of an older document come in, use this for the full set of documents.<br><br>Remember to remove when new version is added!   
| 906__b-1 | Reviewed | Text to accompany field above | Always use in conjunction with `906__a-1`|
| 336__a   | Document Type | See Help | Policy and Procedure are controlled doctypes. We CANNOT USE THESE (or the Our Policies collection) without OK from PACT.|
| 7102_a   | Author | Team, department, or organization responsible for the doc | Do not use individual names.|
| 7102_a   | Author | | |
| 926__a   | Agency Author   | | |
| 520__a   | Abstract | Description, explanation. | Use for title translations and deccriptions. 164 character limit to brief (search) display. Will display full text on record. Can use multiple 520 fields. |
| 546__a-1 | Language 1 | Language(s) of the text | Start typing for options.<br><br>Use: Espanol for Spanish, Francais for French                                                                                                                     
| 546__a-2 | Language 2 |  | |
| 980__a   | Collection 1 | Major groupings/ pathways for navigation |  |
| 980__a   | Collection 2  | | |
| 907__a   | Archive Status | Document is in the Archives. | Only use in conjunction with `981` |
| 981__a   | Archive collection 1 | Major archive groupings | Base on 980 collections. Use with `907__a` |
| 981__a   | Archive collection 2  | |  |
| 690__a-1 | Sector | Document informs or pertains to a type of programming. | Based on 980 Sectors & Technical Guidance collections. Refer to GAIT for Program Docs and other docs linked to GAIT.| 
| 690__a-2 | Sector |  | |
| 653__a   | Keyword 1 | Tags to connect like concepts, especially ideas not clear from title. | Refer to list of team keywords. If term/phrase does not exist can type new one.<br><br>Drag to order alphabetically.<br><br>Can also use keywords to help push group of documents higher in search results.|
| 653__a   | Keyword 2 | | |
| 908__a   | Key Resource | Really important document for topic; selected by owner/team. | Intended as alternative to Collection Guides. If English version is key resource, mark translations as well.|
| 651__a-1 | Countries | Authored by or pertaining to country | Any country, not just MC countries |
| 651__a-2 | Countries | | |
| 691__a   | Region | Regions for all countries at 651 | Use only current MC regions. If country at 651 is in a current region, use this; if country not in a current region, leave blank. |
| 916__a   | Program Management Lifecycle | Pertains to or informs certain aspect(s) of PM lifecycle | Refers to guidance, forms, templates, etc. (esp. Program Development & Management), not used for Program Documents.<br><br>If document pertains to ALL aspects, check each option.|
| 918__a   | Employee Type (Working at MC) | Relevant to certain employee type(s). | Primarily HR related.|
| 917__a   | Function (Supporting Operations) | If document appears in any Supporting Ops subcollection, use equivalent function. | Allows for sorting by department/area within Supporting Ops collection. |
| 919__a   | Sharing Guidance: Mercy Corps only | Whether the document can be shared outside MC. | Internal/external: Anything on public site. Add dldoc link (85641y).Public: Country/MC fact sheets. MC only: Docs pertaining to internal operations, donors (all standard GAIT documents except fact sheets, public facing)|
| 923__a   | Finding Aids (Collection Guides) | Document is linked to collection guide (tool kits) | When removing or archiving documents, check this field to see if collection guide(s) must be updated as well.|
| 591__a   | Librarian Notes | | |
| 590__a   | Submission Notes | Instructions by submitter | Submission form, or paste from email. Use sparingly |
| 583__a   | Event Action | Type of management action should be taken on record. | Admin must manually apply actions each month.|
| 583__c   | Event Date | Date of management action | Use the first of the relevant month |
| 347__a   | File Format| 

#### Policy Information   

| MARC | Field name | Definition | Usage Notes |
| -------- |  --------  |  --------  | --------  |
| 920__a | Policy Effective Date | | |
| 920__b | Version Number | | |
| 920__c   | Version Date | | |
| 920__d   | Policy Type | | |
| 920__e   | Formal Policy Review Date | | |

#### Grant Information 

| MARC | Field name | Definition | Usage Notes |
| -------- |  --------  |  --------  | --------  |                                 
| 902__a   | GAIT ID | | One GAIT ID per field|
| 902__a   | GAIT ID | | |
| 902__c   | GAIT Funding Status | Is this grant funded? | Only for concepts and proposals. "Funded" only.|
| 902__b   | Donor | Donor from GAIT. Show subaward relationships in 520 abstract field.|
| 902__i   | Donor Type | | Match donor type in GAIT|
| 912__e   | Publication Date (upload date) | | |

#### Links
| MARC | Field name | Definition | Usage Notes |
| -------- |  --------  |  --------  | --------  |
| 767__t   | Translation Name | Link(s) to translations in DL | `767__t` & `767__w` are paired fields. Repeatable. |
| 767__w   | Record ID | Link(s) to translations in DL |
| 787__t   | See Also Name | Link to related documents in DL | `787__t` & `787__w` are paired fields. Repeatable.|
| 787__w   | Record ID | Link to related documents in DL |
| 85641y   | External link text | Link text for the field below. | `85641y` & `85641u` are paired fields. Repeatable. Use sparingly. More obviously a link if this field is omitted. Paste full link to make it obvious this is a link.|
| 85641u   | External link | | http:// - `85641y` & `85641u` are paired fields. Repeatable. `https://` If this is a publicly available document, put `http://dldocs.mercycorps.org/[filename]` link here. Use relative links to other records, pages `/record/12345`. ONLY USED FOR POLICY TRANSLATIONS. If there is an attachment on the record, this URL CANNOT be a library.mercycorps.org URL that includes a file path. One link is best because multiple links display on record on the same line (not stacked) so hard to read. |
| 85642y | DL Link Text | | `85642y` & `85642u` are paired fields. Repeatable. Used for links to DL searches, static pages, etc.|
| 85642u | DL Link | | `85642y` & `85642u` are paired fields. Repeatable. Use relative links.|
| 950__a   | submitter email address (form only) || Not included in form|
| 991__a   | Restricted | Document only visible to admins | Unpublished status. Must remove from `980`, `981`, `907`.

### Sub Categories of MARC field `908__a`

- Agency Overview - 3I Resources - 3I Guidelines
- Agency Overview - 3I Resources - 3I Impact, Influence & Innovation (3I) Awards 2017
- Agency Overview - 3I Resources - 3I Impact, Influence, Innovation Awards 2016
- Agency Overview - 3I Resources - 3I Innovations & Impact Competition 2012
- Agency Overview - 3I Resources - 3I Innovations & Impact Competition 2014
- Agency Overview - 3I Resources - 3I Innovations Competition 2009
- Agency Overview - 3I Resources - 3I Reports
- Agency Overview - 3I Resources - 4I Guidelines
- Agency Overview - 3I Resources - 4th I Awards 2019
- Agency Overview - 3I Resources - COVID 4I Awards 2020
- Agency Overview - About Mercy Corps - Corporate Governance
- Agency Overview - About Mercy Corps - Energy 4 Impact
- Agency Overview - About Mercy Corps - Leadership Transition & Accountability
- Agency Overview - About Mercy Corps - Mission & Vision for Change
- Agency Overview - About Mercy Corps - NGO Standards
- Agency Overview - About Mercy Corps - Organizational Structure & Leadership
- Agency Overview - Brand & Communications - Brand Guidelines & Templates
- Agency Overview - Brand & Communications - Crisis Communications
- Agency Overview - Brand & Communications - Fact Sheets for External Audiences - Country Fact Sheets
- Agency Overview - Brand & Communications - Fact Sheets for External Audiences - MC Fact Sheets
- Agency Overview - Brand & Communications - Internal Communications
- Agency Overview - Brand & Communications - RD Communications - Consent Forms
- Agency Overview - Brand & Communications - RD Communications - Key Messaging
- Agency Overview - Brand & Communications - Resource Development & Fundraising
- Agency Overview - Compass & Strategic Planning - Compass
- Agency Overview - Compass & Strategic Planning - Country Strategies
- Agency Overview - Compass & Strategic Planning - HQ Plans
- Agency Overview - Compass & Strategic Planning - Pathway to Possibility Companion
- Agency Overview - Compass & Strategic Planning - Pathway to Possibility Key Resources
- Agency Overview - Compass & Strategic Planning - Pathway to Possibility Process
- Agency Overview - Compass & Strategic Planning - Program Department Redesign
- Agency Overview - Compass & Strategic Planning - Regional Strategies
- Agency Overview - Compass & Strategic Planning - Strategic Planning Resources
- Agency Overview - Compass & Strategic Planning - Strategic Planning Resources - Country Strategy Development
- Agency Overview - Compass & Strategic Planning - Strategic Planning Resources - Country Strategy Realization Fund
- Agency Overview - Compass & Strategic Planning - Strategic Planning Resources - Donor Strategy Alignment
- Agency Overview - Compass & Strategic Planning - Strategic Planning Resources - General Strategy Development
- Agency Overview - Impact - Impact Briefs
- Agency Overview - Influence - Advocacy in Action
- Agency Overview - Influence - COVID
- Agency Overview - Influence - PA Team
- Agency Overview - Influence - Peace - Key Resources/Top Ten
- Agency Overview - Influence - Peace - Policy Briefs
- Agency Overview - Influence - Peace - Research
- Agency Overview - Influence - Peace - Talking Points
- Agency Overview - Influence - Peace - Technical Capacity, Approaches, Fact Sheets
- Agency Overview - Innovation - Community Investment Trust
- Agency Overview - Innovation - Innovation at Mercy Corps
- Agency Overview - Innovation - Social Ventures
- Program Development - CARM - About - Getting Started
- Program Development - CARM - About - Toolkit
- Program Development - CARM - About - Understanding CARM
- Program Development - CARM - Automation
- Program Development - CARM - CARM Policy
- Program Development - CARM - CARM in Emergencies
- Program Development - CARM - CARM in Emergencies - Established Country
- Program Development - CARM - CARM in Emergencies - New Country
- Program Development - CARM - CARM in Emergencies - Standards
- Program Development - CARM - CARM in Proposals
- Program Development - CARM - CARM with Partners
- Program Development - CARM - Collecting Feedback
- Program Development - CARM - Logging Feedback
- Program Development - CARM - MEL
- Program Development - CARM - Quality
- Program Development - CARM - Reporting
- Program Development - CARM - Staffing
- Program Development - CARM - Taking Action
- Program Development - Case Studies
- Program Development - Lessons Learned
- Program Development - Monitoring Evaluation - Beneficiary Counting
- Program Development - Monitoring Evaluation - Data Collection, Management & Analysis
- Program Development - Monitoring Evaluation - Final Internal Performance Reviews
- Program Development - Monitoring Evaluation - MEL External Resources
- Program Development - Monitoring Evaluation - MEL Policy
- Program Development - Monitoring Evaluation - MEL Policy Guidance
- Program Development - Monitoring Evaluation - MEL Policy Resources
- Program Development - Monitoring Evaluation - MEL Resilience Measurement
- Program Development - Monitoring Evaluation - MEL Technology
- Program Development - Monitoring Evaluation - MEL Tools & Methods
- Program Development - Monitoring Evaluation - MEL at Mercy Corps
- Program Development - Monitoring Evaluation - MER-MSA
- Program Development - Monitoring Evaluation - Tola
- Program Development - Program Management - Community Accountability
- Program Development - Program Management - Complex Program Boards
- Program Development - Program Management - Complex Program Learning
- Program Development - Program Management - Complex Program Procedures
- Program Development - Program Management - Complex Program Reports
- Program Development - Program Management - Complex Program Reviews
- Program Development - Program Management - Complex Program Start-Up
- Program Development - Program Management - Complex Program Templates
- Program Development - Program Management - PM@MC
- Program Development - Program Management - PM@MC Training & Certifications
- Program Development - Program Management - PMMC Closure - Closure Plan (S19)
- Program Development - Program Management - PMMC Closure - Internal Review (S20)
- Program Development - Program Management - PMMC Closure - Program File Completion (S21)
- Program Development - Program Management - PMMC Design - Budget (S7)
- Program Development - Program Management - PMMC Design - Cash Goods Infrastructure (S6)
- Program Development - Program Management - PMMC Design - Expertise (S8)
- Program Development - Program Management - PMMC Design - Logic Model (S5)
- Program Development - Program Management - PMMC Design - Program File Creation (S4)
- Program Development - Program Management - PMMC Design - Program Manager (S3)
- Program Development - Program Management - PMMC External
- Program Development - Program Management - PMMC Identification - Analysis (S2)
- Program Development - Program Management - PMMC Identification - Stakeholders (S1)
- Program Development - Program Management - PMMC Implementation - Adaptive Management (S15)
- Program Development - Program Management - PMMC Implementation - CARM Management (S18)
- Program Development - Program Management - PMMC Implementation - MEL (S17)
- Program Development - Program Management - PMMC Implementation - Quality Control (S16)
- Program Development - Program Management - PMMC Planning - CARM Procedures (S11)
- Program Development - Program Management - PMMC Planning - Participant SOPs (S13)
- Program Development - Program Management - PMMC Planning - Planning Coordination (S12)
- Program Development - Program Management - PMMC Planning - Program File Maintenance (S14)
- Program Development - Program Management - PMMC Planning - Program Implementation Plan (S10)
- Program Development - Program Management - PMMC Planning - Start-up Planning (S9)
- Program Development - Program Management - PMMC Policy
- Program Development - Program Management - PMMC Related
- Program Development - Program Management - Program Minimum Standards (Cash, Goods)
- Program Development - Program Management - Program Performance General
- Program Development - Program Management - Program Record Retention & Archiving
- Program Development - Program Management - Remote Program Management
- Program Development - Program Management - Strategic Leadership
- Program Development - Proposal Dev - Complex Program Proposals
- Program Development - Proposal Dev - Donor Guidelines
- Program Development - Proposal Dev - Planning & Initial - Matching Contributions
- Program Development - Proposal Dev - Planning & Initial - Proposal Go No-Go
- Program Development - Proposal Dev - Planning & Initial - Proposal Planning
- Program Development - Proposal Dev - Planning & Initial - Proposal Planning Assessment Tools
- Program Development - Proposal Dev - Planning & Initial - Proposal Planning Collaborative Relationships
- Program Development - Proposal Dev - Program Design - Program Design Collaborative Relationships
- Program Development - Proposal Dev - Program Design - Program Design Key Steps
- Program Development - Proposal Dev - Program Design - Proposal Cost Proposal Preparation
- Program Development - Proposal Dev - Program Design - Proposal M&E Tools
- Program Development - Proposal Dev - Program Design - Proposal Writing & Reviewing
- Program Development - Proposal Dev - Proposal Development New Initiatives Team
- Program Development - Proposal Dev - Proposal Minimum Standards & Policies
- Program Development - Proposal Dev - Proposal Pre-Positioning
- Program Development - Research
- Program Development - Subaward Financial Management Manual - All Subawards
- Program Development - Subaward Financial Management Manual - Mercy Corps Europe
- Program Development - Subaward Financial Management Manual - Mercy Corps Global
- Program Development - Subawards Other Guidance - Contracts v Subawards
- Program Development - Subawards Other Guidance - Proposals
- Program Documents - Agreements
- Program Documents - Assessments
- Program Documents - Evaluations
- Program Documents - Final Reports
- Program Documents - Other Program Documents
- Program Documents - Program Performance Reviews
- Program Documents - Program Proposals
- Program Documents - Progress Reports
- Sectors - Agriculture - Agribusiness Development
- Sectors - Agriculture - Agriculture - AgriFin
- Sectors - Agriculture - Agriculture - Market Systems Development
- Sectors - Agriculture - Agriculture - Resilient Agriculture
- Sectors - Agriculture - Agriculture Food Safety & Nutrition
- Sectors - Agriculture - Agriculture Monitoring & Evaluation
- Sectors - Agriculture - Agriculture Overview & Approaches
- Sectors - Agriculture - Agriculture Thought Leadership & Learning
- Sectors - Agriculture - Production - Crop Production
- Sectors - Agriculture - Production - Livestock Production
- Sectors - Agriculture - Production - Pests & Disease Management
- Sectors - Agriculture - Production - Storage Techniques & Technologies
- Sectors - Cash Transfers - Cash Quality Assurance
- Sectors - Cash Transfers - Cash Transfer Programming Approaches & Policy
- Sectors - Cash Transfers - Cash Transfer Programming Toolkit - Cash Transfer Implementation
- Sectors - Cash Transfers - Cash Transfer Programming Toolkit - Cash for Work
- Sectors - Cash Transfers - Cash Transfer Programming Toolkit - Methodology
- Sectors - Cash Transfers - Cash Transfer Programming Toolkit - Vouchers & Fairs Implementation
- Sectors - Cash Transfers - Cash Transfers - Payment Mechanisms & E-Transfers
- Sectors - Cash Transfers - Cash Transfers Monitoring & Evaluation
- Sectors - Cash Transfers - Cash Transfers Nepal CVA
- Sectors - Cash Transfers - Cash Transfers Thought Leadership & Learning
- Sectors - Cash Transfers - Consortium Guidance
- Sectors - Cash Transfers - Other Cash Transfers Documents
- Sectors - Education
- Sectors - Emergency - Emergency Analysis - Emergency After Action Reviews
- Sectors - Emergency - Emergency Analysis - Humanitarian Analysis
- Sectors - Emergency - Emergency Analysis - Humanitarian Capacity Building
- Sectors - Emergency - Emergency Preparedness - Emergency Preparedness Planning Workshop
- Sectors - Emergency - Emergency Preparedness - Emergency Preparedness Plans (EPP)
- Sectors - Emergency - Humanitarian Response - Emergency - Sectors & Technical Guidance
- Sectors - Emergency - Humanitarian Response - Humanitarian Response Approach
- Sectors - Emergency - Humanitarian Response - Humanitarian Response M&E
- Sectors - Emergency - Humanitarian Response - Humanitarian Response Tools & Guidelines
- Sectors - Environment & Energy - Carbon
- Sectors - Environment & Energy - Climate Change Adaptation
- Sectors - Environment & Energy - Climate Smart
- Sectors - Environment & Energy - Disaster Risk Reduction
- Sectors - Environment & Energy - Energy Access
- Sectors - Environment & Energy - Environment & Energy Approaches
- Sectors - Environment & Energy - Environmental Compliance
- Sectors - Environment & Energy - Other Environment & Energy Documents
- Sectors - Environment & Energy - Water Security
- Sectors - Financial Inclusion - Financial Inclusion Approaches & Strategies
- Sectors - Financial Inclusion - Financial Inclusion Thought Leadership & Learning
- Sectors - Financial Inclusion - Financial Products & Services
- Sectors - Financial Inclusion - Other Financial Inclusion Documents
- Sectors - Food Security & Nutrition - Food Security
- Sectors - Food Security & Nutrition - Food Security Commodities
- Sectors - Food Security & Nutrition - Food Security Thought Leadership & Learning
- Sectors - Food Security & Nutrition - Nutrition
- Sectors - Food Security & Nutrition - Other Food Security Documents
- Sectors - Gender - Gender Approaches
- Sectors - Gender - Gender Guidebooks & Tools
- Sectors - Gender - Gender Policies & Procedures
- Sectors - Gender - Gender Thought Leadership & Learning
- Sectors - Gender - Other Gender Documents
- Sectors - Goods Distribution Material Aid
- Sectors - Goods Distribution Programming
- Sectors - Governance - Community Mobilization
- Sectors - Governance - Governance Approaches
- Sectors - Governance - Governance Thought Leadership & Learning
- Sectors - Governance - Local Advocacy Toolkit
- Sectors - Governance - Local Civil Society Partnerships - Operationalizing Local Partnerships
- Sectors - Governance - Local Civil Society Partnerships - Organizational Capacity
- Sectors - Governance - Other Governance Documents
- Sectors - Health - Health Approaches
- Sectors - Health - Infectious Diseases - Avian Influenza
- Sectors - Health - Infectious Diseases - COVID-19
- Sectors - Health - Infectious Diseases - Ebola
- Sectors - Health - Infectious Diseases - H1N1 Swine Flu
- Sectors - Health - Infectious Diseases - HIV/AIDS
- Sectors - Health - Maternal & Child Health
- Sectors - Health - Other Health Documents
- Sectors - Health - Thought Leadership & Learning
- Sectors - Infrastructure
- Sectors - Market Development - Market Analysis & Assessments
- Sectors - Market Development - Market Development Approaches
- Sectors - Market Development - Market Development Programming
- Sectors - Market Development - Market Development Thought Leadership & Learning
- Sectors - Market Development - Other Market Development Documents
- Sectors - Market Development - Private Sector Engagement
- Sectors - Peace & Conflict - Addressing Root Causes
- Sectors - Peace & Conflict - Do No Harm
- Sectors - Peace & Conflict - Negotiation & Mediation
- Sectors - Peace & Conflict - Other Peace & Conflict Documents
- Sectors - Peace & Conflict - Peace & Conflict Approaches
- Sectors - Peace & Conflict - Peace & Conflict Monitoring & Evaluation
- Sectors - Peace & Conflict - Peace & Conflict Thought Leadership & Learning
- Sectors - Peace & Conflict - Preventing/Countering Violent Extremism
- Sectors - Peace & Conflict - Youth & Conflict
- Sectors - Protection - Child Protection - Cash for Protection
- Sectors - Protection - Child Protection - Child Safeguarding
- Sectors - Protection - Disability Inclusion
- Sectors - Protection - Gender Based Violence - General
- Sectors - Protection - Gender Based Violence Prevention
- Sectors - Protection - Gender Based Violence Response
- Sectors - Protection - Protection Approaches - General
- Sectors - Protection - Protection Approaches - Mainstreaming
- Sectors - Protection - Protection Monitoring
- Sectors - Protection - Protection Thought Leadership & Learning
- Sectors - Protection - Psychosocial Support - Child Friendly Spaces
- Sectors - Protection - Psychosocial Support - Comfort for Kids
- Sectors - Protection - Psychosocial Support - General
- Sectors - Protection - Psychosocial Support - Sports
- Sectors - Refugees/IDPs/Returnees
- Sectors - Resilience - Other Resilience Documents
- Sectors - Resilience - Resilience Approaches
- Sectors - Resilience - Resilience Guidebooks & Tools
- Sectors - Resilience - Resilience Measurement & Evaluation
- Sectors - Resilience - Resilience Thought Leadership & Learning
- Sectors - Resilience - Strategic Resilience Assessments (STRESS)
- Sectors - Technical Support
- Sectors - Technology - DLT & Cryptocurrency
- Sectors - Technology - Data Analytics & Measurement
- Sectors - Technology - Design
- Sectors - Technology - Digital Identity
- Sectors - Technology - Field Technology Testing Program (FTTP)
- Sectors - Technology - Mobile Technology
- Sectors - Technology - Other Technology Documents
- Sectors - Technology - Remote Sensing
- Sectors - Technology - T4D Team
- Sectors - Technology - Technology Approaches
- Sectors - Technology - WiFi & Connectivity
- Sectors - WASH - WASH Approaches
- Sectors - WASH - WASH Monitoring & Evaluation
- Sectors - WASH - WASH Sanitation
- Sectors - WASH - WASH Thought Leadership & Learning
- Sectors - WASH - WASH Water Supply
- Sectors - WASH - WASH, Gender & Protection
- Sectors - Youth - Adolescents in Emergencies
- Sectors - Youth - Curriculum - 321 Move Curriculum
- Sectors - Youth - Curriculum - Skills and Knowledge for Youth Leaders (SKYLS)
- Sectors - Youth - Curriculum - Transferable Skills for Youth
- Sectors - Youth - Curriculum - Youth Curriculum - Other Youth Documents
- Sectors - Youth - Curriculum - Youth Curriculum - Youth Curriculum Overview
- Sectors - Youth - Curriculum - Youth Curriculum - Youth Curriculum: Conflict Management
- Sectors - Youth - Curriculum - Youth Curriculum - Youth Curriculum: Global Citizenship
- Sectors - Youth - Curriculum - Youth Curriculum - Youth Curriculum: Life Skills
- Sectors - Youth - Curriculum - Youth Curriculum - Youth Curriculum: Psychosocial
- Sectors - Youth - Curriculum - Youth Curriculum - Youth Curriculum: Social Entrepreneurship/Civil Society
- Sectors - Youth - Curriculum - Youth Curriculum - Youth Curriculum: Workforce Development
- Sectors - Youth - Youth Approaches
- Sectors - Youth - Youth Employment & Entrepreneurship
- Sectors - Youth - Youth Engagement
- Sectors - Youth - Youth Guidebooks & Tools
- Sectors - Youth - Youth Thought Leadership & Learning
- Supporting Operations - Administration - Facilities
- Supporting Operations - Administration - Field Administration
- Supporting Operations - Administration - Field Office Management OIB
- Supporting Operations - Administration - HQ Office Management
- Supporting Operations - Administration - HR Administration - Compensation & Benefits Templates
- Supporting Operations - Administration - HR Administration - HR Systems
- Supporting Operations - Administration - HR Administration - Handbook Templates
- Supporting Operations - Administration - HR Administration - Handbook Templates OIB
- Supporting Operations - Administration - HR Administration - PAFs
- Supporting Operations - Administration - HR Administration - Performance Forms
- Supporting Operations - Administration - HR Administration - Procedures - Discipline & Termination
- Supporting Operations - Administration - HR Administration - Procedures - Filing
- Supporting Operations - Administration - HR Administration - Procedures - Hiring - Candidate Selection
- Supporting Operations - Administration - HR Administration - Procedures - Hiring HQ & Expats
- Supporting Operations - Administration - HR Administration - Procedures - Hiring National Staff
- Supporting Operations - Administration - HR Administration - Procedures - Offboarding
- Supporting Operations - Administration - HR Administration - Rosters & Org Charts
- Supporting Operations - Administration - HR Administration - US Employment Notices
- Supporting Operations - Administration - Ineligibility & Compliance Checking
- Supporting Operations - Administration - Insurance & Risk Management
- Supporting Operations - Administration - Internal Audits
- Supporting Operations - Administration - Knowledge Management
- Supporting Operations - Administration - Policy Development
- Supporting Operations - Consultants
- Supporting Operations - Coronavirus - Continuity
- Supporting Operations - Coronavirus - Finance
- Supporting Operations - Coronavirus - HR Benefits
- Supporting Operations - Coronavirus - HR Health
- Supporting Operations - Coronavirus - HR Onboarding
- Supporting Operations - Coronavirus - HR Recruitment
- Supporting Operations - Coronavirus - Preparedness
- Supporting Operations - Coronavirus - Programming
- Supporting Operations - Coronavirus - Team Communications
- Supporting Operations - Coronavirus - Travel
- Supporting Operations - Coronavirus - Vaccines
- Supporting Operations - Ethics
- Supporting Operations - Finance - Accounting Reference
- Supporting Operations - Finance - Field Finance Forms
- Supporting Operations - Finance - Field Finance Manual
- Supporting Operations - Finance - Field Finance Operations - Budgeting
- Supporting Operations - Finance - Field Finance Operations - Staffing
- Supporting Operations - Finance - Finance Award Management - Budgeting
- Supporting Operations - Finance - Finance Award Management - Policies
- Supporting Operations - Finance - Finance Award Management - Regulations Compliance
- Supporting Operations - Finance - Finance Corporate Docs - Audited Financial Statements
- Supporting Operations - Finance - Finance Corporate Docs - IRS Form 990
- Supporting Operations - Finance - Finance Corporate Docs - Other
- Supporting Operations - Finance - Finance Costing Ref - Indirect Cost Rates (NICRA)
- Supporting Operations - Finance - Finance Costing Ref - Internal Costing Reference
- Supporting Operations - Finance - Financial Analysis
- Supporting Operations - Finance - HQ Finance
- Supporting Operations - Finance - Ineligibility & Compliance Checking
- Supporting Operations - Finance - MCE Finance
- Supporting Operations - Finance - Navigator - Field Connect Procedures & Guides
- Supporting Operations - Finance - Navigator - Navigator Procedures - Navigator Award Management (AM)
- Supporting Operations - Finance - Navigator - Navigator Procedures - Navigator Cash Management - Country (CMC)
- Supporting Operations - Finance - Navigator - Navigator Procedures - Navigator Country Financial Management (CFM)
- Supporting Operations - Finance - Navigator - Navigator Procedures - Navigator Country Payment Processing (CPP)
- Supporting Operations - Finance - Navigator - Navigator Procedures - Navigator Country Payroll (CPR)
- Supporting Operations - Finance - Navigator - Navigator Procedures - Navigator General Ledger Management (GLM)
- Supporting Operations - Finance - Navigator - Navigator Procedures - Navigator References
- Supporting Operations - Finance - Navigator - Navigator Procedures - Navigator Reports (RPT)
- Supporting Operations - Finance - Navigator - Navigator Procedures - Navigator System (SYS)
- Supporting Operations - Finance - Navigator - Other Navigator Reference Guides
- Supporting Operations - Finance - Navigator - ProSource Finance - ProSource Finance Country Payment Processing
- Supporting Operations - Finance - Navigator - ProSource Finance - ProSource Finance Invoice Processing
- Supporting Operations - Finance - Navigator - ProSource Finance - ProSource Finance References
- Supporting Operations - Finance - Navigator - Procedure Flow Diagrams
- Supporting Operations - Finance - Navigator User Trainers Kit
- Supporting Operations - Finance - Other Finance & Compliance Documents
- Supporting Operations - Finance - Timekeeping - Employees
- Supporting Operations - Finance - Timekeeping - Finance
- Supporting Operations - Finance - Timekeeping - HR
- Supporting Operations - Finance - Timekeeping - Supervisors
- Supporting Operations - Information Technology - Anti-Virus & Safe Computing
- Supporting Operations - Information Technology - Data Protection
- Supporting Operations - Information Technology - Field IT - Guidelines
- Supporting Operations - Information Technology - Field IT - Office Solar
- Supporting Operations - Information Technology - Field IT - Satellite Communications
- Supporting Operations - Information Technology - IT Policies & Standards
- Supporting Operations - Information Technology - Information Tools & Sites
- Supporting Operations - Information Technology - Portland IT
- Supporting Operations - Information Technology - System Administration
- Supporting Operations - Legal - Ethics
- Supporting Operations - Legal - Export Compliance
- Supporting Operations - Legal - Non-Disclosure Agreements
- Supporting Operations - Legal - Organizational Statements
- Supporting Operations - Legal - Other Legal Documents
- Supporting Operations - Legal - Templates for Contracts & MOUs
- Supporting Operations - Procurement & Logistics - Administrative Close-Out
- Supporting Operations - Procurement & Logistics - Asset Management
- Supporting Operations - Procurement & Logistics - Facilities & Office Management
- Supporting Operations - Procurement & Logistics - Fleet Management
- Supporting Operations - Procurement & Logistics - Operations Management Guidance
- Supporting Operations - Procurement & Logistics - Procurement - Electronic Procurement System
- Supporting Operations - Procurement & Logistics - Procurement - Field Procurement (pre-FP3)
- Supporting Operations - Procurement & Logistics - Procurement - Field Procurement Policies & Procedures (FP3)
- Supporting Operations - Procurement & Logistics - Procurement - Field Procurement Policies FP3 ProSource
- Supporting Operations - Procurement & Logistics - Procurement - HQ Procurement Policies & Procedures (HP3)
- Supporting Operations - Procurement & Logistics - Procurement - Other Procurement Documents
- Supporting Operations - Procurement & Logistics - Procurement - Procurement Finance & Compliance
- Supporting Operations - Procurement & Logistics - Procurement - Procurement Position Descriptions
- Supporting Operations - Procurement & Logistics - Procurement - Procurement Training Materials
- Supporting Operations - Procurement & Logistics - Warehousing
- Supporting Operations - Recruitment - Hiring - Candidate Selection
- Supporting Operations - Recruitment - Hiring HQ & Expats
- Supporting Operations - Recruitment - Hiring National Staff
- Supporting Operations - Recruitment - Interns & Volunteers
- Supporting Operations - Recruitment - Offboarding
- Supporting Operations - Recruitment - Position Descriptions - Administration PDs
- Supporting Operations - Recruitment - Position Descriptions - Ethics PDs
- Supporting Operations - Recruitment - Position Descriptions - Field Leadership PDs
- Supporting Operations - Recruitment - Position Descriptions - Finance & Compliance PDs
- Supporting Operations - Recruitment - Position Descriptions - Operations PDs
- Supporting Operations - Recruitment - Position Descriptions - PAQ PDs
- Supporting Operations - Recruitment - Position Descriptions - Program Management PDs
- Supporting Operations - Recruitment - Position Descriptions - Sector PDs
- Supporting Operations - Recruitment - Position Descriptions OIB
- Supporting Operations - Security - Constant Companions
- Supporting Operations - Security - Field Security Management OIB
- Supporting Operations - Security - Field Security Manual
- Supporting Operations - Security - Security Management
- Supporting Operations - Security - Security Management Plans
- Supporting Operations - Security - Security Minimum Standards
- Supporting Operations - Security - Security Sample SOPs
- Supporting Operations - Travel - Atlas Travel
- Supporting Operations - Travel - Fly America
- Supporting Operations - Travel - MC Europe Travel
- Supporting Operations - Travel - Travel Forms & Templates
- Supporting Operations - Travel - Travel Policies & Procedures
- Supporting Operations - Travel - Travel Safety - General
- Supporting Operations - Travel - Visa Letter Templates
- Working at MC - Benefits - Equitable Compensation
- Working at MC - Benefits - General Compensation & Payroll
- Working at MC - Benefits - Health & Safety
- Working at MC - Benefits - MCE Expat Benefits Summaries
- Working at MC - Benefits - MCE Expat EARP
- Working at MC - Benefits - MCE Expat Insurance
- Working at MC - Benefits - National Staff
- Working at MC - Benefits - US Expat Benefits Summaries
- Working at MC - Benefits - US Expat EARP
- Working at MC - Benefits - US Expat Family Leave
- Working at MC - Benefits - US Expat Hardship
- Working at MC - Benefits - US Expat Insurance
- Working at MC - Benefits - US Expat Retirement
- Working at MC - Benefits - US HQ Benefits Summaries
- Working at MC - Benefits - US HQ EARP
- Working at MC - Benefits - US HQ Family Leave
- Working at MC - Benefits - US HQ Insurance
- Working at MC - Benefits - US HQ Notices
- Working at MC - Benefits - US HQ Retirement
- Working at MC - Careers - Careers at Mercy Corps
- Working at MC - Careers - Cornerstones of Leadership
- Working at MC - Careers - Emerging Leaders Program (ELP)
- Working at MC - Careers - Female Leadership Initiative (FLI)
- Working at MC - Careers - Next Generation Leadership
- Working at MC - Careers - People with Possibility
- Working at MC - Careers - Senior Management Team Development
- Working at MC - Careers - Skills Development
- Working at MC - Careers - Women in Leadership
- Working at MC - Culture - Organizational Learning
- Working at MC - Culture - Our Culture & Values
- Working at MC - Gender, Diversity & Inclusion
- Working at MC - Onboarding
- Working at MC - Our Policies - Award Management
- Working at MC - Our Policies - Code of Conduct
- Working at MC - Our Policies - Finance
- Working at MC - Our Policies - Governance and Legal
- Working at MC - Our Policies - Human Resources and Talent Acquisition
- Working at MC - Our Policies - Information Technology
- Working at MC - Our Policies - Operations and Management Services
- Working at MC - Our Policies - Programming, Research and Advocacy
- Working at MC - Our Policies - Resource Development
- Working at MC - Our Policies - Safety and Security
- Working at MC - Performance

