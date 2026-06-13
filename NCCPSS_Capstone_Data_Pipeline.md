# Capstone Project - NCCPSS Database Design
**1. Problem Statement**

The North Carolina Certified Peer Support Specialist Program manages certification for nearly
7,000 peers across North Carolina. Program data is currently stored across multiple Excel and
Access files. This makes it difficult to combine data, track participants over time, ensure
accuracy, and perform analysis.
Because there is no centralized database, the program faces challenges with reporting,
longitudinal tracking, and decision making based on data. This limits the program’s ability to
identify trends, monitor progress, and improve coordination with partners and stakeholders.
The goal of this project is to design a centralized, accurate, and well structured database that
supports certification management, reporting, and analysis for the program.

**2. Background**

The NCCPSS Program operates in partnership with the North Carolina Department of Health
and Human Services and the Division of Mental Health, Developmental Disabilities, and
Substance Use Services. The program oversees certification and ongoing program
management for thousands of peer support specialists statewide.
Historical data has grown over time and is now spread across disconnected systems. This
creates inefficiencies and increases the risk of data errors. A unified system would improve
oversight, consistency, and long term program evaluation.

**3. Stakeholders**

- UNC School of Social Work  
- North Carolina Certified Peer Support Specialist Program  
- North Carolina Department of Health and Human Services  
- Division of Mental Health, Developmental Disabilities, and Substance Use Services  
- Program staff, trainers, and partners  
- Certified peer support specialists  

**4. Team & Roles**

- Taylor Baldwin
- Claudia Dare
- Michael Borasy
- Usman Siddiqu

**5. Data Plan**

The NCCPSS data currently comes from multiple sources, including a Microsoft Access registry,
a Drupal-based application and recertification system, and supplemental Excel files. Our data
plan focuses on consolidating these sources into a single, well structured system that separates
stable participant information from time based records such as certification, recertification, and
employment outcomes. We developed a data dictionary and a proposed data structure to guide
data cleaning, validation, and historical tracking. This approach supports longitudinal analysis,
improves reporting accuracy, and allows for future scalability and automation.
Existing data sources include Access databases, application forms, workflows, and reporting
outputs. The team will assess all current data sources to identify required fields, data quality
issues, and reporting needs.
Data will be cleaned, standardized, and migrated into a new centralized database designed to
support tracking over time and analysis.
Additional data sources include the PS Registry Access database and Drupal, which has been
used for recertification data starting in 2024. Data from these systems may be exported to CSV
or JSON formats for analysis and integration. Some data cleaning and standardization will be
required due to manual data entry and inconsistent field naming.

**6. Approach & Methodology**

The team will first assess current systems and data sources to define requirements. A database
structure will then be designed to support consolidation, tracking, and reporting. Existing data
will be migrated into the new system and validated for accuracy.
The system will be tested with program staff and refined based on feedback before broader
implementation. As part of the database design process, the team will create a data dictionary
to clearly define fields, data types, and relationships, as a formal data dictionary does not
currently exist. The database schema will be designed to support certification history over time
and allow for future automation of data updates.

**7. Timeline & Milestones**

Assess existing data and systems
Design database schema
Clean and migrate data
Test system with stakeholders
Refine and finalize database
Prepare final presentation and documentation
Dates to be updated as the project progresses

**8. Deliverables & Presentations**

Centralized database for the NCCPSS Program
Clean and documented data structure
Ability to track participants over time
Standardized reporting and workflows
Visualizations or dashboards for program insights
Final presentation and project documentation

**9. Risks**

Some potential risks include inconsistencies between the Access and Drupal data, limited time
within the semester, and possible changes in stakeholder needs. We also need to consider
university infrastructure policies and any Microsoft licensing or funding requirements tied to
long-term use of Fabric. Although the dashboards will present aggregate and anonymized data,
final implementation may still depend on institutional approval and technical validation.

**10. Team Literature Review**

Our team reviewed academic research, government reports, and industry case studies related
to peer support programs, legacy data systems, data modernization, and reporting and
analytics. The literature shows that fragmented systems like Excel and Access limit reporting,
historical tracking, and decision making, especially for public health and workforce programs.
Prior work emphasizes the importance of centralized data structures, longitudinal tracking, and
reliable reporting to evaluate outcomes such as employment and retention. These findings
directly support the goals of the NCCPSS project and inform our approach to database design
and analysis.

