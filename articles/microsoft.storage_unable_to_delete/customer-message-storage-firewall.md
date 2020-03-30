<properties
	pageTitle="No Access (403) when trying to delete an Azure File Share"
	description="No Access (403) when trying to delete an Azure File Share"
	service="microsoft.storage"
	resource="storageAccounts"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
	articleId="1fcba446-43d0-4ea6-8f31-24417f9b5c40"
	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# No Access (403) when trying to delete an Azure File Share

<!--issueDescription-->
We've researched your case and believe that your unable to delete issue is due to Azure Firewall being enabled on your storage account and the source IP/Public IP of the connection not being whitelisted. In order to resolve this issue you must whitelist the Public IP within the Firewall of the Storage Account.
<!--/issueDescription-->