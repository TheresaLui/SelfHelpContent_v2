<properties
	pageTitle="Expensive queries RCA"
	description="RCA - expensive query operations on collection"
	infoBubbleText="The account has expensive query operations."
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="bharathb"
	displayOrder=""
	articleId="query_86D7D1E8-4CEF-40D5-AB7F-B16304CDB097"
  diagnosticScenario="MachineKeyUpdates"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
/>
# We ran diagnostics on your resource and found an issue
<!--issueDescription-->
We found a high number of expensive queries for your account
<!--/issueDescription-->
We found that a large percentage of the total RUs consumed for your account were due to expensive queries. You might want to consider rewriting the queries to consume fewer RUs. Additonally, you can follow this [link](https://docs.microsoft.com/en-us/azure/cosmos-db/performance-tips) for general performance guidelines.
