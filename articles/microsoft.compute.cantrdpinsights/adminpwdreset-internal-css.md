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
cloudEnvironments="public"
/>


# Built-in Administrator account password has expired
<!--issueDescription-->
We have investigated and detected that the built-in administrator account password has expired which may prevent your connectivity to the VM via RDP.
<!--/issueDescription-->

## **Recommended Steps**
You can use either the Azure portal or the Azure PowerShell to reset the administrator account password. Please follow the instructions below:
* Make sure that you have the [latest PowerShell module installed and configured](https://docs.microsoft.com/powershell/azure/overview) and are signed in to your Azure subscription with the ```Connect-AzureRmAccount``` cmdlet.
* Now validate the VM has the VM agent is Ready by executing the below commands via PowerShell.
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
  * In case the agent is ready reset the password via Azure Portal or PowerShell by following the instructions in the article [Reset RDP password](https://docs.microsoft.com/azure/virtual-machines/windows/reset-rdp).
  * In case the agent is not ready, follow the instructions at [Reset local password without Azure Guest agent](https://docs.microsoft.com/azure/virtual-machines/windows/reset-local-password-without-agent)


## **Internal**

Please refer to the [internal article](https://www.csssupportwiki.com/index.php/curated:Azure/Virtual_Machine/Can%E2%80%99t_RDP-SSH/Basic_Workflow/VM_Responding_Bucket/Password_Reset_Bucket)
