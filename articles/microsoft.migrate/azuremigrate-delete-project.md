<properties
  pagetitle="Deleting an Azure Migrate Project and associated artifacts&#xD;"
  description="Deleting an Azure Migrate Project and associated artifacts"
  service="microsoft.migrate"
  resource="migrateprojects"
  ms.author="shsaluja,panshar"
  selfhelptype="Generic"
  supporttopicids="32683731"
  resourcetags=""
  productpesids="16348"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="523af262-4b6b-4499-8234-74d8e16929ad"
  ownershipid="Compute_AzureMigrate" />
# Deleting an Azure Migrate Project and associated artifacts

## **Recommended Steps**  

### **Deleting an Azure Migrate project**

* Check for access. To delete a project, the user needs **owner** or **contributor** permissions. See if you have [required access for a project](https://docs.microsoft.com/azure/role-based-access-control/check-access).
* Follow [these steps](https://docs.microsoft.com/azure/migrate/how-to-delete-project) to delete project and related resources

**Note:** Project deletion doesn't impact the migrated VMs that are already running in Azure.

* If you want to delete the discovered servers, we recommend deleting the project, according to the steps outlined above.

* The assessments can be deleted from portal. To do this, navigate to the assessment to be deleted and select **Delete Assessment**. 
