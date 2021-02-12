<properties
  pagetitle="Deployment issues with Azure Migrate appliance for Hyper-V &#xD;"
  service="microsoft.migrate"
  resource="migrateprojects"
  ms.author="vibansa"
  selfhelptype="Generic"
  supporttopicids="32675746"
  resourcetags=""
  productpesids="16348"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="75vc1276-2a3f-4d0d-96c5-b2e8886483e6"
  ownershipid="Compute_AzureMigrate" />
# Deployment issues with Azure Migrate appliance for Hyper-V 

## **Recommended Steps**

For general queries, refer to the documentation [here](https://docs.microsoft.com/azure/migrate/common-questions-appliance).


### Issues with setting up an appliance

* **I am unable to allocate the recommended hardware configuration to the appliance**

   The recommended [configuration](https://docs.microsoft.com/azure/migrate/migrate-appliance#appliance---hyper-v) is required to support the discovery and assessment of the Hyper-V VMs. Providing less than recommended configuration may have an impact on one of these operations.

* **I have a mixed on-premises environment with VMware VMs, Hyper-V VMs and physical servers. Can I discover all these using one Azure Migrate appliance?**

   You need to set up separate appliances for each scenario: VMware, Hyper-V, Physical servers. Each of the appliances can be registered to the same Azure Migrate project to assess the discovered servers together.

* **I don’t have enough resources to set up an appliance on-premises. Can I set up the appliance on an Azure VM?**

   No, setting up the appliance on an Azure VM is not recommended.


### Issues with the prerequisites check on appliance

* **I get an error in the Internet prerequisites check on the appliance**

   1.  Ensure that you can connect to the required [URLs](https://docs.microsoft.com/azure/migrate/migrate-appliance#url-access) from the appliance
   1.  Check if there is a proxy/firewall blocking access to these URLs. If allow listing is required, make sure to allow list all the URLs.
   1.  If there is a proxy server configured on-premises, ensure that you provide the proxy details correctly by selecting **Set up proxy** in the same step. Make sure that you provide the authorization credentials if the proxy needs them.
   1.  Ensure that the appliance server has not been previously used to set up the [replication appliance](https://docs.microsoft.com/azure/migrate/migrate-replication-appliance) or have mobility service agent installed on the server

* **I get an error in the auto update check on the appliance**

   Ensure that you have allow listed the required [URLs](https://docs.microsoft.com/azure/migrate/migrate-appliance#url-access) and no proxy/firewall setting is blocking the URLs. In case the update of any appliance component is failing, either rerun the prerequisites or follow these [steps](https://docs.microsoft.com/azure/migrate/migrate-appliance#manually-update-an-older-version) to manually update the component.

### Issues in registering the appliance with Azure Migrate _(New experience)_

* **After I successfully log in with an Azure user account, the appliance registration step fails with the message, "Failed to connect to the Azure Migrate project. Check the error details, follow the remediation steps on click on 'Retry' button"** 

   1. This issue happens when the Azure user account used to log in from the appliance configuration manager is not the same user account that was used to generate the Azure Migrate project key on the portal
   1. To complete the registration of the appliance, use the same Azure user account that generated the Azure Migrate project key on portal, or assign the required roles and [permissions](https://docs.microsoft.com/azure/migrate/tutorial-prepare-hyper-v#prepare-azure) to the other Azure user account which is used for appliance registration

* **I have issues when registering the appliance using the Azure Migrate project key copied from the project**

   1. Ensure that you have copied the correct key from the project. To check, on the **Server Assessment** card in your project, select **Discover** and then **Manage Existing appliance** in Step 1. Select the appliance name (for which you generated a key previously) from the menu and copy the corresponding key.
   1. Ensure that you are pasting the key to the appliance of the correct **cloud type** (Public/ US Gov) and **appliance type** (VMware/Hyper-V/Physical or other). Check at the top of appliance configuration manager to confirm the cloud and scenario type.

* **I am unable to complete registration due to insufficient AAD privileges and get the error, "Azure Active Directory (AAD) operation failed with status 'Forbidden' "**

   Ensure that you have the required [permissions](https://docs.microsoft.com/azure/migrate/tutorial-prepare-hyper-v#prepare-azure) to create and manage AAD Applications in Azure. You should have the Application Developer role, or the user role with **User can register applications allowed** at the tenant level.

* **I am unable to complete registration due to errors related to AAD Application operation failure**

   This error is encountered when the Azure user account used to initiate the discovery is different from the account used to register the appliance.<br>
   Do one of the following:
   * Ensure that the user account initiating the discovery is same as the one used to register the appliance
   * Provide AAD Application access permissions to the other user account for which the discovery operation is failing
   * Delete the Resource Group previously created for Azure Migrate project and create another Resource Group to start again

* **I have Key Vault create/update issues during appliance registration**

   Refer to this [document](https://docs.microsoft.com/azure/migrate/troubleshoot-appliance-discovery#error-6003060031-key-vault-management-operation-failed) for different types of Key Vault related errors and their remediation steps.

### Issues in adding Hyper-V hosts/clusters

* **I cannot connect to the Hyper-V host/cluster due to incorrect credentials or insufficient permissions**

   Verify the credentials provided for Hyper-V host/cluster. The local or domain user account provided should either be a part of an Administrators security group, or should be a part of the following groups: Remote Management Users, Hyper-V Administrators, and Performance Monitor Users.

* **I get WinRM errors while validating Hyper-V hosts/clusters**

   Using PowerShell as an administrator, run the `winrm qc` and `Enable-PSRemoting` commands on the Hyper-V hosts to be discovered. Ensure that WinRM ports 5985 (HTTP) is open. You can also do this by running the [Hyper-V prerequisites configuration script](https://docs.microsoft.com/azure/migrate/tutorial-prepare-hyper-v#hyper-v-prerequisites-configuration-script).

* **I get an error that the host names in the cluster cannot be resolved**

   Hyper-V Hosts in a cluster may not be reachable due to a name resolution issue. Get the DNS to resolve the host names if it is not an FQDN. If this is not feasible, update the **hosts** file on the appliance to map the IP address with the host names.

### Issues post discovery initiation

* **Some performance data is missing on servers in the assessment I created**

   Refer to this [document](https://docs.microsoft.com/azure/migrate/troubleshoot-assessment#why-is-performance-data-missing-for-someall-vms-in-my-assessment-report) for different types of performance data missing issues and their remediation steps.
