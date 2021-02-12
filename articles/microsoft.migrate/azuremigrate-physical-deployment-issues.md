<properties
  pagetitle="Deployment issues with Azure Migrate appliance for physical server assessment&#xD;"
  service="microsoft.migrate"
  resource="migrateprojects"
  ms.author="vibansa"
  selfhelptype="Generic"
  supporttopicids="32691005"
  resourcetags=""
  productpesids="16348"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="75vc1276-2a3f-4d0d-96c5-b2e8886483eb"
  ownershipid="Compute_AzureMigrate" />
# Deployment issues with Azure Migrate appliance for physical server assessment

Most customers can resolve deployment issues with Azure Migrate appliance using the following resources.

## **Recommended Steps**

For general queries about Azure Migrate appliance, refer to the [documentation](https://docs.microsoft.com/azure/migrate/common-questions-appliance). <br>


### Issues setting up an appliance

* **I am unable to allocate the recommended hardware configuration to the appliance while setting it up**

    For the appliance to support both the discovery and assessment of the physical servers, make sure that you meet the [configuration requirements](https://docs.microsoft.com/azure/migrate/migrate-appliance#appliance---physical). Not meeting the recommended configuration can have an impact on one of these operations.


* **I have a mixed on-premises environment with VMware VMs, Hyper-V VMs, and physical servers. Can I discover all of these using one Azure Migrate appliance?**

    You must set up separate appliances for each scenario (that is, for VMware VMs, Hyper-V VMs, and physical servers). Each of the appliances can be registered to the same Azure Migrate project to assess the discovered servers together.


* **I don’t have enough resources to set up an appliance on-premises. Can I set up the appliance on an Azure VM?**

    No, setting up the appliance on an Azure VM is not recommended.<br><br>

### Issues with the prerequisites check on appliance

* **I get an error during the Internet prerequisites check**
    * Ensure that you can connect to the required [URLs](https://docs.microsoft.com/azure/migrate/migrate-appliance#url-access) from the appliance.
    * Check if a proxy/firewall is blocking access to these URLs. If allow listing is required, make sure that you allow list all of the URLs.
    * If a proxy server is configured on-premises, provide the proxy details by selecting **Set up proxy** in the same step. Make sure that you provide the authorization credentials if the proxy needs them.
    * Ensure that the appliance server has not been previously used to set up the [replication appliance](https://docs.microsoft.com/azure/migrate/migrate-replication-appliance) or have mobility service agent installed on the server.

* **I get an error during the auto update check**

    Include all of the [required URLs](https://docs.microsoft.com/azure/migrate/migrate-appliance#url-access) to the allow list, and make sure they are not blocked by proxy or firewall settings. If the update of any appliance component fails, manually update the component either by rerunning the prerequisites, or by following these [steps](https://docs.microsoft.com/azure/migrate/migrate-appliance#manually-update-an-older-version).<br><br>

### Issues in registering the appliance with Azure Migrate _(New experience)_

* **After a successful login with my Azure user account, the appliance registration step fails with the message, "Failed to connect to the Azure Migrate project. Check the error details, follow the remediation steps, or click on 'Retry' button"**. 

    This issue occurs when you log in from the Appliance configuration manager using a different Azure user account than the account used to generate the Azure Migrate project key on the Azure portal.
    * To complete the registration of the appliance, use the same Azure user account that generated the Azure Migrate project key on the Azure portal. Or, assign the required roles and [permissions](https://docs.microsoft.com/azure/migrate/tutorial-prepare-physical#prepare-azure-for-server-assessment) to the Azure user account that received the error, and then register the appliance.

* **I am having issues when I try to register the appliance using the Azure Migrate project key copied from the project**

    * Ensure that you have copied the correct key from the project. To check, on the **Server Assessment** card in your project, select  **Discover** and **Manage Existing appliance** in Step 1. From the menu, select the appliance name (for which you generated a key previously) and copy the corresponding key.
    * Ensure that you are pasting the key to the appliance of the right **cloud type** (Public/US Gov) and **appliance type** (VMware/Hyper-V/Physical or other). Check at the top of appliance configuration manager to confirm the cloud and scenario type.

* **I am unable to complete registration due to insufficient AAD privileges and get the error "Azure Active Directory (AAD) operation failed with status 'Forbidden' "**

    Ensure that you have the required [permissions](https://docs.microsoft.com/azure/migrate/tutorial-prepare-physical#prepare-azure-for-server-assessment) to create and manage AAD Applications in Azure. You should have the **Application Developer** role or a user role with **User can register applications** allowed at the tenant level.

* **I am unable to complete registration due to errors related to AAD Application operation failure**

    This error is encountered when the Azure user account used to initiate the discovery is different from the account used to register the appliance. Do one of the following:

   * Ensure that the user account initiating the discovery is the same as the account used to register the appliance
   * Provide AAD Application access permissions to the other user account for which the discovery operation is failing
   * Delete the Resource Group previously created for Azure Migrate project and create another Resource Group to start again

* **I am having Key Vault create/update issues during appliance registration**

     Refer to this [document](https://docs.microsoft.com/azure/migrate/troubleshoot-appliance-discovery#error-6003060031-key-vault-management-operation-failed) for different types of Key Vault related errors and their remediation steps.<br><br>

### Issues in adding physical, AWS, or GCP servers

* **I am unable to connect to the physical server due to incorrect credentials or insufficient permissions**

    Verify the credentials provided for the physical server: 

     * **Windows:** Use a domain account for domain-joined machines, and a local account for machines that are not domain-joined. Add the user account to these groups: Remote Management Users, Performance Monitor Users, and Performance Log Users.

     * **Linux:** You need a root account on the Linux servers that you want to discover.

* **I am unable to provide SSH key-based credentials for Linux servers**

   Currently, SSH key-based credentials are not supported as an input on the appliance for Linux servers.


* **I get WinRM errors while validating Windows servers**

    On the server to be discovered, run the `winrm qc` and `Enable-PSRemoting` commands using PowerShell as an administrator. Ensure that WinRM port 5985 (HTTP) is open.


* **I do not want to use a root account to discover Linux servers** 

    Find details on an alternative [here](https://docs.microsoft.com/azure/migrate/migrate-support-matrix-physical#physical-server-requirements).


* **I am unable to connect to an AWS or GCP server at the validation stage in the appliance**

    * Ensure password-based authentication is enabled in Linux servers. 
    * Ensure that port 5985 is open on Windows servers to allow remote WMI calls. 
    * On GCP Linux VMs, ensure root login is enabled.<br><br>

### Issues post discovery initiation

* **I am seeing some performance data missing on servers in the assessment I created**

    Refer to this [document](https://docs.microsoft.com/azure/migrate/troubleshoot-assessment#why-is-performance-data-missing-for-someall-vms-in-my-assessment-report) for different types of performance data missing issues and their remediation steps.
