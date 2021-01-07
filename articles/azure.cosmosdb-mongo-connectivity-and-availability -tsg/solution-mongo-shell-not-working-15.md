<properties
	  pageTitle="Mongo Shell Not Working"
	  description="Mongo Shell Not Working"
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
	  articleId="917efcbe-61c1-4398-b4af-3e7be1c3a3a1"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Mongo Shell Not Working

<!--issueDescription-->

Dear customer,

**Issue**: When user is trying to open a mongo shell, nothing happens and the tab just keeps blank.  
**Solution**: Check Firewall. Firewall is not supported with the Mongo shell.
<br>The recommendation is to:
- Install mongo shell on the local computer within the firewall rules
- Use legacy mongo shell

Thank you.

<!--/issueDescription-->

