<h1 style="text-align: center;">Big Query</h1>

Adding and configuring BigQuery connection within Qualytics empowers the platform to build a symbolic link with your schema to perform operations like data discovery, visualization, reporting, cataloging, profiling, scanning, anomaly surveillance, and more.  

This documentation provides a step-by-step guide on adding BigQuery as both a source and enrichment datastore in Qualytics. It covers the entire process, from initial connection setup to testing and finalizing the configuration. 

By following these instructions, enterprises can ensure their BigQuery environment is properly connected with Qualytics, unlocking the platform's potential to help you proactively manage your full data quality lifecycle.

Let’s get started 🚀

##  BigQuery Setup Guide 

This guide explains how to create and use a temporary dataset with an expiration time in BigQuery. This dataset helps manage intermediate query results and temporary tables when using the Google BigQuery JDBC driver.

It is recommended for efficient data management, performance optimization, and automatic reduction of storage costs by deleting data when it is no longer needed.

### Access the BigQuery Console

**Step 1:** Navigate to the BigQuery console within your Google Cloud Platform (GCP) account.

![alt text](image9.png)

**Step 2:** Click on the “vertical ellipsis”, it will open a popup menu for creating a dataset.
Click on the “Create dataset” to set up a new dataset.

![alt text](image8.png)

**Step 3:** Fill details for the following fields to create a new dataset.

>**Info:**
>>⦁	Dataset Location: Select the location that aligns with where your other datasets reside to minimize data transfer delays.
>>⦁	Default Table Expiration: Set the expiration to 1 day to ensure any table created in this dataset is automatically deleted one day after its creation.

![alt text](image5.png)

**Step 4:** Click the **"Create Dataset"** button to apply the configuration and create the dataset.

![alt text](image20.png)

**Step 5:** Navigate to the **“created dataset”** and **find the Dataset ID** in the **Dataset Info**.

![alt text](image4.png)

The dataset Info section contains the Dataset ID and other information related to the created
dataset. This generated Dataset ID is used to configure the BigQuery datastore.

## BigQuery Roles and Permissions

This section explains the roles required for viewing, editing, and running jobs in BigQuery. To
integrate BigQuery with Qualytics, you need specific roles and permissions.

Assigning these roles ensures Qualytics can perform data discovery, management, and
analytics tasks efficiently while maintaining security and access control.

## BigQuery Roles

- BigQuery Data Editor ```(roles/bigquery.dataEditor)```
Allows modification of data within BigQuery, including adding new tables and changing
table schemas. It is suitable if you want to regularly update or insert data.
- BigQuery Data Viewer ```(roles/bigquery.dataViewer)```
Enables viewing datasets, tables, and the contents. It is essential if you need to read
data structures and information.
- BigQuery Job User ```(roles/bigquery.jobUser)```
Allows creating and managing jobs in BigQuery, such as queries, data imports, and data
exports. It is important if you want to run automated queries.
- BigQuery Read Session User ```(roles/bigquery.readSessionUser)```
Allows usage of the BigQuery Storage API for efficient retrieval of large data volumes. It
provides capabilities to create and manage read sessions, facilitating large-scale data
transfers.


