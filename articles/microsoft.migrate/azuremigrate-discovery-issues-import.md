<properties
    pageTitle="Discovery issues with import"
    description="Discovery issues with import"
    service="microsoft.migrate"
    resource="migrateprojects"
    authors="An-mol"
    ms.author="anvar"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32691006"
    resourceTags=""
    productPesIds="16348"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="3a672f3a-1f25-4ba7-92f8-cecd50db4ebc"
	ownershipId="Compute_AzureMigrate"
/>

# Discovery issues with import

## **Recommended Steps**

### **Where can I find documentation on the fields in the CSV template?**
Documentation on the fields in the CSV template is available [here](https://docs.microsoft.com/azure/migrate/tutorial-assess-import#add-server-information).

### **I imported a CSV but I see "Discovery is in progress"**
This can happen if your CSV upload failed due to a validation problem. Try to import the CSV again. You can download the error report of the previous upload and follow the remediation guidance in the file to fix the errors. The error report can be downloaded from the 'Import Details' section on 'Discover machines' page.

### **Error: The file uploaded is not in the expected format**
Some tools have regional settings that create the CSV file with semi-colon as a delimiter. Please change the settings to ensure the delimiter is a comma.

### **How can I delete the imported servers?**

Currently, deleting servers is not feasible. You can overwrite a server by importing another entry with the same server name. 

### **I want to add more than 2 disks, but I see columns for only 2 disks in the template.**

Disk details can be added for up to 8 disks. You can add details for more disks by adding columns in the template. [Learn more](https://docs.microsoft.com/azure/migrate/tutorial-assess-import#add-multiple-disks) about how you can add more than 2 disks in the CSV.

### **How can I prepare the CSV file to import servers?**
You can export server inventory from tools you use for on-premises server management, such as VMware vSphere or your configuration-management database (CMDB).



