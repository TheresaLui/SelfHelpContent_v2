<properties
	pageTitle="Large documents - RCA"
	description="RCA - High number operations inserting/updating large documents"
	infoBubbleText="High number operations inserting/updating large documents."
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="bharathb"
	displayOrder=""
	articleId="largedocument_2F574F61-4568-4D9D-940E-1817C22DC671"
  diagnosticScenario="MachineKeyUpdates"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
/>
# We ran diagnostics on your resource and found an issue
<!--issueDescription-->
We found a high number operations inserting/updating large documents
<!--/issueDescription-->
Inserting or updating large documents would require many RUs. If there are a large number of such operations, you might end up using most of your provisioned throughput. Please consider modelling your data to use smaller documents following this [link](https://docs.microsoft.com/en-us/azure/cosmos-db/modeling-data)
