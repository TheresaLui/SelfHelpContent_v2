<properties
 pageTitle="Getting 400 error code"
 description="Getting 400 error code"
 service="Microsoft.Databricks"
 resource="Microsoft.Databricks/workspaces"
 authors="AzureData_AzureDatabricks"
 ms.author="AzureData_AzureDatabricks"
 displayOrder=""
 selfHelpType="TSG_Content"
 supportTopicIds=""
 resourceTags=""
 productPesIds=""
 cloudEnvironments="public, fairfax, usnat, ussec"
 articleId="3d3a7146-f26c-4df9-bab1-f6bbcbb59dac"
 ownershipId="AzureData_AzureDatabricks"
/>

# Getting 400 error code

### Symptom

Rest API call fails with 400 error.

### Troubleshooting & Solution

This usually means a bad request; errors can be like malformed request syntax, invalid request message parameters:

- Check all the parameters being passed in request JSON structure
- Cross-check with databricks documentation for all the valid parameters
- Check the used API endpoint is correct or not
- Check the correct syntax for example like POST, GET and PUT
- One way to get an example rest query would be to do same operation from UI and check the rest call from network tab in developer console 	
- If issue persists, ask SME on Ava and create Databricks SF ticket if needed

### Recommended Documents

[Rest API 2.0](https://docs.microsoft.com/en-us/azure/databricks/dev-tools/api/latest/)
[Azure Databricks APIs](https://docs.microsoft.com/en-us/azure/databricks/dev-tools/api/latest/#apis)
