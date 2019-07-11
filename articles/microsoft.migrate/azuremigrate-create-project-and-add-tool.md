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
    cloudEnvironments="public"  
    articleId="75vc3501-2a3f-4d0d-96c5-b2b5886483e6"  
 />  

# Creating an Azure Migrate project and adding a tool to the project

## **Recommended Steps**  

### **My Azure Migrate project creation fails with a deployment failed error.**  

You can usually retry to fix this error. Click on the job notification for the failed deployment, navigate to "Deployments", and click on "Re-deploy" to re-trigger the creation of the project and addition of the selected tools. This should solve the issue.

### **I want to create a new project in a different geography and add tools to it.**  
  
If you need to specify a different geography to store discovery, assessment or migration related metadata (typically used for scenarios where your data centers are present in different geographies), go to 'Servers' or 'Databases' and click on 'Change' against the 'Migrate project (Change)' on the top-right corner of your screen. Then click on 'click here' to create a new Azure Migrate project. [Learn more](https://aka.ms/migrate/self-help/create-migrate-project).

### **My added tools don't show up in the "Servers" or "Databases" page.**

Make sure that you have selected the right project by clicking on 'Change' against 'Migrate project (Change)' on the top-right corner of your screen in 'Servers' or 'Databases'. Now choose the correct subscription and project name and click on 'OK'. The page should refresh with the added tools of the selected Azure Migrate project. [Learn more](https://aka.ms/migrate/self-help/create-migrate-project)
  
### **I don't see the tool that I want to use.**
  
We are constantly adding tools to Azure Migrate. [Learn more](https://aka.ms/migrate/self-help/add-new-tools-to-migrate-project).  
  
### **Do I need to pay for Azure Migrate and the non-Microsoft ISV tools that I plan to use?**

Azure Migrate and the in-built Server Assessment, Server Migration tools are available at no additional charge. However, you may incur charges for other non-Microsoft/ISV assessment and migration tools you use while using Azure Migrate. [Learn more](https://aka.ms/migrate/self-help/pricing-of-tools).

### **I don't see a particular geography when creating the Azure Migrate project.**
  
Azure Migrate is currently available in United States, Europe, Asia, and United Kingdom. We will soon add support for Canada and Australia. Other geographies will follow later this year. You can use a project in any geography to perform a migration to an Azure region of your choice.  
