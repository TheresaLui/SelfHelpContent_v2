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

### **Failover Cluster has a Virtual Machine that is in Failed/Error state, causing periodic Discovery/RefreshFabricLayout to fail. This can happen when the actual VM has been deleted on the Hyper-V Host.**
Fix: Delete or fix the VM that is in Failed/Error state in Failover Cluster should resolve the issue.

### **When Hyper-V Failover Cluster is added to the Host list for Discovery and clicked on Validate button. You may see that a validate operation will fail with the error "WinRM is unable to resolve the server. Check DNS"**
Right-click Notepad and choose Run as administrator. In Notepad, click File then Open… In the File name field, paste the following path in: C:\Windows\System32\Drivers\etc\hosts.
Add the IP address and cluster Node Hostname in a row. Repeat for each cluster node.
Save and close hosts file.
Try validate again. It should succeed now.

### **Discovery failed - Error: Azure key vault operation failed. Please retry the operation. If the issue persists, please contact Microsoft support.**
Workaround: 
This issue can occur when there is a failure while trying to acquire token for Azure Key Vault communication. As a workaround, please close the IE browser and launch again after 5 minutes and try “Save and start Discovery” again.
