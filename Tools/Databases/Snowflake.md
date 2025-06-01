---
Aliases: []
Tags: [seedling]
publish: true
---

![[Assets/snowflake_logo.png|100]]

[Snowflake](https://www.snowflake.com/) is a cloud data platform that at it's core features a columnar-stored [[Data Warehouse|data warehouse]]. It's unique architecture separates compute from storage which allows you to scale the database to your needs and only pay for what you use.

### How to connect with SQL
1. Through snowflake web interface called Snowsight. We can create norebooks to rin sql and python code for building and maintaining data pipeline.
2. Worksheets - an interface for creating and running SQL queries.

## Snowflake Drivers and Connectors 
1. ODBC (Open Database Connectivity)
2. JDBC (Java Database Connectivity)
3. Connectors: Python, Spark, and more
4. Snowflake CLI - install on Linux, Windows, or Mac

## Datatypes
![[Pasted image 20250601144043.png]]
Common Datatype:
![[Pasted image 20250531153035.png]]

Unique Snowflake datatypes
1. Numeric - alias for number
2. TIMESTAMP_LTZ - timestamp with local time zone.

Converting datatype
1. CAST(<source_data/column> AS <target_data_type>) 
	Example: CAST('80' AS INT) or use this other syntax '80'::INT 
2. Conversion function: TO_VARCHAR(), TO_DATE()
3. DESC TABLE table_name - get information of all columns of the table_name

## Snowflake function
1. INITCAP() - cappitalizes each word in a string
2. CONCAT - use to joins expressions - 
![[Pasted image 20250531214647.png]]

3. DATE & TIME Captions:
	1. CURRENT_DATE() / CURRENT_DATE - shows exact date
	2. CURRENT_TIME() / CURRENT_TIME - shows exact time

4. EXTRACT - extract specific parts from date/time/ timestamp
		![[Pasted image 20250531214955.png]]

5. GROUP BY ALL - group by all column in the SELECT list 

## Snowflake Joins
1. Natural Join - automatically match columns and eliminate duplicate ones.
![[Pasted image 20250601124039.png]]
2. Lateral Joins - lets a subquery in FROM reference columns from preceding tables or views.
![[Pasted image 20250601124619.png]]


## Subquerying and CTE (Common Table Expressions)

![[Pasted image 20250601133527.png]]

![[Pasted image 20250601133539.png]]

![[Pasted image 20250601133635.png]]

### Why use CTE?
1. Managing Complex operations
2. Modular
3. Readable
4. Reusable

## Query history
sonwflake.account_usage.query_history
![[Pasted image 20250601140913.png]]

![[Pasted image 20250601141001.png]]


## Handling Semi- Structured Data

![[Pasted image 20250601142943.png]]
![[Pasted image 20250601143115.png]]
![[Pasted image 20250601143151.png]]
![[Pasted image 20250601143209.png]]
![[Pasted image 20250601143239.png]]
![[Pasted image 20250601143519.png]]


![[Pasted image 20250601144121.png]]



## SEMI-SRUCTURED DATA FUNCTION
1. PARSE-JSON - convert 



## Snowflake Official Documentation
https://docs.snowflake.com/en/index.html

## Snowflake Learning Resources
https://developers.snowflake.com/resources/

%% wiki footer: Please don't edit anything below this line %%

## This note in GitHub

<span class="git-footer">[Edit In GitHub](https://github.dev/data-engineering-community/data-engineering-wiki/blob/main/Tools/Databases/Snowflake.md "git-hub-edit-note") | [Copy this note](https://raw.githubusercontent.com/data-engineering-community/data-engineering-wiki/main/Tools/Databases/Snowflake.md "git-hub-copy-note")</span>

<span class="git-footer">Was this page helpful?
[👍](https://tally.so/r/mOaxjk?rating=Yes&url=https://dataengineering.wiki/Tools/Databases/Snowflake) or [👎](https://tally.so/r/mOaxjk?rating=No&url=https://dataengineering.wiki/Tools/Databases/Snowflake)</span>
