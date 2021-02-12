<properties pageTitle="How to access customer workspace and check cluster Event logs"
            description="How to access customer workspace and check cluster Event logs"
            service="Microsoft.Databricks"
            resource="Microsoft.Databricks/workspaces"
            authors="JRMayberry"
            ms.author="rimayber"
            displayOrder=""
            selfHelpType="TSG_Content"
            supportTopicIds=""
            resourceTags=""
            productPesIds=""
            cloudEnvironments="public, fairfax, usnat, ussec"
            articleId="b5fa6469-4fd8-4bb0-8e89-bd73fec2a2c3"
            ownershipId="Centennial_CloudNet_LoadBalancer" />

# How to access customer workspace and check cluster Event logs

**Access customer workspace through Genie as below**

1. Go to [Genie](https://genie-azure-prod.dev.databricks.com/)
2. Fill customer workspace and ticket details gathered in previous steps

**Cluster Event logs:**

The cluster event log displays important cluster lifecycle events that are triggered manually by user actions or automatically by Databricks. Such events affect the operation of a cluster as a whole and the jobs running in the cluster. Events are stored for 60 days, which is comparable to other data retention times in Databricks. 

To access these logs, please follow these steps:

1. Click the clusters icon in the sidebar
2. Click a cluster name
3. Click the Event Log tab

Given timestamp(s) provided earlier, look for event(s) when cluster fails and click on it to get more info to get more details of the quota limit being hit.

**Check for errors similar to the following:** 

1. Cloud Provider Launch Failure: A cloud provider error was encountered while setting up the cluster
2. Azure error code: OperationNotAllowed
3. Operation results in exceeding quota limits of Core
