<properties
  pagetitle="Discovery issues with import"
  description="Discovery issues with import"
  service="microsoft.migrate"
  resource="migrateprojects"
  ms.author="anvar,deseelam"
  selfhelptype="Generic"
  supporttopicids="32691006"
  resourcetags=""
  productpesids="16348"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="3a672f3a-1f25-4ba7-92f8-cecd50db4ebc"
  ownershipid="Compute_AzureMigrate" />
# Discovery issues with import

## **Recommended Steps**

### **Where can I find documentation on the fields in the CSV template?**
See [this tutorial](https://docs.microsoft.com/azure/migrate/tutorial-assess-import#add-server-information).

### **I imported a CSV but I see the message, "Discovery is in progress"** 
This can happen if your CSV upload failed due to a validation problem. Try to import the CSV again. You can download the error report of the previous upload and follow the remediation guidance in the file to fix the errors. Download the error report from the Import details section on the Discover machines page.

### **Error: The file uploaded is not in the expected format**
Some tools have regional settings that create the CSV file with semicolon as a delimiter. Change the settings to ensure that the delimiter is a comma.

### **How can I delete the imported servers?**
Currently, deleting servers is not possible. You can overwrite a server by importing another entry with the same server name. 

### **I want to add more than 2 disks, but I see columns for only 2 disks in the template**
Disk details can be added for up to 8 disks. You can add details for more disks by adding columns in the template. [Learn more](https://docs.microsoft.com/azure/migrate/tutorial-assess-import#add-multiple-disks).

### **How can I prepare the CSV file to import servers?**
You can export server inventory from tools that you use for on-premises server management, such as VMware vSphere or your configuration-management database (CMDB).

### I am unable to import/export the CSV template (for Azure Migrate projects with private endpoint connectivity only).
This error may occur if the import/export request was not initiated from an authorized network. Retry the operation from a client residing in a virtual network that’s connected to Azure by using Azure Private Link.
