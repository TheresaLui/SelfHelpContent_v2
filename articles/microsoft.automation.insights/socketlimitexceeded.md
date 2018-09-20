<properties
pageTitle="Runbook was suspended because it exceeded the open socket limit"
description="Runbook was suspended because it exceeded the open socket limit"
infoBubbleText="Found a suspended runbook that exceeded the open socket limit. See details on the right."
service="microsoft.automation"
resource="runbooks"
authors="stevechi"
displayOrder=""
articleId="socket-limit-48a86414-6e14-4785-8beb-33269666cc3f"
diagnosticScenario="AARunbookFailedInsights"
selfHelpType="diagnostics"
supportTopicIds="32599859,32599860,32599853"
resourceTags="windows"
productPesIds="15607"
cloudEnvironments="public"
/>
# Runbook was suspended because it exceeded the open socket limit
## **The runbook, <!--$RunbookName-->[RunbookName]<!--/$RunbookName-->, was suspended after exceeding the <!--$SocketLimit-->[SocketLimit]<!--/$SocketLimit--> open socket limit**
We have investigated and identified that your runbook, <!--$RunbookName-->[RunbookName]<!--/$RunbookName-->, was suspended <!--$FailedJobs-->[FailedJobs]<!--/$FailedJobs--> times in the <!--$TimeRange-->[TimeRange]<!--/$TimeRange--> days prior to case creation. It exceeded the <!--$SocketLimit-->[SocketLimit]<!--/$SocketLimit--> open socket limit.
### Recommended Steps
To avoid runbook failures caused by exceeding the <!--$SocketLimit-->[SocketLimit]<!--/$SocketLimit--> open socket limit, we recommend one of the following methods to resolve this problem:
#### 1) Look at the [Socket limit troubleshooting guide](https://docs.microsoft.com/azure/automation/troubleshoot/runbooks#job-attempted-3-times)

- Modify the runbook to release socket connections, and socket pools as soon as possible. This will keep the number of open sockets at any time to a minimum. The [Sysinternals TCPView to monitor socket usage](https://docs.microsoft.com/sysinternals/downloads/tcpview) is a valuable tool to monitor socket usage when executing the PowerShell cmdlets in a local PowerShell IDE.
- You can also execute the runbook on a [Hybrid Runbook Worker](https://docs.microsoft.com/azure/automation/automation-hybrid-runbook-worker). Hybrid Runbook Workers do not impose socket limits on job execution.

#### 2) Optimize the runbook
If the methods described in the [socket limit troubleshooting guide](https://docs.microsoft.com/azure/automation/troubleshoot/runbooks#job-attempted-3-times) do not help, you'll need to optimize the runbook.

One optimization option is to create child runbooks. If your runbook loops through the same function on a number of resources, such as a database operation on several databases, you can move that function to a [child runbook](https://docs.microsoft.com/azure/automation/automation-child-runbooks). Each of these child runbooks executes in parallel in separate processes decreasing the total number of sockets necessary for each runbook.

The PowerShell cmdlets that enable this scenario are:

- [Start-AzureRMAutomationRunbook](https://docs.microsoft.com/powershell/module/azurerm.automation/start-azurermautomationrunbook) This cmdlet allows you to start a runbook and pass parameters to the runbook
- [Get-AzureRmAutomationJob](https://docs.microsoft.com/powershell/module/azurerm.automation/Get-AzureRmAutomationJob) This cmdlet allows you to check the job status for each child if there are operations that need to be performed after the child runbook completes.

### Additional references

- [Socket limit troubleshooting guide](https://docs.microsoft.com/azure/automation/troubleshoot/runbooks#job-attempted-3-times)
- [Hybrid Runbook Worker overview](https://docs.microsoft.com/azure/automation/automation-hybrid-runbook-worker)
- [Deploy Windows Hybrid Runbook Worker](https://docs.microsoft.com/azure/automation/automation-windows-hrw-install)
- [Deploy Linux Hybrid Runbook Worker](https://docs.microsoft.com/azure/automation/automation-linux-hrw-install)
- [Run runbooks on a Hybrid  Worker](https://docs.microsoft.com/azure/automation/automation-hrw-run-runbooks)
- [Child runbooks](https://docs.microsoft.com/azure/automation/automation-child-runbooks)
- [Get-AzureRmAutomationJob](https://docs.microsoft.com/powershell/module/azurerm.automation/Get-AzureRmAutomationJob)
- [Start-AzureRMAutomationRunbook](https://docs.microsoft.com/powershell/module/azurerm.automation/start-azurermautomationrunbook)
- [Runbook Troubleshooting Guide](https://docs.microsoft.com/azure/automation/troubleshoot/runbooks)
- [Automation Service Limits](https://docs.microsoft.com/azure/azure-subscription-service-limits#automation-limits)
- [Sysinternals TCPView to monitor socket usage](https://docs.microsoft.com/sysinternals/downloads/tcpview)
