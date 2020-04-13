<properties
	pageTitle="Operating system provisioning timeout failure"
	description="Operating system provisioning timeout failure"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	ms.author="scotro"
	displayOrder=""
	articleId="DeploymentFailure_rca-ProvisioningFailure-GuestOS-Linux"
	diagnosticScenario="DeploymentFailure"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags="linux"
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines"
/>

# Operating System Provisioning Timeout Failure

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed to deploy because the provisioning of the operating system (guest OS) timed out. 

Indications show that the VM agent failed to send status back to the Compute Resource Provider (CRP). The virtual machine's operating system (guest OS) may have had issues when the VM was created from an image.<br> 

<!--/issueDescription-->
In addition to trying again, you have the following options:

- Create a new VM with the attach option using this VM as a specialized VHD.
- Generalize the VM for use as an image to create new VMs.<br>

### Create a new VM with an attached VHD

You can the use VM as a specialized data VHD to create a new VM. For more information, see [Create a Windows VM from a specialized disk by using PowerShell](https://azure.microsoft.com/documentation/articles/virtual-machines-windows-create-vm-specialized/).<br>

### Generalize the VM for use as an image

Perform the following steps to deploy a VM based on the image of the original VM:

1. Deprovision the VM by running this bash command: `sudo waagent -deprovision+user`
1. Create the VM image
1. Create a VM from the image

For more information, see [How to create an image of a virtual machine or VHD](https://docs.microsoft.com/azure/virtual-machines/linux/capture-image).<br>

## Troubleshooting

Use the following information sources to troubleshoot provisioning errors:

### Timeouts

You can use the [Azure Resource Explorer](https://azure.microsoft.com/blog/azure-resource-explorer-a-new-tool-to-discover-the-azure-api/) to easily view JSON responses from API requests on your Azure resources, such as to see the timeout messages. This tool provides an interactive way to make API calls directly in your own subscriptions.<br>

In the hierarchy in the left panel, navigate to the instance view of your virtual machine: **subscriptions** > *your subscription* > **resourceGroups** > *your resource group* > **providers** > **Microsoft.Compute** > **virtualMachines** > *your vm name* > **instanceView**.<br>  

Review the results for failed statues such as the following:

```json
"statuses": [ 
                { 
                    "code": "ProvisioningState/failed/OSProvisioningTimedOut", 
                    "level": "Error", 
                    "displayStatus": "Provisioning failed", 
                    "message": "OS provisioning failure has reached terminal state and is non-recoverable for VM '<vmname>'. Consider deleting and recreating this virtual machine. Additional Details: {\r\n  \"resourceType\": \"Microsoft.WindowsAzure.ComputeResourceProvider.Core.Shared.Strings, CRP.Core.Shared, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\",\r\n  \"ResourceCode\": \"OSProvisioningTimedOut\",\r\n  \"ResourceParameters\": [\r\n    \"MSAZULP083\"\r\n  ]\r\n}\nInternal detail: RoleInstanceContainerProvisioningDetails: MediaStorageAccountName:ProvisionVmWithUpdate; MediaStorageHostName:ProvisionVmWithUpdate; MediaRelativeUrl:ProvisionVmWithUpdate; MediaTenantSecretId:00000000-0000-0000-0000-000000000000; ProvisioningResult:Timeout; ProvisioningResultMessage:; CertificateThumbprint:; RequestCreatedDateTime:1/1/0001 12:00:00 AM; LastUpdatedDateTime:1/1/0001 12:00:00 AM; RequestIncarnation:096b12dd-8f11-4525-ab1d-33dd5bd8c94b", 
                    "time": "2018-07-12T13:28:51.3727577+00:00" 
                }, 
                { 
                    "code": "PowerState/running", 
                    "level": "Info", 
                    "displayStatus": "VM running" 
                } 
            ] 

```

### VM Agent properties

You can check the agent, also known as the guest agent, status and its version under **Properties** on the VM blade in the Azure Portal. If the agent status is not **Ready** or **Success**, determine the following:<br>

- Is the agent installed?
- Is the agent able to send or receive heart beats from the fabric?
- Is there any other error or warning related to the agent or OS?<br>

To check the status, start, and restart the agent, you can perform the following bash commands:<br>

Azure Linux agent: `service walinuxagent restart`
Centos, Oracle, SuSE: `service waagent status|stop|start|restart`
Ubuntu: `service walinuxagent status|stop|start|restart` 
CoreOS: `systemctl status|stop|start|restart waagent` <br>

Also review the following logs:

/var/lib/waagent/*.xml
/var/log/waagent.log
/var/log/azure/*
Linux OS Version (cat /etc/*-release) output.<br>

You can extract log information through queries in the Azure Portal. See [Get started with Azure Monitor Log Analytics](https://docs.microsoft.com/azure/azure-monitor/log-query/get-started-portal).<br> 

### Extensions

Also check the status on the extensions on your VM in **Extensions** under **Settings** on the VM blade in the Azure Portal.<br> 

### Log analytics

You can extract log information through queries in the Azure Portal. See [Get started with Azure Monitor Log Analytics](https://docs.microsoft.com/azure/azure-monitor/log-query/get-started-portal).<br>
