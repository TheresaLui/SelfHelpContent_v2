<properties 
    pageTitle="Diagnose and resolve issues with source control integration – Azure DevOps" 
    description="Diagnose and resolve issues with source control integration – Azure DevOps" 
    service="microsoft.databricks" 
    resource="workspaces" 
    authors="lahaddad" 
    ms.author="lahaddad" 
    displayOrder="15" 
    selfHelpType="generic" 
    supportTopicIds="32784333" 
    resourceTags="" 
    productPesIds="16432" 
    cloudEnvironments="public, fairfax, usnat, ussec" 
    articleId="91efc742-2e53-4d6f-a7ba-4edcadc2718d" 
    ownershipId="AzureData_AzureDatabricks" 
/> 

# Diagnose and resolve issues with source control integration – Azure DevOps 

## **Recommended Steps** 

* **Git Sync failure: 403 access denied** - Validate the Git token configured on Databricks.

* **Git Sync failure: Error while syncing Git history: Could not authenticate using AAD token: FailureNoIdentityProviderCredential** - This error usually returns from the AAD side where authentication fails before syncing to Git server.

* **Error linking with Git: Unexpected character ('<' (code 60)): expected a valid value (number, String, array, object, 'true', 'false' or 'null')? at [Source: ????<!DOCTYPE html PUBLIC …** - This error is due to a known issue where your Databricks and DevOps are in different AAD tenants, which fails the passthrough sign-in and blocks them from using the feature altogether. Currently, this feature is not supported. As a workaround, follow the steps in [this blog](https://thedataguy.blog/ci-cd-with-databricks-and-azure-devops/ ). 
 

## **Recommended Documents** 

* [Azure DevOps Services version control](https://docs.microsoft.com/azure/databricks/notebooks/azure-devops-services-version-control) 
* [Troubleshooting](https://docs.microsoft.com/azure/databricks/notebooks/azure-devops-services-version-control#troubleshooting) 
