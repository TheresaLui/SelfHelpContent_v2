<properties
	pageTitle="Cluster could not be started in 50 minutes"
	description="Cluster could not be started in 50 minutes"
	service=""
	resource=""
	authors="rimayber"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="cd047075-4a83-489e-92f8-b14c9250204e"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Cluster could not be started in 50 minutes

Error when Cluster startup fails : *Cluster could not be started in 50 minutes. Cause: Timed out with exception after 601 attempts* . This error happens when execution of initscript gets hung and cluster creation gets timed out.

1. Check for any global initscripts under *dbfs:/databricks/init/* or cluster scoped initscripts *%sh /dbfs/databricks/init/<ClusterName>* .
2. Remove the initscript and try to create the cluster to confirm the issue with initscript.
3. If this is cluster scoped initscript, create a test cluster without any init script and run the each command in initscript manually to find which command is getting hung and try to fix it.
4. Convert scripts to cluster scoped init scripts.

If issue persists, please involve Databricks team. Please follow this [Wiki Link](https://supportability.visualstudio.com/AzureDataBricks/_wiki/wikis/AzureDataBricks.wiki/312121/Engaging-Databricks-Support) to create the Salesforce ticket.
