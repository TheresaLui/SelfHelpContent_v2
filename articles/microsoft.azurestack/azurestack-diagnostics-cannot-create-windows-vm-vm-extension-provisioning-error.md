<properties
pageTitle="Cannot create a Windows VM VMExtensionProvisioningError"
description="There are issues that prevent creating a virtual machine"
infoBubbleText="See details on the right"
service="microsoft.azurestack"
resource="azurestack"
authors="justinha"
ms.author="justinha"
displayOrder=""
articleId="azurestack-diagnostics-cannot-create-windows-vm-vm-extension-provisioning-error"
diagnosticScenario="Cannot create a Windows VM VMExtensionProvisioningError"
selfHelpType="diagnostics"
supportTopicIds="32663892"
resourceTags="windows"
productPesIds="16226"
cloudEnvironments="public, FairFax, usnat, ussec"
	ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# Cannot create a Windows VM VMExtensionProvisioningError

<!--issueDescription-->

ResultCode: VMExtensionProvisioningError
ErrorDetails: Failed to provision VM extensions for VM 'VM18040257'

<!--/issueDescription-->

## **Recommended Steps**

Remove the VM extensions during VM deployment and add the VM extensions one-by-one to the VM after successful VM deployment. To troubleshooting VM extensions, see [Troubleshooting Azure Windows VM extension failures](https://docs.microsoft.com/azure/virtual-machines/extensions/troubleshoot) or look for specific VM extension troubleshooting guidance such as [Microsoft Monitoring Agent](https://docs.microsoft.com/azure/azure-monitor/platform/vmext-troubleshoot).
