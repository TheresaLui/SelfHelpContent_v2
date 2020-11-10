<properties
pageTitle="Password Expired"
description="Administrator account password expired"
infoBubbleText="Built-in Administrator account password has expired"
service="microsoft.compute"
resource="virtualmachines"
authors="ram-kakani"
displayOrder=""
articleId="vmhealthsignal_e78569b2-cde5-488b-acc4-c79a307c12c9"
diagnosticScenario="Admini password expired"
selfHelpType="diagnostics"
supportTopicIds="32411835"
resourceTags="windows"
productPesIds="14749"
cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>


# Built-in Administrator account password has expired
<!--issueDescription-->
We have investigated and detected that the built-in administrator account password has expired which may prevent RDP connectivity to the VM.
<!--/issueDescription-->

## **Recommended Steps**
Resetting the built-in account password may restore your RDP connectivity to the VM.

* First, ensure that you have the [latest PowerShell module installed and configured](https://docs.microsoft.com/powershell/azure/overview) and are signed in to your Azure subscription with the ```Connect-AzureRmAccount``` cmdlet.
* Now validate the VM has the VM agent in Ready state by executing the below commands via PowerShell.

  ```
  PS C:\WINDOWS\system32> $vm=Get-AzureRmVM -ResourceGroupName MyRG -Name MyVM -Status
  PS C:\WINDOWS\system32> $vm.VMAgent.Statuses

  Code          : ProvisioningState/succeeded
  Level         : Info
  DisplayStatus : Ready
  Message       : GuestAgent is running and accepting new configurations.
  Time          : 7/3/2018 7:44:45 AM
  ```

* Based on the Agent status, you have 2 options:

  * If agent is ready, reset the password via Azure Portal or PowerShell by following the instructions in the article [Reset RDP password](https://docs.microsoft.com/azure/virtual-machines/windows/reset-rdp).
  * In case the agent is not ready, follow the instructions at [Reset local password without Azure Guest agent](https://docs.microsoft.com/azure/virtual-machines/windows/reset-local-password-without-agent)
