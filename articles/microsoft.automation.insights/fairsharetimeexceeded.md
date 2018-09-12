<properties
pageTitle="Runbook was stopped and evicted because it exceeded the fair share time limit"
description="Runbook was stopped and evicted because it exceeded the fair share time limit"
infoBubbleText="Found a stopped and evicted runbook that exceeded the fair share time limit. See details on the right."
service="microsoft.automation"
resource="runbooks"
authors="stevechi"
displayOrder=""
articleId="fair-share-time-limit-d99142cd-50b0-43af-acec-db23da3f4cbf"
diagnosticScenario="AARunbookFailedInsights"
selfHelpType="diagnostics"
supportTopicIds="32599859,32599860,32599853"
resourceTags="windows"
productPesIds="15607"
cloudEnvironments="public"
/>
# Runbook was stopped and evicted because it exceeded the fair share time limit
## **The runbook, <!--$RunbookName-->[RunbookName]<!--/$RunbookName-->, was stopped and evicted after exceeding the fair share time limit**
We have investigated and identified that your runbook, <!--$RunbookName-->[RunbookName]<!--/$RunbookName-->, was stopped and evicted <!--$FailedJobs-->[FailedJobs]<!--/$FailedJobs--> times in the <!--$TimeRange-->[TimeRange]<!--/$TimeRange--> days prior to case creation. It exceeded the 180-minute [fair share](https://docs.microsoft.com/azure/automation/automation-runbook-execution#fair-share).
### Recommended Steps
In order to avoid runbook failures caused by exceeding the fair share time limit, we recommend one of the following methods to resolve this problem:
#### 1) [Fair share documentation](https://docs.microsoft.com/azure/automation/automation-runbook-execution#fair-share)

- The [documentation](https://docs.microsoft.com/azure/automation/automation-runbook-execution#fair-share) describes using [powershell workflow](https://docs.microsoft.com/azure/automation/automation-powershell-workflow) to checkpoint the runbook. This will allow the runbook to be restarted.
- The [documentation](https://docs.microsoft.com/azure/automation/automation-runbook-execution#fair-share) also describes executing the runbook on a [Hybrid Runbook Worker](https://docs.microsoft.com/azure/automation/automation-hybrid-runbook-worker). Hybrid workers do not impose a time limit on job execution.

#### 2) Optimize the runbook
If the methods described in the [Fair share documentation](https://docs.microsoft.com/azure/automation/automation-runbook-execution#fair-share) are not acceptable you will need to optimize the runbook.

One optimization option is to create child runbooks. If your runbook loops through the same function on a number of resources, such as a database operation on several databases, you can move that function to a [child runbook](https://docs.microsoft.com/azure/automation/automation-child-runbooks). Each of these child runbooks executes in parallel in separate processes decreasing the total amount of time for the parent runbook to complete.

The PowerShell cmdlets that enable this scenario are:

- [Start-AzureRMAutomationRunbook](https://docs.microsoft.com/powershell/module/azurerm.automation/start-azurermautomationrunbook) This cmdlet allows you to start a runbook and pass parameters to the runbook
- [Get-AzureRmAutomationJob](https://docs.microsoft.com/powershell/module/azurerm.automation/Get-AzureRmAutomationJob) This cmdlet allows you to check the job status for each child if there are operations that need to be performed after the child runbook completes.

### Additional references

- [Fair Share documentation](https://docs.microsoft.com/azure/automation/automation-runbook-execution#fair-share)
- [Create a PowerShell workflow runbook](https://docs.microsoft.com/azure/automation/automation-powershell-workflow)
 - [Learning PowerShell Workflow](https://docs.microsoft.com/azure/automation/automation-powershell-workflow)


- [Hybrid Runbook Worker overview](https://docs.microsoft.com/azure/automation/automation-hybrid-runbook-worker)
 - [Deploy Windows Hybrid Runbook Worker](https://docs.microsoft.com/azure/automation/automation-windows-hrw-install)
 - [Deploy Linux Hybrid Runbook Worker](https://docs.microsoft.com/azure/automation/automation-linux-hrw-install)
 - [Run runbooks on a Hybrid  Worker](https://docs.microsoft.com/azure/automation/automation-hrw-run-runbooks)


- [Child runbooks](https://docs.microsoft.com/azure/automation/automation-child-runbooks)
 - [Get-AzureRmAutomationJob](https://docs.microsoft.com/powershell/module/azurerm.automation/Get-AzureRmAutomationJob)
 - [Start-AzureRMAutomationRunbook](https://docs.microsoft.com/powershell/module/azurerm.automation/start-azurermautomationrunbook)


- [Runbook Troubleshooting Guide](https://docs.microsoft.com/azure/automation/troubleshoot/runbooks)
- [Automation Service Limits](https://docs.microsoft.com/azure/azure-subscription-service-limits#automation-limits)
