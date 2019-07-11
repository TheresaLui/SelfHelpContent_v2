<properties 
    pageTitle="Deployment issues with Azure Migrate appliance for VMware "
    description="Issues and guidance regarding deployment issues in Azure Migrate appliance for VMware"
    service="microsoft.migrate"
    resource="migrateprojects"
    authors="vikram1988"
    ms.author="vibansa"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32675747, 32675748"
    resourceTags=""
    productPesIds="16348"
    cloudEnvironments="public"
    articleId="75vc4298-4f6f-4d8e-96c5-b2b5886483e6"
/>

# Deployment issues with Azure Migrate appliance for VMWare

## **Recommended steps**

## Issues with the prerequisites check on appliance

### **I am getting an error in the Internet prerequisite check on the appliance.**

The appliance should have Internet connectivity (either directly or via a proxy). Ensure you are able to connect to the URLs listed [here](https://aka.ms/migrate/selfhelp/appliancevmware/urls). If whitelisting is required, please ensure you whitelist all the URLs.

## Issues in registering the appliance with Azure Migrate

### **I am unable to register the appliance to Azure Migrate due to insufficient permissions on the subscription.** 

Ensure that the Azure user account used to register the appliance has at least the Contributor role on the subscription. You can check for the required Azure roles and permissions [here](https://aka.ms/migrate/selfhelp/appliancevmware/azureperms).

## Issues in adding vCenter Server

### **I am unable to connect to vCenter Server due to incorrect credentials or insufficient permissions.**

Verify the credentials provided for vCenter Server. You’ll need a read-only account to access the vCenter Server managing the VMs you want to discover.

## Issues after hitting 'Save and start discovery'

### **I am unable to initiate discovery due to insufficient AAD privileges.**

Ensure that you have the required [permissions](https://aka.ms/migrate/selfhelp/appliancevmware/azureperms) to create and manage AAD Applications in Azure. You should have "Application Developer" role or user role with "User can register applications" allowed at the tenant level.

### **I am unable to initiate discovery due to errors related to AAD Application operation failure.**

This error is encountered when the Azure user account used to initiate the discovery is different from the account used to register the appliance. You can do one of the following:

1. Ensure that the user account initiating the discovery is same as the one used to register the appliance

2. Provide AAD Application access permissions to the other user account for which the discovery operation is failing

3. Delete the Resource Group previously created for Azure Migrate project and create another Resource Group to start again

### **I am getting errors related to discovery operation failure due to conflict in creation of some Migrate artifacts.**

This error indicates a previous discovery operation is still ongoing. Please wait for some time and review the list of machines discovered on Azure portal. If you see the machines are still not discovered, start discovery again on the appliance.
