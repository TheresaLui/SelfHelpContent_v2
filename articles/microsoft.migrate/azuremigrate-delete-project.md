<properties
    pageTitle="Deleting an Azure Migrate Project"  
    description="Deleting an Azure Migrate Project and associated artifacts"  
    service="microsoft.migrate"
    resource="migrateprojects"  
    authors="shsaluja"  
    ms.author="shsaluja"  
    displayOrder=""  
    selfHelpType="generic"  
    supportTopicIds="32683731"  
    resourceTags=""  
    productPesIds="16348"  
    cloudEnvironments="public, Fairfax"  
    articleId="523af262-4b6b-4499-8234-74d8e16929ad"  
	ownershipId="Compute_AzureMigrate"
/>

# Deleting an Azure Migrate Project and associated artifacts

## **Recommended Steps**  

### **Deleting an Azure Migrate project**

To delete an Azure Migrate project and its associated resources including sites, recovery services vaults, migrate vaults, key vaults, assessment projects etc, go to "Resource groups" page on the Azure portal, select the resource group where the migrate project was created and select "Show hidden types". Then select the migrate project and its associated resources as shown in the table below and delete them. Alternatively, if the resource group is exclusively used by the migrate project and its associated resources, you can delete the entire resource group. Note that the table presents an exhaustive list of all resource types created for all scenarios (discovery, assessment and migration). You will only find the resources that were created for your scenario in the resource group.

### Resources created for servers on VMware or physical servers [Resource (Type)]

- "Appliancename"kv (Key vault)
- "Appliancename"site (Microsoft.OffAzure/VMwareSites)
- "ProjectName" (Microsoft.Migrate/migrateprojects)
- "ProjectName"project (Microsoft.Migrate/assessmentProjects)
- "ProjectName"rsvault (Recovery Services vault)
- "ProjectName"-MigrateVault-* (Recovery Services vault)
- migrateappligwsa* (Storage account)
- migrateapplilsa* (Storage account)
- migrateapplicsa* (Storage account)
- migrateapplikv* (Key vault)
- migrateapplisbns16041 (Service Bus Namespace)

### Resources created for servers on Hyper-V [Resource (Type)]

- "ProjectName" (Microsoft.Migrate/migrateprojects)
- "ProjectName"project (Microsoft.Migrate/assessmentProjects)
- HyperV*kv (Key vault)
- HyperV*site (Microsoft.OffAzure/HyperVSites)
- "ProjectName"-MigrateVault-* (Recovery Services vault)

For more details around project deletion please have a look at the article [here](https://docs.microsoft.com/azure/migrate/how-to-delete-project).
