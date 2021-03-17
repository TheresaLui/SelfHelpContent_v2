<properties
pageTitle="Cannot create a Windows VM"
description="There are issues that prevent creating a virtual machine"
infoBubbleText="See details on the right"
service="microsoft.azurestack"
resource="azurestack"
authors="justinha"
ms.author="justinha"
displayOrder=""
articleId="azurestack-diagnostics-cannot-create-windows-vm"
diagnosticScenario="Cannot create a Windows VM"
selfHelpType="diagnostics"
supportTopicIds="32663892"
resourceTags="windows"
productPesIds="16226"
cloudEnvironments="public, FairFax, usnat, ussec"
ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# Cannot create a Windows virtual machine

## Cannot create a Windows VM FabricVmPlacementErrorNotEnoughCapacity

<!--issueDescription-->

ResultCode: FabricVmPlacementErrorNotEnoughCapacity
ErrorDetails: Failed to create VM 'VM18040135'

<!--/issueDescription-->

Solution: Manage the capacity of your Azure Stack System by [reclaiming capacity](https://docs.microsoft.com/azure-stack/operator/azure-stack-manage-storage-physical-memory-capacity) or [adding scale units](https://docs.microsoft.com/azure-stack/operator/azure-stack-add-scale-node) or [public IP space](https://docs.microsoft.com/azure-stack/operator/azure-stack-add-ips).

## Cannot create a Windows VM OperationNotAllowed/QuotaExceeded

<!--issueDescription-->

ResultCode: OperationNotAllowed/QuotaExceeded
Message: Operation results in exceeding quota limits of Core. Maximum allowed: 1000, Current in use: 1000, Additional requested: 4. 

<!--/issueDescription-->

Solution: Identify the quota that has been exceeded (in this case for example, Compute Cores) and increase the plan associated with the subscription to [include more cores](https://docs.microsoft.com/azure-stack/operator/azure-stack-quota-types). For more information about increasing quota limits, see [Increase standard quota limits](https://docs.microsoft.com/azure/azure-portal/supportability/per-vm-quota-requests).

## Cannot create a Windows VM VMExtensionProvisioningError

<!--issueDescription-->

ResultCode: VMExtensionProvisioningError
ErrorDetails: Failed to provision VM extensions for VM 'VM18040257'

<!--/issueDescription-->

Solution: Remove the VM extensions during VM deployment and add the VM extensions one-by-one to the VM after successful VM deployment. To troubleshooting VM extensions, see [Troubleshooting Azure Windows VM extension failures](https://docs.microsoft.com/azure/virtual-machines/extensions/troubleshoot) or look for specific VM extension troubleshooting guidance such as [Microsoft Monitoring Agent](https://docs.microsoft.com/azure/azure-monitor/platform/vmext-troubleshoot).
