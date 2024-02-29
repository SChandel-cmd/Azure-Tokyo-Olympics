# Tokyo Olympics Data Transformation Project

## Overview

![Architecture](https://github.com/SChandel-cmd/Azure-Tokyo-Olympics/blob/main/architecture.bmp)

This project focuses on leveraging Azure services such as Azure Data Factory, Azure Databricks, and Azure Synapse Analytics to process, transform, and analyze Tokyo Olympics data. The data is initially stored in CSV files and uploaded to Azure Storage on Data Lake Gen2. Azure Data Factory orchestrates data movement, Azure Databricks handles data processing and transformation, and Azure Synapse Analytics is utilized for querying and analyzing the transformed data stored in SQL tables.

## Steps

### 1. Setting up Azure Storage Account
1. **Create Azure Storage Account**: 
    - Log in to the Azure portal.
    - Navigate to the Azure Storage Accounts service.
    - Click on "Add" to create a new storage account.
    - Follow the prompts to configure the storage account details such as name, resource group, location, and performance.
    - Enable Hierarchical Namespace for Data Lake Gen2 compatibility.

2. **Create Containers**: 
    - Inside the created storage account, set up containers for storing the CSV files.
    - Create containers as per your data organization requirements.

### 2. Uploading CSV Files to Azure Storage
1. **Azure Data Factory Setup**:
    - Navigate to Azure Data Factory service in the Azure portal.
    - Create a new Azure Data Factory instance if not already available.

2. **Create Pipelines**:
    - Define a pipeline in Azure Data Factory for data movement.
    - Configure a copy activity within the pipeline to copy data from your local storage to Azure Storage.
    - Set up connections to your local storage and Azure Storage within the copy activity.

3. **Triggering the Pipeline**:
    - Schedule the pipeline to run at appropriate intervals or trigger it manually to upload data to Azure Storage.

### 3. Setting up Azure Databricks
1. **Create Databricks Workspace**:
    - Navigate to Azure Databricks service in the Azure portal.
    - Create a new Databricks workspace if not already available.

2. **Set up Azure Data Lake Storage (ADLS) Connection**:
    - Inside your Databricks workspace, create a connection to Azure Data Lake Storage Gen2 where your data is stored.
    - Provide necessary details such as account name, filesystem, and credentials.

3. **Create Databricks Cluster**:
    - Configure a Databricks cluster with appropriate specifications for your data processing needs.

4. **Access Control**:
    - Ensure proper access controls are set up for Azure Databricks, granting necessary permissions to access Azure Storage.

### 4. Data Processing with Azure Databricks
1. **Loading Data**:
    - Load the CSV files from Azure Storage into Databricks using Spark DataFrame APIs or Databricks utilities.

2. **Data Transformation**:
    - Perform necessary transformations on the loaded data using DataFrame operations or SQL queries depending on your requirements.

3. **Write Transformed Data**:
    - Write the transformed data back to Azure Storage or any other desired destination using appropriate write operations in Databricks.

4. **Optimization**:
    - Optimize your data processing tasks by leveraging Databricks' capabilities such as cluster management, parallel processing, and caching.

### 5. Setting up Azure Synapse Analytics
1. **Create Azure Synapse Workspace**:
    - Navigate to Azure Synapse Analytics service in the Azure portal.
    - Create a new Synapse workspace if not already available.

2. **Data Integration**:
    - Configure data integration pipelines within Azure Synapse to ingest data from Azure Storage into Synapse SQL Pools.
    - Define mappings to specify how CSV data should be loaded into SQL tables.

3. **Data Querying**:
    - Utilize SQL scripts or tools like Synapse Studio to query and analyze the transformed data stored in SQL tables.
    - Perform exploratory data analysis and generate insights as needed.

### 6. Monitoring and Maintenance
1. **Monitoring**:
    - Monitor pipeline execution in Azure Data Factory, job runs in Azure Databricks, and queries in Azure Synapse Analytics for any errors or performance issues.

2. **Maintenance**:
    - Regularly review and optimize your data processing workflows to ensure efficiency and cost-effectiveness.
    - Keep Azure services updated with the latest patches and features.

## Conclusion
This README provides a comprehensive guide to setting up and executing a data transformation project using Azure Data Factory, Azure Databricks, and Azure Synapse Analytics for Tokyo Olympics data. By following these steps, you can efficiently manage data movement, processing, transformation, and analysis tasks in the cloud environment, enabling valuable insights and decision-making capabilities.
