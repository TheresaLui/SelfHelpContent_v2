
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

For general queries, please refer to the documentation [here](https://docs.microsoft.com/azure/migrate/common-questions-appliance).

### Issues with setting up an appliance


**I am unable to allocate the recommended hardware configuration to the appliance while setting it up**

The recommended [configuration](https://docs.microsoft.com/azure/migrate/migrate-appliance#appliance---physical) is required for the appliance to support the discovery and assessment of the physical servers. Providing less than recommended configuration may have an impact on one of these operations.

**I have a mixed on-premises environment with VMware VMs, Hyper-V VMs and physical servers. Can I discover all these using one Azure Migrate appliance?**

You need to set up separate appliances for each scenario- VMware/ Hyper-V/ Physical servers. Each of the appliances can be registered to the same Azure Migrate project to assess the discovered servers together.


**I don’t have enough resources to set up an appliance on-premises. Can I set up the appliance on an Azure VM?**

No, setting up the appliance on an Azure VM is not recommended.

### Issues with the prerequisites check on appliance

**I am getting an error in the Internet prerequisite check on the appliance**

1. Ensure that you can connect to the required [URLs](https://docs.microsoft.com/azure/migrate/migrate-appliance#url-access) from the appliance.
2. Check if there is a proxy/firewall blocking access to these URLs. If whitelisting is required, please ensure you whitelist all the URLs.
3. If there is a proxy server configured on-premises, ensure that you provide the proxy details correctly by clicking on “Setup proxy” in the same step. Make sure you provide the authorization credentials if the proxy needs them.
4. Ensure that the appliance VM has not been previously used to set up the [replication appliance](https://docs.microsoft.com/azure/migrate/migrate-replication-appliance) or have mobility service agent installed on the VM.

**I am getting an error in the auto update check on the appliance**

Ensure that you have whitelisted  the required [URLs](https://docs.microsoft.com/azure/migrate/migrate-appliance#url-access) and no proxy/firewall setting is blocking the URLs. In case the update of any appliance component is failing, either rerun the prerequisites or follow these [steps](https://docs.microsoft.com/azure/migrate/migrate-appliance#manually-update-an-older-version) to manually update the component.

### Issues in registering the appliance with Azure Migrate

**I am unable to register the appliance to Azure Migrate due to insufficient permissions on the subscription** 

Ensure that the Azure user account used to register the appliance has at least the Contributor role on the subscription. You can check for the required Azure roles and permissions [here](https://docs.microsoft.com/azure/migrate/tutorial-prepare-physical#azure-permissions).

**I am unable to see the list of customer subscriptions in the Subscriptions drop-down, when logged in using my CSP credentials on the appliance**

Currently, listing of the customer subscriptions managed by a CSP partner is not supported. To register the appliance with an Azure Migrate project in a customer subscription, you need to log in with Azure user account from the customer's tenant to see their subscription(s) in the drop-down.

### Issues in adding physical servers

**I am unable to connect to the physical server due to incorrect credentials or insufficient permissions**

Verify the credentials provided for the physical server: 

**Windows:** Use a domain account for domain-joined machines, and a local account for machines that are not domain-joined. The user account should be added to these groups: Remote Management Users, Performance Monitor Users, and Performance Log Users.

**Linux:** You need a root account on the Linux servers that you want to discover.

**I am unable to provide SSH key based credentials for Linux servers**

Currently SSH key based credentials are not supported as an input on the appliance for Linux servers.


**I am facing WinRM errors while validating Windows servers**

Execute 'winrm qc' and 'Enable-PSRemoting' commands using PowerShell as an administrator on the server to be discovered. Ensure that WinRM ports 5985 (HTTP) is open.

### Issues after hitting Save and Start discovery

**I am unable to initiate discovery due to insufficient AAD privileges and seeing the error- Azure Active Directory (AAD) operation failed with status "Forbidden"**

Ensure that you have the required [permissions](https://docs.microsoft.com/azure/migrate/tutorial-prepare-physical#azure-permissions) to create and manage AAD application in Azure. The user that you use should have the "Application Developer" role or user role with 'User can register applications' allowed at the tenant level.

**I am unable to initiate discovery due to errors related to AAD application operation failure**

This error is encountered when the Azure user account used to initiate the discovery is different from the account used to register the appliance. You can do one of the following:

1. Ensure that the user account initiating the discovery is same as the one used to register the appliance
2. Provide AAD application access permissions to the other user account for which the discovery operation is failing
3. Delete the Resource Group previously created for Azure Migrate project and create another Resource Group to start again


**I am getting Key Vault create/update issues after clicking on 'Save and start discovery'**

Refer to this [document](https://docs.microsoft.com/azure/migrate/troubleshoot-appliance-discovery#error-6003060031-key-vault-management-operation-failed) for different types of Key Vault related errors and their remediation steps.

### Issues post discovery initiation

**I am seeing some performance data is missing on servers in the assessment I created**

Refer to this [document](https://docs.microsoft.com/azure/migrate/troubleshoot-assessment#why-is-performance-data-missing-for-someall-vms-in-my-assessment-report) for different types of performance data missing issues and their remediation steps.