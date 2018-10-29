<properties
pageTitle="Runbook failed because it exceeded the open socket limit"
description="Runbook failed because it exceeded the open socket limit"
infoBubbleText="A runbook was found that failed because it exceeded the open socket limit. See details on the right."
service="microsoft.automation"
resource="runbooks"
authors="stevechi,csand-msft"
displayOrder=""
articleId="socket-limit-48a86414-6e14-4785-8beb-33269666cc3f"
diagnosticScenario="AARunbookFailedInsights"
selfHelpType="diagnostics"
supportTopicIds="32599859,32599860,32599853"
resourceTags="windows"
productPesIds="15607"
cloudEnvironments="public"
/>
# Runbook failed because it exceeded the open socket limit
## **The runbook, <!--$RunbookName-->[RunbookName]<!--/$RunbookName-->, failed after exceeding the <!--$SocketLimit-->[SocketLimit]<!--/$SocketLimit--> open socket limit**
We have investigated and identified that your runbook, <!--$RunbookName-->[RunbookName]<!--/$RunbookName-->, failed <!--$FailedJobs-->[FailedJobs]<!--/$FailedJobs--> times in the <!--$TimeRange-->[TimeRange]<!--/$TimeRange--> days prior to case creation. It exceeded the <!--$SocketLimit-->[SocketLimit]<!--/$SocketLimit--> open socket limit.
### Recommended Steps
To avoid runbook failures caused by exceeding the <!--$SocketLimit-->[SocketLimit]<!--/$SocketLimit--> open socket limit, please refer to the following information for methods to solve this problem:

#### 1) Implement the recommendations in the [Socket Limit troubleshooting guide](https://docs.microsoft.com/azure/automation/troubleshoot/runbooks#job-attempted-3-times) including:

- Execute the runbook on a [Hybrid Runbook Worker](https://docs.microsoft.com/azure/automation/automation-hybrid-runbook-worker). Hybrid workers typically have a much larger limit on the number of sockets.

#### 2) Another technique to solve this problem is to:

- Modify the runbook to release socket connections and connection pools as soon as possible. This will keep the number of open sockets to a minimum. [Sysinternals TCPView](https://docs.microsoft.com/sysinternals/downloads/tcpview), to monitor socket usage, is a valuable tool when debugging the PowerShell cmdlets to reduce socket consumption on a local PowerShell IDE.

#### 3) Optimize the runbook
Another option is to optimize the runbook by starting child runbooks from the parent runbook. If your runbook loops through the same function on a number of resources, such as a database operation on several databases, you can move that function to a [child runbook](https://docs.microsoft.com/azure/automation/automation-child-runbooks#starting-a-child-runbook-using-cmdlet). Each of these child runbooks will execute in parallel in separate processes, and thereby decrease the total amount of time for the parent runbook to complete.

The PowerShell cmdlets that enable this scenario are:

- [Start-AzureRMAutomationRunbook](https://docs.microsoft.com/powershell/module/azurerm.automation/start-azurermautomationrunbook) This cmdlet allows you to start a runbook and pass parameters to the runbook
- [Get-AzureRmAutomationJob](https://docs.microsoft.com/powershell/module/azurerm.automation/Get-AzureRmAutomationJob) This cmdlet allows you to check the job status for each child if there are operations that need to be performed after the child runbook completes.

### Additional references

- [Automation Service Limits](https://docs.microsoft.com/azure/azure-subscription-service-limits#automation-limits)
