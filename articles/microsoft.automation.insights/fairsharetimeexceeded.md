<properties
pageTitle="Runbook was stopped because it exceeded the fair share time limit"
description="Runbook was stopped because it exceeded the fair share time limit"
infoBubbleText="A stopped runbook was found that exceeded the fair share time limit. See details on the right."
service="microsoft.automation"
resource="runbooks"
authors="stevechi,csand-msft"
displayOrder=""
articleId="fair-share-time-limit-d99142cd-50b0-43af-acec-db23da3f4cbf"
diagnosticScenario="AARunbookFailedInsights"
selfHelpType="diagnostics"
supportTopicIds="32599859,32599860,32599853"
resourceTags="windows"
productPesIds="15607"
cloudEnvironments="public"
/>
# Runbook was stopped because it exceeded the fair share time limit
## **The runbook, <!--$RunbookName-->[RunbookName]<!--/$RunbookName-->, was stopped after exceeding the fair share time limit**
We have investigated and identified that your runbook, <!--$RunbookName-->[RunbookName]<!--/$RunbookName-->, was stopped <!--$FailedJobs-->[FailedJobs]<!--/$FailedJobs--> times in the <!--$TimeRange-->[TimeRange]<!--/$TimeRange--> days prior to case creation. It exceeded the <!--$TimeLimit-->[TimeLimit]<!--/$TimeLimit--> minute [fair share](https://docs.microsoft.com/azure/automation/automation-runbook-execution#fair-share) time limit.
### Recommended Steps
To avoid runbook failures caused by exceeding the fair share time limit, follow these steps: 

#### 1) Implement the recommendations in the [Fair Share documentation](https://docs.microsoft.com/azure/automation/automation-runbook-execution#fair-share) including: 

- Execute the runbook on a [Hybrid Runbook Worker](https://docs.microsoft.com/azure/automation/automation-hybrid-runbook-worker). Hybrid workers do not impose a job limit on job execution time.
- Use a [Powershell Workflow runbook](https://docs.microsoft.com/azure/automation/automation-first-runbook-textual) to checkpoint the runbook. This allows the runbook to be restarted from the checkpoint and not the beginning of the runbook.


#### 2) Optimize the runbook
Another option is to optimize the runbook.

One optimization is to start child runbooks from the parent runbook. If your runbook loops through the same function on a number of resources, such as a database operation on several databases, you can move that function to a [child runbook](https://docs.microsoft.com/azure/automation/automation-child-runbooks#starting-a-child-runbook-using-cmdlet). Each of these child runbooks will execute in parallel in separate processes, thereby decreasing the total amount of time for the parent runbook to complete.

The PowerShell cmdlets that enable this scenario are:

- [Start-AzureRMAutomationRunbook](https://docs.microsoft.com/powershell/module/azurerm.automation/start-azurermautomationrunbook): This cmdlet allows you to start a runbook and pass parameters to the runbook.  Determine if you need to use the -Wait parameter to wait for the child job to complete and the output of the child runbook to be returned.  If you don't need to wait for the child runbook then don't use the -Wait parameter, and the parent runbook will finish even more quickly
- [Get-AzureRmAutomationJob](https://docs.microsoft.com/powershell/module/azurerm.automation/Get-AzureRmAutomationJob): If you start child runbooks using the above cmdlet and don't use the -Wait parameter, but you still need to know if the child job has finished and perhaps collect the job output, then you can use this cmdlet to check the job status for each child.

### Additional references

- [Automation Service Limits](https://docs.microsoft.com/azure/azure-subscription-service-limits#automation-limits)
