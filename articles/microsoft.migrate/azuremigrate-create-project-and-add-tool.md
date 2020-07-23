<properties
    pageTitle="Creating an Azure Migrate project"  description="Issues and guidance regarding creating a Migrate project and adding a tool"  service="microsoft.migrate"  
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

# Creating an Azure Migrate project

## **Recommended Steps**

### **How to check whether user has appropriate access to create a project**
For creating a project user needs "Owner" or "Contributor" permissions. [Please check here,](https://docs.microsoft.com/azure/role-based-access-control/check-access) whether you have required access

### **I don't see a particular geography when creating the Azure Migrate project**

 One can use a project in any geography to perform a migration to an Azure region of your choice. Review the supported geographies for [public](https://docs.microsoft.com/azure/migrate/migrate-support-matrix#supported-geographies-public-cloud) and [government clouds](https://docs.microsoft.com/azure/migrate/migrate-support-matrix#supported-geographies-azure-government).

### **I want to create a new project in a different geography and add tools to it**  
  
If you need to specify a different geography to store discovery, assessment or migration related metadata (typically used for scenarios where your data centers are present in different geographies), go to 'Servers' or 'Databases' and click on 'Change' against the 'Migrate project (Change)' on the top-right corner of your screen. Then click on 'click here' to create a new Azure Migrate project. [Learn more](https://docs.microsoft.com/azure/migrate/how-to-add-tool-first-time#create-additional-projects).

### **My added tools don't show up in the "Servers" or "Database" or "VDI" or "Web Apps" goal page**

Make sure that [project you are looking for is selected](https://docs.microsoft.com/azure/migrate/create-manage-projects#find-a-project)
  
### **My Azure Migrate project creation fails**  

This can be due to some intermittent issue, retry is suggested way to fix this issue. Click on the job notification for the failed deployment, navigate to "Deployments", and click on "Re-deploy" to re-trigger the creation of the project and addition of the selected tools. If a re-deploy does not solve the issue, make sure that your account has "Owner" or "Contributor" permissions for the subscription or resource group where you wish to create the migrate project. 

### **Do I need to pay for Azure Migrate and the non-Microsoft ISV tools that I plan to use?**

Azure Migrate and the first party Server Assessment & Server Migration tools are available at [no additional charge](https://azure.microsoft.com/pricing/details/azure-migrate). However, you may incur charges for using inetrgated non-Microsoft ISV assessment and migration tools.
  
### **I don't see the tool that I want to use**
  
We are constantly [adding tools to Azure Migrate](https://docs.microsoft.com/azure/migrate/how-to-add-tool-first-time).

### **ISV tools that are available in other geographies are not listed in Azure Government**

ISV partners are in process of enabling their tools in Azure Government for Azure Migrate. In the meanwhile, either you can use the partner tool independently or use any of the listed tools.

### **Looking to know more about Azure Migrate**

Extensive details regarding Azure Migrate are [documented here](https://docs.microsoft.com/azure/migrate/).
