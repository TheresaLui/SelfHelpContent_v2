<properties
    pageTitle="Creating an Azure Migrate project and adding a tool to the project"  description="Issues and guidance regarding creating a Migrate project and adding a tool"  service="microsoft.migrate"  
    resource="migrateprojects"  
    authors="ponatara"  
    ms.author="ponatara"  
    displayOrder=""  
    selfHelpType="generic"  
    supportTopicIds="32675740"  
    resourceTags=""  
    productPesIds="16348"  
    cloudEnvironments="public, Fairfax, usnat, ussec"  
    articleId="75vc3501-2a3f-4d0d-96c5-b2b5886483e6"  
 	ownershipId="Compute_AzureMigrate"
/>  

# Creating an Azure Migrate project and adding a tool to the project

## **Recommended Steps**  

### **Do I need to pay for Azure Migrate and the non-Microsoft ISV tools that I plan to use?**

Azure Migrate and the in-built Server Assessment, Server Migration tools are available at [no additional charge](https://azure.microsoft.com/pricing/details/azure-migrate). However, you may incur charges for other non-Microsoft/ISV assessment and migration tools you use while using Azure Migrate.

### **I don't see a particular geography when creating the Azure Migrate project**
  
Azure Migrate is currently available in Asia, Europe, Japan, United Kingdom, United States, Canada, India, and Australia. Other geographies like Brazil, France, and Azure Government will follow later this year. You can use a project in any geography to perform a migration to an Azure region of your choice.  

### **I want to create a new project in a different geography and add tools to it**  
  
If you need to specify a different geography to store discovery, assessment or migration related metadata (typically used for scenarios where your data centers are present in different geographies), go to 'Servers' or 'Databases' and click on 'Change' against the 'Migrate project (Change)' on the top-right corner of your screen. Then click on 'click here' to create a new Azure Migrate project. [Learn more](https://docs.microsoft.com/azure/migrate/how-to-add-tool-first-time#create-additional-projects).

### **My added tools don't show up in the "Servers" or "Databases" page**

Make sure that you have selected the right project by clicking on 'Change' against 'Migrate project (Change)' on the top-right corner of your screen in 'Servers' or 'Databases'. Now choose the correct subscription and project name and click on 'OK'. The page should refresh with the added tools of the selected [Azure Migrate](https://docs.microsoft.com/azure/migrate/how-to-add-tool-first-time#create-additional-projects) project.
  
### **My Azure Migrate project creation fails**  

You can usually retry to fix this error. Click on the job notification for the failed deployment, navigate to "Deployments", and click on "Re-deploy" to re-trigger the creation of the project and addition of the selected tools. If a re-deploy does not solve the issue, make sure that your account has "Owner" or "Contributor" permissions for the subscription or resource group where you wish to create the migrate project. This should solve the issue.

### **Not able to select the geography to create my migrate project**
If you are not able to see and choose a geography where Azure Migrate was deployed recently, wait for up to 15-20 mins and retry project creation. Azure Migrate is deployed in these [geographies](https://docs.microsoft.com/azure/migrate/how-to-add-tool-first-time#create-a-project-and-add-a-tool). 
  
### **I don't see the tool that I want to use**
  
We are constantly [adding tools to Azure Migrate](https://docs.microsoft.com/azure/migrate/how-to-add-tool-first-time).

### **Deleting an Azure Migrate project**

To delete an Azure Migrate project and its associated resources including sites, recovery services vaults, migrate vaults, key vaults, assessment projects etc, go to "Resource groups" page on the Azure portal, select the resource group where the migrate project was created and select "Show hidden types". Then select the migrate project and its associated resources as shown in the table below and delete them. Alternatively, if the resource group is exclusively used by the migrate project and its associated resources, you can delete the entire resource group. Note that the table presents an exhaustive list of all resource types created for all scenarios (discovery, assessment and migration). You will only find the resources that were created for your scenario in the resource group.

### Resources created for servers on VMware or physical servers [Resource (Type)]:

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

### Resources created for servers on Hyper-V [Resource (Type)]:

- "ProjectName" (Microsoft.Migrate/migrateprojects)
- "ProjectName"project (Microsoft.Migrate/assessmentProjects)
- HyperV*kv (Key vault)
- HyperV*site (Microsoft.OffAzure/HyperVSites)
- "ProjectName"-MigrateVault-* (Recovery Services vault)

For more details around project deletion please have a look at the article [here](https://docs.microsoft.com/azure/migrate/how-to-delete-project).
