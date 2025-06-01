---
Aliases: [data warehouse, enterprise data warehouse, EDW, DWH, Concepts/Data Warehouse]
Tags: [incubating]
publish: true
---
![[Pasted image 20250530180236.png]]

A data warehouse is a central repository for data which will be used for reporting and analytics. Data comes into the data warehouse from [[Online Transaction Processing|transactional systems]], relational databases, or [[Data Lake|other sources]] usually on a regular cadence. Business analysts, data engineers, data scientists, and decision makers then access the data through [[Business Intelligence|business intelligence]] tools, [[data-engineering-wiki/Tools/Programming Languages/SQL]] clients, and other analytics applications. Because the primary use cases for a data warehouse revolve around analytics, they typically use an [[Online Analytical Processing|OLAP]] technology for performance.

Purpose
* Reporting and Analysis of the organizational process.
## What does data warehouse do?

- The data warehouse is a central repository for clean and organized data for the organization.
- Gathers data from a different areas
- Integrates and stores the data
- Make data available for analysis

## Data Warehouse Advantages
* Support business intelligence activity
* enable effective analysis and decision-making
* foster data-driven innovation

## Data Warehouse Disadvantages

- A significant investment of time and resources to properly build
- Not designed for ingesting data in real-time (although they can typically handle near real-time)

## When to use a Data Warehouse

Data warehouses are made for complex queries on large datasets. You should consider a data warehouse if you're looking to keep your historical data separate from current transactions for performance reasons.

## Data Warehouse Life Cycle
![[Pasted image 20250530180948.png]]

1. Planning - the team plan how to design the data warehouse to satisfy the organization's need.
	1. Business requirements - understanding the organizational needs. Who and hoe will they use the data warehouse. (data scientist, data analyst job)
	2. Planning - Planning and organizing on integrating data. 
	3. Personas: 
		1. Data Engineer and Database admins - design data pipeline. Data engineers and admins plan data pipelines from database systems to the warehouse.
		2. Analyst and Data Scientist - data business knowledge. ensures that the data model accurately represents the organization. 
2. Implementation - team build data warehouse
	1. ETL Designs 
		Personas:
		1. Data Engineer coordinate with database admin to extract data from sources.
	2. Implementation - BI Application Development
		1. After the team loads the data into the warehouse, they work on BI application development. They setup BI or business intelligence tools to interact with the data warehouse and create reports needed by the organization.
			Example of BI Tools:
			* Tableau
			* Power BI
			* Google's Looker
		
3. Support/ Maintenance - the team trains end users and maintain the warehouse
	Personas:
		1.  Analyst and Data Scientist test the system to confirm their business requirements are met.
		2. Data Engineer deploy and make the warehouse available to the organization.
	*After deployment, any significant changes will follow the same steps starting back at the planning phase*

![[Pasted image 20250530183043.png]]

## Data Warehouse Architecture and Properties
![[Pasted image 20250530193738.png]]
1. Data Source - all data for the sources (files, databases, transactional db, json)
2. Data Staging - layer extracts, transform and clean data through ETL process. This contains ETL process and storage tables.
	1. ETL - extract data -> transform using business rules, staging database often used
3. Data Storage - Data may be stored from Datawarehouse -> Data mart/ Data mart -> Datawarehouse	

## Data Presentation Rules
User interacts with the presentation layer - are of constant development
1. Automated reporting/ dashboard tools - to create reports needed for decision making. 
	1. Tableau
	2. Powerbi
	3. Googles looker
2. BI/ data analytics - used to explore data and find patterns
	1. tableau
	2. knime
	3. rapidminer
	4. looker
	5. oracle
3. Direct queries to look at the data - sophisticated tools for exploration
	1. SQL server
	2. Azure Data Studio
	3. python
	4. R

## Data Warehouse Architecture
1. Inmon-top-down approach
![[Pasted image 20250530195949.png]]

* concise cleaning before putting data to data warehouse
* normalize warehouse for data integrity
Advantage
- normalization - less storage
- single source of truth
- easy to change data marts to support reporting changes

Disadvantage
* More joins = slower response time
* lengthy upfront work = higher startup cost

1. Kimball - bottom-up
![[Pasted image 20250530200240.png]]
* denormalizes data into star schema 
* Start schema - a way of storing data that makes query writing fast and straight forward

Advantage
* lower startup cost33333
Disadvantage
* increased ATL processing time
* greater possibility of duplicate data
* Ongoing development needed

## On premise and cloud data

1. On premise
	* Purchase and install software an hardware
	* On the grounds of organization

		Pros
		* complete control
		* implement custom data governance
		* local network speeds
		* can optimize for workloads
		Cons
		* Upfront hardware and software costs
		* Personnel/staff must maintain system
		* Must keep up with patches and security of system
2. In the cloud
	Pros
	* No maintaining equipment and infrastructure
	* Frees up personnel
	* Can scale storage and compute resources
	* No upfront investment in equipment/software
	Cons
	* less control
	* cannot optimize warehouse workloads
	* Possible unanticipated costs
3. Hybrid Approach
	* On premise and in the cloud data warehouse
		Reason
		* Backup
		* Disaster Recovery


		
## OLAP and OLTP systems
1. [[Online Analytical Processing]]
2. [[Online Transaction Processing|Concepts/Online Transaction Processing]]



## In the Cloud Popular Data Warehouses
- [[Tools/Databases/Amazon Redshift|Amazon Redshift]]
- [[Azure Synapse Analytics]]
- [[Google BigQuery]]
- [[Microsoft SQL Server]]
- [[Snowflake]]

## Data Warehouse Benchmarks
- 1 TB: [2020 - Redshift, Snowflake, Presto and BigQuery](https://fivetran.com/blog/warehouse-benchmark)
- 30 TB: [2019 - Redshift, Azure SQL Data Warehouse, BigQuery, Snowflake](https://gigaom.com/report/cloud-data-warehouse-performance-testing/)

![[Learning Resources#Data Warehousing Learning Resources]]

%% wiki footer: Please don't edit anything below this line %%



## This note in GitHub

<span class="git-footer">[Edit In GitHub](https://github.dev/data-engineering-community/data-engineering-wiki/blob/main/Concepts/Data%20Architecture/Data%20Warehouse.md "git-hub-edit-note") | [Copy this note](https://raw.githubusercontent.com/data-engineering-community/data-engineering-wiki/main/Concepts/Data%20Architecture/Data%20Warehouse.md "git-hub-copy-note")</span>

<span class="git-footer">Was this page helpful?
[👍](https://tally.so/r/mOaxjk?rating=Yes&url=https://dataengineering.wiki/Concepts/Data%20Architecture/Data%20Warehouse) or [👎](https://tally.so/r/mOaxjk?rating=No&url=https://dataengineering.wiki/Concepts/Data%20Architecture/Data%20Warehouse)</span>
