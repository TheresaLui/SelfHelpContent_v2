<properties
    pageTitle="Deploying the replication appliance(Configuration Server)"
    description="Troubleshooting issues while deploying the replication appliance(Configuration Server)"
    service="microsoft.migrate"
    resource="migrateprojects"
    authors="bsiva"
    ms.author="bsiva"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32675745"
    resourceTags=""
    productPesIds="16348"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="f1a6ef2d-defb-4b92-a779-de3a118e6dd1"
	ownershipId="Compute_AzureMigrate"
/>

# Deploying the replication appliance (Configuration Server)

## **Recommended Steps**

### **Configuration Server registration requires admin approval to grant permissions**

If you are deploying the replication appliance on VMware using the .ova template, you'll need permissions to register an AAD application and to consent to delegated permissions to access resources. You'll see a message asking for admin approval during appliance configuration if the tenant administrator of your Azure account hasn't given you permissions to provide user consent. [Learn more](https://aka.ms/migrate/replication_appliance_permissions).

If you are unable to consent to the necessary permissions, you can do one of the following:

- You can ask your tenant admin to provide all users in the tenant the ability to consent to delegate permissions

- You can ask your tenant admin to assign the 'Application Developer' role to you. [Learn more](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles)

- You can ask your tenant admin to grant consent to the AAD application created by the replication appliance (the AAD application name is displayed when admin approval is requested

If none of the above options are feasible, you can install the replication appliance software on a Windows Server 2016 machine using the software installer. [Prepare the replication appliance](https://aka.ms/migrate/replication_appliance_for_physical) like you would for migration of physical servers. The registration experience for the installer based replication appliance doesn't register an AAD app and doesn't require the AAD roles/permissions referenced above.

After completing registration of the appliance, finalize registration of the replication appliance (Click Discover on the Server Migration tool tile in the Azure portal > Select VMware, install new replication appliance, select the replication appliance that you registered by friendly name, and click finalize registration.)

To add a vCenter, click Overview on the Server Migration tool tile, select Infrastructure Servers from the left menu, and select the replication appliance to drill down to the replication appliance page. Click +vCenter on the replication appliance page to add a vCenter server to the appliance.

### **The replication appliance (Configuration Server) status is 'Not connected'**

Validate the following:

- The replication appliance is running

- The time on the system clock and the time zone settings on the replication appliance are accurate

- The following services on the replication appliance are running (Run > services.msc to see the list of services): 'cxprocessserver', 'InMage Scout VX Agent – Sentinel/Outpost', 'Microsoft Azure Site Recovery Service', 'Microsoft Azure Recovery Services Agent', 'tmansvc'

- Inbound ports TCP 443 and TCP 9443 on the replication servers are open and are not being blocked by the Windows firewall or a network firewall device

- The replication appliance is able to make outbound connections on port 443 and has access to the following URLS:

  - *.backup.windowsazure.com
  
  - *.store.core.windows.net
  
  - *.blob.core.windows.net
  
  - *.hypervrecoverymanager.windowsazure.com
  
  - https://management.azure.com
  
  - *.services.visualstudio.com
  
  - time.windows.com

- If there is a web filtering proxy between the replication appliance and the internet, ensure that the above URIs are whitelisted for access (including possible canonical name resolution for some of the URIs)
