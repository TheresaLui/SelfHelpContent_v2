<properties
pageTitle="Runbook was stopped because it exceeded the memory limit"
description="Runbook was stopped because it exceeded the memory limit"
infoBubbleText="A stopped runbook was found that exceeded the memory limit. See details on the right."
service="microsoft.automation"
resource="runbooks"
authors="stevechi,csand-msft"
displayOrder=""
articleId="memory-limit-48a86414-6e14-4785-8beb-33269666cc3f"
diagnosticScenario="AARunbookFailedInsights"
selfHelpType="diagnostics"
supportTopicIds="32599859,32599860,32599853"
resourceTags="windows"
productPesIds="15607"
cloudEnvironments="public"
/>
# Runbook was stopped because it exceeded the memory limit
## **The runbook, <!--$RunbookName-->[RunbookName]<!--/$RunbookName-->, was stopped after exceeding the <!--$MemoryLimit-->[MemoryLimit]<!--/$MemoryLimit--> Mbyte memory limit**
We have investigated and identified that your runbook, <!--$RunbookName-->[RunbookName]<!--/$RunbookName-->, was stopped <!--$FailedJobs-->[FailedJobs]<!--/$FailedJobs--> times in the <!--$TimeRange-->[TimeRange]<!--/$TimeRange--> days prior to case creation. It exceeded the <!--$MemoryLimit-->[MemoryLimit]<!--/$MemoryLimit--> Mbyte memory limit.
### Recommended Steps
To avoid runbook failures caused by exceeding the <!--$MemoryLimit-->[MemoryLimit]<!--/$MemoryLimit--> Mbyte memory limit, please refer to the following information for methods to solve this problem:
#### 1) Implement the recommendations in the [Memory Limit troubleshooting guide](https://docs.microsoft.com/azure/automation/troubleshoot/runbooks#job-attempted-3-times) including:

- Execute the runbook on a [Hybrid Runbook Worker](https://docs.microsoft.com/azure/automation/automation-hybrid-runbook-worker). The memory on hybrid workers is limited only by the amount of memory on the machine that is hosting the hybrid worker, and this is typically much larger than the memory limit for Automation sandboxes.

#### 2) Optimize the runbook
Another option is to optimize the runbook.

One optimization option is to create child runbooks. If your runbook loops through the same function on a number of resources, such as a database operation on several databases, you can move that function to a [child runbook](https://docs.microsoft.com/azure/automation/automation-child-runbooks). Each of these child runbooks executes in parallel in separate processes decreasing the total amount of memory necessary for each runbook.

The PowerShell cmdlets that enable this scenario are:

- [Start-AzureRMAutomationRunbook](https://docs.microsoft.com/powershell/module/azurerm.automation/start-azurermautomationrunbook) This cmdlet allows you to start a runbook and pass parameters to the runbook.
- [Get-AzureRmAutomationJob](https://docs.microsoft.com/powershell/module/azurerm.automation/Get-AzureRmAutomationJob) This cmdlet allows you to check the job status for each child if there are operations that need to be performed after the child runbook completes.

### Additional references

- [Automation Service Limits](https://docs.microsoft.com/azure/azure-subscription-service-limits#automation-limits)
