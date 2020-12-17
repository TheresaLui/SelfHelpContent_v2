<properties
	  pageTitle="Create or Delete Collection/Database issue"
	  description="Create or Delete Collection/Database issue"
      service="Microsoft.DocumentDB"
      resource="databaseAccounts"
	  authors="anferrei"
	  ms.author="anferrei"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="7c8f4bf8-f074-43de-84fe-16793dda183c"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Create or Delete Collection/Database issue

<!--issueDescription-->

Dear customer,

The Collection Delete can be done in follow ways.

**Via Azure Portal:**  
We can tract the collection delete and point to a user since the portal is accessed through a user credential.  This information is logged in the Azure portal Telemetry. Incase, you do not have access to the Azure portal Telemetry, then you can reach out to the Azure support team to get this information for you.  I have added the kusto query for references.


**Via SDK:**  
Any delete operation performed through application goes through SDK call. This SDK uses Master Key for accessing the Cosmos Database Account which mean we do not track the user and cannot find who delete the resource.   However, sometime, you can be able to provide some hint to customer using the user agent.

< ADD DETAILS  OF  YOUR  INVESTIGATION  IN THE LAST STEP>

Thank you.

<!--/issueDescription-->

