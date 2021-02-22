<properties
  pagetitle="Deployment issues with Azure Migrate appliance for VMware&#xD;"
  service="microsoft.migrate"
  resource="migrateprojects"
  ms.author="vibansa"
  selfhelptype="Generic"
  supporttopicids="32675747,32675748,32755157"
  resourcetags=""
  productpesids="16348"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="75vc4298-4f6f-4d8e-96c5-b2b5886483e6"
  ownershipid="Compute_AzureMigrate" />
# Deployment issues with Azure Migrate appliance for VMware

Resolve deployment issues with the Azure Migrate appliance for VMware using the following steps.

## **Recommended Steps**

For general queries, see [common questions about Azure Migrate appliance for VMware](https://docs.microsoft.com/azure/migrate/common-questions-appliance)

### Issues with setting up an appliance

* **I am unable to create a VM and set up an appliance using the OVA template downloaded from the Azure Migrate project**

   If you are unable to use the OVA file, download the [PowerShell installer script](https://docs.microsoft.com/azure/migrate/deploy-appliance-script#set-up-the-appliance-for-vmware) to set up the appliance on an existing VM or a physical server running Windows Server 2016 with the required hardware configuration.

* **I am unable to allocate the recommended hardware configuration to the appliance while setting it up using OVA file or the PowerShell installer script**

   The appliance requires this [hardware configuration](https://docs.microsoft.com/azure/migrate/migrate-appliance#appliance---vmware) to support the discovery, assessment, and agentless migration of the VMware VMs. Providing less than the recommended configuration may impact these operations.

* **I have a mixed on-premises environment with VMware VMs, Hyper-V VMs and physical servers. Can I discover all these using one Azure Migrate appliance?**

   You need to set up separate appliances for each scenario: VMware, Hyper-V, physical servers. Each of the appliances can be registered to the same Azure Migrate project to assess the discovered servers together.

* **I don’t have enough resources to set up an appliance on-premises. Can I set up the appliance on an Azure VM?**

   No, setting up the appliance on an Azure VM is not recommended.
   

### Issues with the prerequisites check on appliance

* **I am getting an error message in the internet prerequisites check on the appliance**

   1. Ensure that you can connect to the required [URLs](https://docs.microsoft.com/azure/migrate/migrate-appliance#url-access) from the appliance
   1. Check if there is a proxy/firewall blocking access to these URLs. If you are required to create an allow list, ensure that you include all the URLs.
   1. If there is a proxy server configured on-premises, ensure that you provide the proxy details correctly by selecting **Setup proxy** in the same step. Ensure that you provide the authorization credentials if the proxy needs them.
   1. Make sure that the appliance server has not been previously used to set up the [replication appliance](https://docs.microsoft.com/azure/migrate/migrate-replication-appliance) and that you have the mobility service agent installed on the server

* **I am getting an error in the auto update check on the appliance**

   Ensure that you have created an allow list for the required [URLs](https://docs.microsoft.com/azure/migrate/migrate-appliance#url-access) and that no proxy/firewall setting is blocking the URLs. If the update of any appliance component is failing, either rerun the prerequisites or [manually update the component](https://docs.microsoft.com/azure/migrate/migrate-appliance#manually-update-an-older-version).
   

### Issues in registering the appliance with Azure Migrate _(New experience)_

* **After a successful login with an Azure user account, the appliance registration step fails with the message "Failed to connect to the Azure Migrate project. Check the error detail and follow the remediation steps by clicking Retry"** 

   This issue happens when the Azure user account used to log in from the appliance configuration manager is different from the user account used to generate the Azure Migrate project key on the Azure portal 
   To complete the registration of the appliance, use the same Azure user account that generated the Azure Migrate project key on the portal, or assign the required roles and [permissions](https://docs.microsoft.com/azure/migrate/tutorial-prepare-vmware#prepare-azure) to the other Azure user account that is used for appliance registration

* **I am having issues when I try to register the appliance using the Azure Migrate project key copied from the project**

   1. Ensure that you have copied the correct key from the project. To check, on the **Server Assessment** card in your project, select **Discover** and then **Manage Existing appliance** in Step 1. Select the appliance name (for which you generated a key previously) from the drop-down menu and copy the corresponding key.
   2. Ensure that you are pasting the key to the appliance of the right **cloud type** (Public/ US Gov) and **appliance type** (VMware/Hyper-V/Physical or other). Check at the top of appliance configuration manager to confirm the cloud and scenario type.

* **I am unable to complete registration due to insufficient AAD privileges and get the error, "Azure Active Directory (AAD) operation failed with status Forbidden"**

   Ensure that you have the required [permissions](https://docs.microsoft.com/azure/migrate/tutorial-prepare-vmware#prepare-azure) to create and manage AAD Applications in Azure. You should have the Application Developer role or the user role with **User can register applications** allowed at the tenant level.

* **I am unable to complete registration due to errors related to AAD Application operation failure**

   This error occurs when the Azure user account used to initiate the discovery is different from the account used to register the appliance. <br>
Do one of the following:
   * Ensure that the user account initiating the discovery is same as the one used to register the appliance
   * Provide AAD Application access permissions to the other user account for which the discovery operation is failing
   * Delete the Resource Group previously created for Azure Migrate project and create another Resource Group to start again

* **I am experiencing Key Vault create/update issues during appliance registration**

   See [troubleshoot appliance discovery errors](https://docs.microsoft.com/azure/migrate/troubleshoot-appliance-discovery#error-6003060031-key-vault-management-operation-failed) for different types of Key Vault related errors and their remediation steps.


### Issues in adding credentials and discovery sources

* **I am unable to connect to vCenter Server due to incorrect credentials or insufficient permissions**

   Verify the credentials provided for vCenter Server. You’ll need a **read-only account** to access the vCenter Server managing the VMs that you want to discover. If you want to scope discovery to specific VMware objects (e.g., vCenter Server datacenters, clusters, a folder of clusters, hosts, a folder of hosts, or individual VMs), follow these [steps](https://docs.microsoft.com/azure/migrate/set-discovery-scope). 

* **I am unable to add multiple vCenter servers on the appliance configuration manager**

   Adding multiple vCenter Servers to a single appliance is not currently supported. There is a one-to-one relation between appliance and a vCenter server. To discover multiple vCenter servers, you must deploy multiple appliances. You can register multiple appliances to the same Azure Migrate project. [Learn more](https://docs.microsoft.com/azure/migrate/scale-vmware-assessment#planning-limits) about how to discover multiple vCenter servers.

* **I don’t have vCenter Server details, can I discover VMware VMs by providing ESXi host details?**

   Currently, this is not supported. If you don't have the vCenter Server details, you can discover the VMs by treating them as physical servers and using the [physical server appliance](https://docs.microsoft.com/azure/migrate/how-to-set-up-appliance-physical) to discover VMs. 
   

### Issues post discovery initiation

* **I can't change the vCenter server details after starting the discovery using the appliance**

   You cannot change the vCenter Server details after you've started the discovery using the appliance. To discover another vCenter Server, you'll need to deploy a new appliance.

* **Some performance data is missing on VMs in the assessment I created**

   See [troubleshoot assessments](https://docs.microsoft.com/azure/migrate/troubleshoot-assessment#why-is-performance-data-missing-for-someall-vms-in-my-assessment-report) for different types of performance data missing issues and remediation steps.
