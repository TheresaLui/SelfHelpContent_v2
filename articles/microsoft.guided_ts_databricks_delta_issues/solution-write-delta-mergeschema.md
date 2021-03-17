<properties
	pageTitle="Writing to a Delta table doesn't merge schema when mergeSchema is set to true"
	description="Writing to a Delta table doesn't merge schema when mergeSchema is set to true"
	service="Microsoft.Databricks"
	resource="Microsoft.Databricks/workspaces"
	ms.author="lahaddad"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="620b4ff4-f680-49b2-a787-8b95ad0f173c"
   	ownershipId="AzureData_AzureDatabricks"
/>

# Writing to a Delta table doesn't merge schema when mergeSchema is set to true

<!--issueDescription-->

Based on provided details and initial investigation, please find a summary of issue as below:

## **Problem**

While writing a dataframe to a delta table, it doesn’t automatically update the schema of delta table, even though the mergeSchema option is set to true.

## **Cause**

This mergeSchema option will not work if the command is executed from a table access control enabled cluster. This will also not work with INSERT INTO operation.

## **Solution**

Use non-ACL enabled cluster to merge schema of the delta table.



<!--/issueDescription-->
