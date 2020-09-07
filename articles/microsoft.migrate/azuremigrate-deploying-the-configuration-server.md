<properties
    pageTitle="Deploying the replication appliance(Configuration Server)"
    description="Troubleshooting issues while deploying the replication appliance(Configuration Server)"
    service="microsoft.migrate"
    resource="migrateprojects"
    authors="anvar-ms"
    ms.author="anvar"
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
 
- Ensure replication appliance is configured on a different machine to the one used for Azure Migrate discovery and assessment
- Ensure replication appliance is not configured on source machine to be replicated

### ***Installation issues with Mobility Agent***
	
Mobility agent installation is not supported on machines that have secure boot enabled. Disable the secure boot and try to install the agent.

- Check if installation failed due to missing OS updates. [Learn more](https://go.microsoft.com/fwlink/?linkid=2141033)
- Check if installation failed due to insufficient boot space on Linux VMs. [Learn more](https://go.microsoft.com/fwlink/?linkid=2140828)

### **Configuration Server registration failing due to permissions (requires admin approval)**

If you are deploying the replication appliance on VMware using the .ova template, you'll need permissions to register an AAD application and to consent to delegated permissions to access resources. You'll see a message asking for admin approval during appliance configuration if the tenant administrator of your Azure account hasn't given you permissions to provide user consent. [Learn more](https://go.microsoft.com/fwlink/?linkid=2140829).

If you are unable to consent to the necessary permissions, you can do one of the following:

- You can ask your tenant admin to provide all users in the tenant the ability to consent to delegate permissions
- You can ask your tenant admin to assign the 'Application Developer' role to you. [Learn more](https://go.microsoft.com/fwlink/?linkid=2140830)
- You can ask your tenant admin to grant consent to the AAD application created by the replication appliance (the AAD application name is displayed when admin approval is requested

If none of the above options are feasible, you can install the replication appliance software on a Windows Server 2016 machine using the software installer. [Prepare the replication appliance](https://go.microsoft.com/fwlink/?linkid=2141034) like you would for migration of physical servers. The registration experience for the installer based replication appliance doesn't register an AAD app and doesn't require the AAD roles/permissions referenced above.

After completing registration of the appliance, finalize registration of the replication appliance (Click Discover on the Server Migration tool tile in the Azure portal > Select VMware, install new replication appliance, select the replication appliance that you registered by friendly name, and click finalize registration.)

To add a vCenter, click Overview on the Server Migration tool tile, select Infrastructure Servers from the left menu, and select the replication appliance to drill down to the replication appliance page. Click +vCenter on the replication appliance page to add a vCenter server to the appliance.

