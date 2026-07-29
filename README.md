# Azure Synapse: Dynamically Remove Spaces

!!! important
  These demos are intended as practical examples. For official guidance and support, refer to [Microsoft documentation](https://learn.microsoft.com/azure/synapse-analytics/) or [Microsoft Support](https://support.microsoft.com/contactus?ContactUsExperienceEntryPointAssetId=S.HP.SMC-HOME).

!!! note
  The examples inspect table and column names, remove spaces, and create normalized views.

<details>
<summary><b>List of References </b> (Click to expand)</summary>

- [What is Azure Synapse Analytics?](https://learn.microsoft.com/en-us/azure/synapse-analytics/overview-what-is)
- [What is dedicated SQL pool (formerly SQL DW) in Azure Synapse Analytics?](https://learn.microsoft.com/en-us/azure/synapse-analytics/sql-data-warehouse/sql-data-warehouse-overview-what-is)
- [Serverless SQL pool in Azure Synapse Analytics](https://learn.microsoft.com/en-us/azure/synapse-analytics/sql/on-demand-workspace-overview)
- [Create and use views using serverless SQL pool in Azure Synapse Analytics](https://learn.microsoft.com/en-us/azure/synapse-analytics/sql/create-use-views)
  
</details>

<details>
<summary><b>Table of contents</b> (click to expand)</summary>

- [Overview](#overview)
  - [SQL Pools](#sql-pools)
  - [Synapse Views](#synapse-views)
- [Dynamically remove spaces from names](#dynamically-remove-spaces-from-names)

</details>

## Overview

Azure Synapse Analytics is an integrated analytics service that accelerates time to insight across data warehouses and big data systems. It combines enterprise data warehousing, Spark-based big data processing, and data integration in a unified experience.

<img width="550" alt="image" src="https://github.com/user-attachments/assets/9a753e36-e229-4da7-8a87-a5c21ddd70f9"> <br/>
From [Microsoft Official Documentation](https://learn.microsoft.com/en-us/azure/synapse-analytics/overview-what-is)

### SQL Pools

SQL pools in Azure Synapse Analytics come in two main types:

| Type | Description | Characteristics | 
| --- | --- | --- |
| Serverless SQL Pool (built in) | This is a built-in, on-demand query service in Azure Synapse Analytics. You don't need to provision or manage any infrastructure. You simply run your queries, and you're billed based on the amount of data processed. It's great for ad-hoc querying and exploring data in your data lake without worrying about the underlying infrastructure. |    - A query service over data in your data lake. <br/> - No infrastructure setup or clusters to maintain. <br/> - Pay-per-use model, charging only for the data processed by queries. <br/> - Suitable for ad-hoc querying and data exploration. |
| Dedicated SQL Pool (formerly SQL DW) | This requires you to provision and manage a set of resources (Data Warehousing Units or DWUs). You have control over the performance and scale of your data warehouse, but it also means you need to manage the infrastructure. It's ideal for large-scale, high-performance analytics and data warehousing. |    - A collection of analytic resources provisioned when using Synapse SQL. <br/> - Uses Data Warehousing Units (DWU) to determine size and performance. <br/> - Ideal for large-scale data warehousing and high-performance analytics. | 

### Synapse Views

Synapse views are virtual tables created by querying one or more tables. They do not store data themselves, but they simplify complex queries and make them reusable. Views can be created over both dedicated and serverless SQL pools.

## Dynamically remove spaces from names

- Follow the [serverless SQL pool walkthrough](https://cloud2br-msftlearninghub.github.io/azSynapse-Dynamic-RemoveBlanks/serverless/) for external tables in a data lake.
- Follow the [dedicated SQL pool walkthrough](https://cloud2br-msftlearninghub.github.io/azSynapse-Dynamic-RemoveBlanks/dedicated/) for provisioned data warehouse tables.
