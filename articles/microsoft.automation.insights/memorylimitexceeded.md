<properties
pageTitle="Runbook was suspended because it exceeded the memory limit"
description="Runbook was suspended because it exceeded the memory limit"
infoBubbleText="Found a suspended runbook that exceeded the memory limit. See details on the right."
service="microsoft.automation"
resource="runbooks"
authors="stevechi"
displayOrder=""
articleId="memory-limit-48a86414-6e14-4785-8beb-33269666cc3f"
diagnosticScenario="AARunbookFailedInsights"
selfHelpType="diagnostics"
supportTopicIds="32599859,32599860,32599853"
resourceTags="windows"
productPesIds="15607"
cloudEnvironments="public"
/>
# Runbook was suspended because it exceeded the memory limit
## **The runbook, <!--$RunbookName-->[RunbookName]<!--/$RunbookName-->, was suspended after exceeding the <!--$MemoryLimit-->[MemoryLimit]<!--/$MemoryLimit--> Mbyte memory limit**
We have investigated and identified that your runbook, <!--$RunbookName-->[RunbookName]<!--/$RunbookName-->, was suspended <!--$FailedJobs-->[FailedJobs]<!--/$FailedJobs--> times in the <!--$TimeRange-->[TimeRange]<!--/$TimeRange--> days prior to case creation. It exceeded the <!--$MemoryLimit-->[MemoryLimit]<!--/$MemoryLimit--> Mbyte memory limit.
### Recommended Steps
In order to avoid runbook failures caused by exceeding the <!--$MemoryLimit-->[MemoryLimit]<!--/$MemoryLimit--> Mbyte memory limit, we recommend one of the following methods to resolve this problem:
#### 1) Look at the [memory limit troubleshooting guide](https://docs.microsoft.com/azure/automation/troubleshoot/runbooks#job-attempted-3-times)

- You may also executes the runbook on a [Hybrid Runbook Worker](https://docs.microsoft.com/azure/automation/automation-hybrid-runbook-worker). Hybrid workers do not impose memory limits on job execution.

#### 2) Optimize the runbook
If the methods described in the [memory limit troubleshooting guide](https://docs.microsoft.com/azure/automation/troubleshoot/runbooks#job-attempted-3-times) are not acceptable you will need to optimize the runbook.

One optimization option is to create child runbooks. If your runbook loops through the same function on a number of resources, such as a database operation on several databases, you can move that function to a [child runbook](https://docs.microsoft.com/azure/automation/automation-child-runbooks). Each of these child runbooks executes in parallel in separate processes decreasing the total amount of time for the parent runbook to complete.

The PowerShell cmdlets that enable this scenario are:

- [Start-AzureRMAutomationRunbook](https://docs.microsoft.com/powershell/module/azurerm.automation/start-azurermautomationrunbook) This cmdlet allows you to start a runbook and pass parameters to the runbook
- [Get-AzureRmAutomationJob](https://docs.microsoft.com/powershell/module/azurerm.automation/Get-AzureRmAutomationJob) This cmdlet allows you to check the job status for each child if there are operations that need to be performed after the child runbook completes.

### Additional references

- [Memory limit troubleshooting guide](https://docs.microsoft.com/azure/automation/troubleshoot/runbooks#job-attempted-3-times)
- [Hybrid Runbook Worker overview](https://docs.microsoft.com/azure/automation/automation-hybrid-runbook-worker)

 - [Deploy Windows Hybrid Runbook Worker](https://docs.microsoft.com/azure/automation/automation-windows-hrw-install)
 - [Deploy Linux Hybrid Runbook Worker](https://docs.microsoft.com/azure/automation/automation-linux-hrw-install)
 - [Run runbooks on a Hybrid  Worker](https://docs.microsoft.com/azure/automation/automation-hrw-run-runbooks)


- [Child runbooks](https://docs.microsoft.com/azure/automation/automation-child-runbooks)

 - [Get-AzureRmAutomationJob](https://docs.microsoft.com/powershell/module/azurerm.automation/Get-AzureRmAutomationJob)
 - [Start-AzureRMAutomationRunbook](https://docs.microsoft.com/powershell/module/azurerm.automation/start-azurermautomationrunbook)


- [Runbook Troubleshooting Guide](https://docs.microsoft.com/azure/automation/troubleshoot/runbooks)
- [Automation Service Limits](https://docs.microsoft.com/azure/azure-subscription-service-limits#automation-limits)
