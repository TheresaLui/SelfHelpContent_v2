<properties
    pageTitle="Issues related to Movere, non-Microsoft tools and non-Server related Microsoft tools"  
    description="Issues and guidance related to non-Microsoft tools added to an Azure Migrate project"  
    service="microsoft.migrate"
    resource="migrateprojects"  
    authors="ponatara"  
    ms.author="ponatara"  
    displayOrder=""  
    selfHelpType="generic"  
    supportTopicIds="32675754"  
    resourceTags=""  
    productPesIds="16348"  
    cloudEnvironments="public, Fairfax, usnat, ussec"  
    articleId="75vc6548-2a3f-4d0d-96c5-b2b5886483e6"  
    ownershipId="Compute_AzureMigrate"
/>

# Issues related to Movere, non-Microsoft tools (ISVs) and non-Server related Microsoft tools in Azure Migrate

## **Recommended Steps**

### **Issues with non-Microsoft tools**

For any issues related to registering the non-Microsoft/ISV tool, features of the tool, or to report any feedback, please reach out to the ISV/partner directly. You can find links to troubleshoot/open support tickets with ISVs in the table below:

- [Cloudamize](https://go.microsoft.com/fwlink/?linkid=2118542)
- [CorentTech](https://go.microsoft.com/fwlink/?linkid=2118704)
- [Device42](https://go.microsoft.com/fwlink/?linkid=2118619)
- [Turbonomic](https://go.microsoft.com/fwlink/?linkid=2118705)
- [UnifyCloud](https://go.microsoft.com/fwlink/?linkid=2118706)
- [Carbonite](https://go.microsoft.com/fwlink/?linkid=2118707)
- Rackware mail to:support@rackwareinc.com
- [Lakeside](https://go.microsoft.com/fwlink/?linkid=2118054)

### **Issues with Movere and non-Server related Microsoft tools**

- [Movere](https://go.microsoft.com/fwlink/?linkid=2118708)
- [WebApp(ASMA)](https://go.microsoft.com/fwlink/?linkid=2118709)

### **My Azure Migrate project creation fails with a deployment failed error**  

You can usually retry to fix this error. Click on the job notification for the failed deployment, navigate to "Deployments" and click on "Re-deploy" to retrigger the creation of the project and addition of the selected tools. This should solve the issue.

### **I want to create a new project in a different geography and add tools to it**  
  
If you need to specify a different geography to store discovery, assessment or migration related metadata (typically used for scenarios where your data centers are present in different geographies), go to 'Servers' or 'Databases' and click on 'Change' against the 'Migrate project (Change)' on the top-right corner of your screen. Then click on 'click here' to create a new Azure Migrate project. [Learn more](https://go.microsoft.com/fwlink/?linkid=2118620).

### **My added tools don't show up in the "Servers" or "Databases" page**

Make sure that you have selected the right project by clicking on 'Change' against 'Migrate project (Change)' on the top-right corner of your screen in 'Servers' or 'Databases'. Now choose the correct subscription and project name and click on 'OK'. The page should refresh with the added tools of the selected Azure Migrate project. [Learn more](https://go.microsoft.com/fwlink/?linkid=2118710)
  
### **I don't see the tool that I want to use**
  
We are constantly adding tools to Azure Migrate. [Learn more](https://go.microsoft.com/fwlink/?linkid=2118711).

### **ISV tools that are available in other geographies are not listed in Azure Government**

ISV partners are in process of enabling their tools in Azure Government for Azure Migrate. In the meanwhile, either you can use the partner tool independently or use any of the listed tools.
  
### **Do I need to pay for Azure Migrate and the non-Microsoft/ISV tools that I plan to use?**

Azure Migrate and the in-built Server Assessment, Server Migration tools are available at no additional charge. However, you may incur charges for other non-Microsoft/ISV assessment and migration tools you use while using Azure Migrate. [Learn more](https://go.microsoft.com/fwlink/?linkid=2118712).

### **I don't see a particular geography when creating the Azure Migrate project**

Azure Migrate is currently available in Asia, Europe, Japan, United Kingdom, United States, Canada, India, Australia and Azure Government. Teams are working continuously to make Azure Migrate available in remaining geographies, as and when the new geographies gets added the same shall be updated. You can use a project in any geography to perform a migration to an Azure region of your choice.
Review the supported geographies for [public](https://docs.microsoft.com/azure/migrate/migrate-support-matrix#supported-geographies-public-cloud) and [government clouds](https://docs.microsoft.com/azure/migrate/migrate-support-matrix#supported-geographies-azure-government).
