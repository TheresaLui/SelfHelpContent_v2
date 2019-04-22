<properties
	pageTitle="Hyper-V (Preview)/Discovery issues"
	description="Hyper-V (Preview)/Discovery issues"
	service="microsoft.migrate"
	resource="projects"
	authors="shijojoy"
	ms.author="shijoy"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32631931"
	resourceTags=""
	productPesIds="16348"
	cloudEnvironments="public"
	articleId="ecf87d57-c8c4-4009-8d82-f6d50af6c145"
/>

# Hyper-V (Preview)/Discovery issues

## **Recommended Steps**

* **Failover Cluster has a Virtual Machine that is in Failed/Error state, causing periodic Discovery/RefreshFabricLayout to fail. This can happen when the actual VM has been deleted on the Hyper-V Host.**

	Delete or fix the VM that is in Failed/Error state in Failover Cluster should resolve the issue.

* **When Hyper-V Failover Cluster is added to the Host list for Discovery and clicked on Validate button. You may see that a validate operation will fail with the error "WinRM is unable to resolve the server. Check DNS"**

	1. Right-click Notepad and choose Run as administrator
	2. In Notepad, click File --> Open
	3. In the File name field, paste the following path in: `C:\Windows\System32\Drivers\etc\hosts`
	4. Add the IP address and cluster Node Hostname in a row. Repeat for each cluster node.
	5. Save and close hosts file
	6. Try validate again. It should succeed now.

*  **Discovery failed - Error: Azure key vault operation failed. Please retry the operation. If the issue persists, please contact Microsoft support.**

	This issue can occur when there is a failure while trying to acquire token for Azure Key Vault communication. As a workaround, please close the IE browser and launch again after 5 minutes and try “Save and start Discovery” again.
	
*  **Disk size missing for Hyper-V VM**

	If you have disks on SMB storage, enable credSSP authentication on the Azure Migrate appliance. [Learn more](https://azuremigrate.blob.core.windows.net/azuremigratelimitedpreview2019/Limited%20Preview%20User%20Guide%20-%20Hyper-V.pdf) about how you can do this.  
	
*  **Machines showing outdated information on portal**

	1. Please ensure the Azure Migrate appliance is up and running 
	2. After you bring up the appliance, please wait for 45 minutes for the latest information to reflect on the portal 
	
*  **Discovery fails with error: "There was a conflict while creating key and secret for the certificate"**

	A previous discovery operation is still ongoing. Please retry after some time. 
	
*  **Discovery fails with error: "Unable to create resources required for the appliance. The specified service principal is not available for use"**

	This error is due to stale artifacts causing an internal error. Please retry after 24 hours. 
	
*  **Discovery fails with error: "A new key vault certificate can not be created or imported while a pending key vault certificate's status is inProgress."**

	A previous discovery operation is still ongoing. Please retry after some time. 
	
*  **Discovery fails with error: "Active directory operation failed with error. Insufficient privileges to complete the operation."**

	The Azure user you used for onboarding does not have the required permissions to create AAD apps. Please ensure you have the necessary privileges required. [Learn more](https://azuremigrate.blob.core.windows.net/azuremigratelimitedpreview2019/Limited%20Preview%20User%20Guide%20-%20Hyper-V.pdf) 
 
	Refer to [this documentation](https://azuremigrate.blob.core.windows.net/azuremigratelimitedpreview2019/Limited%20Preview%20User%20Guide%20-%20Hyper-V.pdf) for guidance on how roles can be assigned; see the “Set up Azure Migrate: Server Assessment” > “Prerequisites” section.  

*  **Discovery fails with error: The client 'xx' with object id 'xx' does not have authorization to perform action 'Microsoft.Resources/subscriptions/resourcegroups/read'**

	The Azure user you used does not have at least Contributor access on the subscription. Please ensure you have the necessary privileges required. [Learn more](https://azuremigrate.blob.core.windows.net/azuremigratelimitedpreview2019/Limited%20Preview%20User%20Guide%20-%20Hyper-V.pdf)
