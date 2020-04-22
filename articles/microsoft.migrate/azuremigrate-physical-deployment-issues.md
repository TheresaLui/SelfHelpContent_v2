
<properties 
    pageTitle="Deployment issues with Azure Migrate appliance for physical server assessment "
    description="Issues and guidance regarding deployment issues in Azure Migrate appliance for physical server assessment"
    service="microsoft.migrate"
    resource="migrateprojects"
    authors="vikram1988"
    ms.author="vibansa"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32691005"
    resourceTags=""
    productPesIds="16348"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="75vc1276-2a3f-4d0d-96c5-b2e8886483eb"
    ownershipId="Compute_AzureMigrate"
/>

# Deployment issues with Azure Migrate appliance for physical server assessment

## **Recommended Steps**

### Issues with the prerequisites check on appliance

**I am getting an error in the Internet prerequisite check on the appliance**

The appliance should have Internet connectivity (either directly or via a proxy). Ensure that you are able to connect to the URLs listed [here](https://docs.microsoft.com/azure/migrate/migrate-support-matrix-physical#assessment-appliance-url-access). If whitelisting is required, please ensure you whitelist all the URLs. For Azure Government customers, ensure that you are able to connect to the URLs listed [here](https://docs.microsoft.com/azure/migrate/migrate-appliance#government-cloud-urls)

### Issues in registering the appliance with Azure Migrate

**I am unable to register the appliance to Azure Migrate due to insufficient permissions on the subscription** 

Ensure that the Azure user account used to register the appliance has at least the Contributor role on the subscription. You can check for the required Azure roles and permissions [here](https://docs.microsoft.com/azure/migrate/tutorial-prepare-physical#azure-permissions).

**I am unable to see the list of customer subscriptions in the Subscriptions drop-down, when logged in using my CSP credentials on the appliance**

Currently, listing of the customer subscriptions managed by a CSP partner is not supported. To register the appliance with an Azure Migrate project in a customer subscription, you need to log in with Azure user account from the customer's tenant to see their subscription(s) in the drop-down.

### Issues in adding physical servers

**I am unable to connect to the physical server due to incorrect credentials or insufficient permissions**

Verify the credentials provided for the physical server. For Windows servers, set up a local user account on all the Windows servers that you want to include in the discovery.The user account needs to be added to these groups-Remote Desktop Users, Performance Monitor Users and Performance Log users.
For Linux servers, you need a root account on the Linux servers that you want to discover.

**I am facing WinRM errors while validating Windows servers**

Execute 'winrm qc' and 'Enable-PSRemoting' commands using PowerShell as an administrator on the server to be discovered. Ensure that WinRM ports 5985 (HTTP) and 5986 (HTTPS) are open.

### Issues after hitting Save and Start discovery

**I am unable to initiate discovery due to insufficient AAD privileges**

Ensure that you have the required [permissions](https://docs.microsoft.com/azure/migrate/tutorial-prepare-physical#azure-permissions) to create and manage AAD application in Azure. The user that you use should have the "Application Developer" role or user role with 'User can register applications' allowed at the tenant level.

**I am unable to initiate discovery due to errors related to AAD application operation failure**

This error is encountered when the Azure user account used to initiate the discovery is different from the account used to register the appliance. You can do one of the following:

1. Ensure that the user account initiating the discovery is same as the one used to register the appliance
2. Provide AAD application access permissions to the other user account for which the discovery operation is failing
3. Delete the Resource Group previously created for Azure Migrate project and create another Resource Group to start again

**I am getting errors related to Discovery operation failure due to conflict in creation of some Migrate artifacts**

This error indicates a previous discovery operation is still ongoing. Please wait for some time and review the list of machines discovered on Azure portal. If you see the machines are still not discovered, start Discovery again on the appliance.
