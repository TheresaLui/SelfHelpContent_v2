<properties
pageTitle="Warning: Runbooks failed because they exceeded either memory, socket, or time limits"
description="Warning: Runbooks failed because they exceeded either memory, socket, or time limits"
infoBubbleText="Runbooks were found that failed because they exceeded the sandbox limits. See details on the right."
service="microsoft.automation"
resource="runbooks"
authors="stevechi"
ms.author="stevechi"
displayOrder=""
articleId="all-runbook-limit-failures-fc7bf8dd-edc1-4247-b19c-59a4eca98ecf"
diagnosticScenario="AAAllRunbookFailedInsights"
selfHelpType="diagnostics"
supportTopicIds="32635012,2599853,32599860,32599908,32615224"
resourceTags="windows"
productPesIds="15607"
cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_Automation"
/>
# Warning Runbooks failed because they exceeded either memory, socket, or time limits

<!--issueDescription-->
We have investigated and identified that runbooks have failed because they exceeded either the maximum memory, sockets, or time limits allowed in the Azure Automation execution environment during the <!--$TimeRange-->[TimeRange]<!--/$TimeRange--> days prior to case creation.

These <!--$MemoryCount-->[number of runbooks]<!--/$MemoryCount--> runbooks exceeded the <!--$MemoryLimit-->[MemoryLimit]<!--/$MemoryLimit--> Mbyte memory limit.

<!--$MemoryFailures-->[table of memory failure runbooks]<!--/$MemoryFailures-->


<br>These <!--$SocketCount-->[number of runbooks]<!--/$SocketCount--> runbooks exceeded the <!--$SocketLimit-->[SocketLimit]<!--/$SocketLimit--> socket limit.

<!--$SocketFailures-->[table of socket failure runbooks]<!--/$SocketFailures-->

<br>These <!--$TimeLimitCount-->[number of runbooks]<!--/$TimeLimitCount--> runbooks exceeded the <!--$TimeLimit-->[TimeLimit]<!--/$TimeLimit--> minute time limit.

<!--$TimeLimitFailures-->[table of time limit failure runbooks]<!--/$TimeLimitFailures-->

<!--/issueDescription-->

## **Recommended Steps**

#### Memory Limit Failures
To avoid runbook failures caused by exceeding the <!--$MemoryLimit-->[MemoryLimit]<!--/$MemoryLimit--> Mbyte memory limit, please refer to the following information for methods to solve this problem:

1. Implement the recommendations in the [Memory Limit troubleshooting guide](https://docs.microsoft.com/azure/automation/troubleshoot/runbooks#job-attempted-3-times)
2. Execute the runbook on a [Hybrid Runbook Worker](https://docs.microsoft.com/azure/automation/automation-hybrid-runbook-worker). The memory on hybrid workers is limited only by the amount of memory on the machine that is hosting the hybrid worker, and this is typically much larger than the memory limit for Automation sandboxes.
3. Optimize the runbook by starting child runbooks from the parent runbook. If your runbook loops through the same function on a number of resources, such as a database operation on several databases, you can move that function to a [child runbook](https://docs.microsoft.com/azure/automation/automation-child-runbooks#starting-a-child-runbook-using-cmdlet). Each of these child runbooks will execute in parallel in separate processes, and thereby decrease the total amount of time for the parent runbook to complete. The PowerShell cmdlets that enable this scenario are:

  - [Start-AzureRMAutomationRunbook](https://docs.microsoft.com/powershell/module/azurerm.automation/start-azurermautomationrunbook) This cmdlet allows you to start a runbook and pass parameters to the runbook.
  - [Get-AzureRmAutomationJob](https://docs.microsoft.com/powershell/module/azurerm.automation/Get-AzureRmAutomationJob) This cmdlet allows you to check the job status for each child if there are operations that need to be performed after the child runbook completes.

#### Socket Limit failures

To avoid runbook failures caused by exceeding the <!--$SocketLimit-->[SocketLimit]<!--/$SocketLimit--> open socket limit, please refer to the following information for methods to solve this problem:

1. Implement the recommendations in the [Socket Limit troubleshooting guide](https://docs.microsoft.com/azure/automation/troubleshoot/runbooks#job-attempted-3-times) including:

	- Execute the runbook on a [Hybrid Runbook Worker](https://docs.microsoft.com/azure/automation/automation-hybrid-runbook-worker). Hybrid workers typically have a much larger limit on the number of sockets.

2. Modify the runbook to release socket connections and connection pools as soon as possible. This will keep the number of open sockets to a minimum. [Sysinternals TCPView](https://docs.microsoft.com/sysinternals/downloads/tcpview), to monitor socket usage, is a valuable tool when debugging the PowerShell cmdlets to reduce socket consumption on a local PowerShell IDE.

3. Another option is to optimize the runbook by starting child runbooks from the parent runbook. If your runbook loops through the same function on a number of resources, such as a database operation on several databases, you can move that function to a [child runbook](https://docs.microsoft.com/azure/automation/automation-child-runbooks#starting-a-child-runbook-using-cmdlet). Each of these child runbooks will execute in parallel in separate processes, and thereby decrease the total amount of time for the parent runbook to complete. The PowerShell cmdlets that enable this scenario are:

	- [Start-AzureRMAutomationRunbook](https://docs.microsoft.com/powershell/module/azurerm.automation/start-azurermautomationrunbook): This cmdlet allows you to start a runbook and pass parameters to the runbook
	- [Get-AzureRmAutomationJob](https://docs.microsoft.com/powershell/module/azurerm.automation/Get-AzureRmAutomationJob): This cmdlet allows you to check the job status for each child if there are operations that need to be performed after the child runbook completes

#### Time Limit failures

To avoid runbook failures caused by exceeding the fair share time limit, follow these steps: 

1. Implement the recommendations in the [Fair Share documentation](https://docs.microsoft.com/azure/automation/automation-runbook-execution#fair-share)
2. Execute the runbook on a [Hybrid Runbook Worker](https://docs.microsoft.com/azure/automation/automation-hybrid-runbook-worker), which does not impose a limit on job execution time
3. Optimize the runbook by starting child runbooks from the parent runbook. If your runbook loops through the same function on a number of resources, such as a database operation on several databases, you can move that function to a [child runbook](https://docs.microsoft.com/azure/automation/automation-child-runbooks#starting-a-child-runbook-using-cmdlet). Each of these child runbooks will execute in parallel in separate processes, and thereby decrease the total amount of time for the parent runbook to complete. The PowerShell cmdlets that enable this scenario are:

  - [Start-AzureRMAutomationRunbook](https://docs.microsoft.com/powershell/module/azurerm.automation/start-azurermautomationrunbook): This cmdlet allows you to start a runbook and pass parameters to the runbook.  Determine if you need to use the -Wait parameter to wait for the child job to complete and the output of the child runbook to be returned.  If you don't need to wait for the child runbook then don't use the -Wait parameter, and the parent runbook will finish even more quickly
  - [Get-AzureRmAutomationJob](https://docs.microsoft.com/powershell/module/azurerm.automation/Get-AzureRmAutomationJob): If you start child runbooks using the above cmdlet and don't use the -Wait parameter, but you still need to know if the child job has finished and perhaps collect the job output, then you can use this cmdlet to check the job status for each child.

## **Recommended Documents**

- [Automation Service Limits](https://docs.microsoft.com/azure/azure-subscription-service-limits#automation-limits)
