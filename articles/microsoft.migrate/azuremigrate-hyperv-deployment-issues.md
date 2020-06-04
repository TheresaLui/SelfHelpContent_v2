
<properties 
    pageTitle="Deployment issues with Azure Migrate appliance for Hyper-V "
    description="Issues and guidance regarding deployment issues in Azure Migrate appliance for Hyper-V"
    service="microsoft.migrate"
    resource="migrateprojects"
    authors="vikram1988"
    ms.author="vibansa"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32675746"
    resourceTags=""
    productPesIds="16348"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="75vc1276-2a3f-4d0d-96c5-b2e8886483e6"
	ownershipId="Compute_AzureMigrate"
/>

# Deployment issues with Azure Migrate appliance for Hyper-V 

## **Recommended Steps**

### Issues with the prerequisites check on appliance

**I am getting an error in the Internet prerequisite check on the appliance**

The appliance should have Internet connectivity (either directly or via a proxy). Ensure that you are able to connect to the URLs listed [here](https://docs.microsoft.com/azure/migrate/migrate-support-matrix-hyper-v#assessment-appliance-url-access). If whitelisting is required, please ensure you whitelist all the URLs. For Azure Government customers, ensure that you are able to connect to the URLs listed [here](https://docs.microsoft.com/azure/migrate/migrate-appliance#government-cloud-urls).

### Issues in registering the appliance with Azure Migrate

**I am unable to register the appliance to Azure Migrate due to insufficient permissions on the subscription** 

Ensure that the Azure user account used to register the appliance has at least the Contributor role on the subscription. You can check for the required Azure roles and permissions [here](https://docs.microsoft.com/azure/migrate/tutorial-prepare-hyper-v#azure-permissions).

**I am unable to see the list of customer subscriptions in the Subscriptions drop-down, when logged in using my CSP credentials on the appliance**

Currently, listing of the customer subscriptions managed by a CSP partner is not supported. To register the appliance with an Azure Migrate project in a customer subscription, you need to log in with Azure user account from the customer's tenant to see their subscription(s) in the drop-down.

### Issues in adding Hyper-V hosts

**I am unable to connect to the Hyper-V host/cluster due to incorrect credentials or insufficient permissions**

Verify the credentials provided for Hyper-V host/cluster. The local or domain user account provided should either be a part of "Administrators" security group or should be a part of the following groups: Remote Management Users, Hyper-V Administrators and Performance Monitor Users.

**I am facing WinRM errors while validating Hyper-V hosts/clusters**

Execute 'winrm qc' and 'Enable-PSRemoting' commands using PowerShell as an administrator on the Hyper-V hosts to be discovered. Ensure that WinRM ports 5985 (HTTP) and 5986 (HTTPS) are open. You can also do this by running the [Hyper-V prerequisites configuration script](https://docs.microsoft.com/azure/migrate/tutorial-prepare-hyper-v#hyper-v-prerequisites-configuration-script).

**I am getting an error that the host name(s) in the cluster cannot be resolved**

Hyper-V Hosts in a cluster may not be reachable due to a name resolution issue. It is advised to get the DNS to resolve the host names if it is not an FQDN. If this is not feasible, update the hosts file on the appliance to map the IP address with the host names.

### Issues after hitting Save and Start discovery

**I am unable to initiate discovery due to insufficient AAD privileges**

Ensure that you have the required [permissions](https://docs.microsoft.com/azure/migrate/tutorial-prepare-hyper-v#azure-permissions) to create and manage AAD application in Azure. The user that you use should have the "Application Developer" role or user role with 'User can register applications' allowed at the tenant level.

**I am unable to initiate discovery due to errors related to AAD application operation failure**

This error is encountered when the Azure user account used to initiate the discovery is different from the account used to register the appliance. You can do one of the following:

1. Ensure that the user account initiating the discovery is same as the one used to register the appliance
2. Provide AAD application access permissions to the other user account for which the discovery operation is failing
3. Delete the Resource Group previously created for Azure Migrate project and create another Resource Group to start again

**I am getting errors related to Discovery operation failure due to conflict in creation of some Migrate artifacts**

This error indicates a previous discovery operation is still ongoing. Please wait for some time and review the list of machines discovered on Azure portal. If you see the machines are still not discovered, start Discovery again on the appliance.
