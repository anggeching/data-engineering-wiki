---
aliases:
  - ETL Best Practices
  - ELT Best Practices
tags:
  - seedling
publish: true
---

## Overview

A best practice guide for data pipelines compiled from data engineers in the community. Follow this guide to help you build more robust, scalable, and more performant data pipelines. These best practices are in no particular order but we've done our best to categorize them.


## Data pipelines (Datawarehouse concepts)
How data get from point A to point B

* ETL and ELT - the goal of both method is to end up to cleansed data that we can use on the data warehouse, but the order they take is different.
* ETL

# Data Cleaning 
1. Data format cleaning before putting on data warehouse
2. Address Parcing, deviding street address into its component
		![[Pasted image 20250531113355.png]]
3. Data validation 
	1. valid Data type check
	2. valid value check
4. Duplication elimination
5. Data Governance - a set of organizational policies processes to help keep data clean.



## General Best Practices

- Verify your assumptions about the data.
- Document your pipelines.
- Add proper logging to your pipelines to make debugging easier.
- Use code and version control (git) for pipelines.
- Make your pipelines [[Idempotence|idempotent]].
- Understand the tradeoff between fast data and accurate data. Data quality takes time.
- Have separate environments for development, staging, and production ideally.
	- If you have separate environments, color code them and label them clearly.
- Use templates whenever possible. If you're writing custom code, try to make it generic/modular.
- Avoid ingesting data from manually created data sources (e.g. Google Sheet/Excel file). If you have to do so, require strict protections on what can change at the source.

## Design

- Use Docker for dependency management.
- Prepare for intermittent or temporary failures. Use exponential back-off and retry strategies.
- Use CI to deploy pipelines to staging and production environments.
- Set up alerting on failures and pipeline run times.
- Surface all parameters and use configuration files/environment variables to change pipeline behavior vs updating the code.

## Optimization

- Don't let file sizes become too large or too small. Large files (>1 GB) can require more resources and many small files can create a large overhead to process. ~250 MB is a good size that allows for better parallel processing.
- Use the [[Claim Check Pattern|claim check pattern]] to pass large amounts of data between tasks in your pipeline.

## Security

- Save credentials in a secrets manager and access them in your pipeline programmatically.
	- Ideally, have secrets rotated automatically.
- Avoid logging any sensitive information like credentials or PII data.

## Testing

- Test data quality with [[Data Unit Test|data unit tests]] regularly.
- Test data pipeline code with regular unit tests.
- Set up a local environment to test pipelines locally first. (see Docker above)
- Re-define pipeline failures. If pipeline fails x times but data is still delivered on time then it was successful.

%% wiki footer: Please don't edit anything below this line %%

## This note in GitHub

<span class="git-footer">[Edit In GitHub](https://github.dev/data-engineering-community/data-engineering-wiki/blob/main/Guides/Data%20Pipeline%20Best%20Practices.md "git-hub-edit-note") | [Copy this note](https://raw.githubusercontent.com/data-engineering-community/data-engineering-wiki/main/Guides/Data%20Pipeline%20Best%20Practices.md "git-hub-copy-note")</span>

<span class="git-footer">Was this page helpful?
[👍](https://tally.so/r/mOaxjk?rating=Yes&url=https://dataengineering.wiki/Guides/Data%20Pipeline%20Best%20Practices) or [👎](https://tally.so/r/mOaxjk?rating=No&url=https://dataengineering.wiki/Guides/Data%20Pipeline%20Best%20Practices)</span>