**11. Data Visualization**

To better understand the structure and quality of the NCCPSS data, the team created initial exploratory visualizations. These include charts showing certification status distribution, demographic patterns such as gender and education level, employment characteristics, and age distribution.

Visualization code and outputs can be viewed here:  
https://github.com/uncsdss/992-S26-TeamB3/blob/main/data_visualizations.ipynb

**12. Data Analysis**

As part of the database design process, the team conducted descriptive data analysis on the NCCPSS datasets during the data cleaning and integration stages. Using PySpark notebooks in Microsoft Fabric, we examined record counts, null value patterns, duplicate detection, and field consistency across the Drupal and Registry systems.

We standardized key fields such as names, gender, employment indicators, wage values, and dates of birth to improve data quality and support accurate record matching. Tiered matching logic was then applied to identify the same individuals across systems using email, name combined with date of birth, and name combined with ZIP code. This helped the team estimate overlap between sources and better understand the number of unique participants in the program.

In the silver layer, these descriptive analytics steps informed the database schema design by revealing which fields were reliable identifiers, which attributes required historical tracking, and where data quality risks existed. The analysis also supported the creation of a cross-reference identity layer that will allow the program to track individuals consistently across systems going forward.

**13. Key Insight**

The data integration and matching process revealed that a significant portion of records existed only in one system, highlighting fragmentation between Drupal and the Registry. Email proved to be the strongest identifier for matching individuals, while name and date of birth provided additional coverage. The creation of a cross-reference identity layer allows for consistent tracking of individuals across systems going forward. Initial visualizations also highlighted patterns in gender distribution, employment status, and recovery experience, though some fields showed signs of missing or inconsistent data.

**14. Project Outcome**

This project resulted in the design of a centralized and structured database system for the NCCPSS program. The team developed a data pipeline that cleans, standardizes, and integrates data from multiple sources, along with an identity layer that enables tracking individuals across systems. The final output includes a proposed database schema and dashboards that support reporting, analysis, and decision-making. Overall, the project provides a foundation for improved data management, better visibility into program outcomes, and more efficient reporting processes.

**15. Future Work**

As part of the project handoff, all code, documentation, and data structures have been organized and delivered to stakeholders, including notebooks, data dictionaries, and guidance on how the system is structured. This allows the NCCPSS team to understand, maintain, and build upon the work completed.

Future work includes implementing the database in a production environment, automating data ingestion from Drupal and Registry systems, and expanding dashboard capabilities to support deeper program insights. Additional refinement of matching logic and continued data quality improvements will further strengthen the system over time.


**References**
1. Substance Abuse and Mental Health Services Administration (SAMHSA). Peer Support
Services. https://www.samhsa.gov/brss-tacs/recovery-support-tools/peers
2. Siantz, E. et al. (2025). Employment trajectories of recently certified peer support
specialists. https://pmc.ncbi.nlm.nih.gov/articles/PMC12320789/
3. Kadakia, K. T. et al. (2023). Transforming Public Health Data Systems to Advance
Population Health. https://pmc.ncbi.nlm.nih.gov/articles/PMC10126962/
4. Assunção, W. K. G. et al. (2025). Contemporary software modernization. ACM
Transactions on Software Engineering and Methodology.
5. Babucea, A.-G. (2025). Database scalability and performance challenges.
6. Kumar, M. et al. (2025). Building healthcare research data platforms using Microsoft
Fabric.
7. Panda, S. P. (2025). Mastering Microsoft Fabric.
8. Astral Forest. Data Platform Migration Case Study.
https://www.astralforest.com/post/data-platform-migration-a-detailed-guide-case-study
9. CDC. Ohio Human Services Data Warehouse Case Study.
https://www.cdc.gov/data-modernization/media/pdfs/2025/03/OH_Case_Study_final-repo
rt_cleared_508.pdf
10. Chanda, D. (2024). Automated ETL Pipelines for Modern Data Warehousing.
https://www.researchgate.net/publication/390849393
