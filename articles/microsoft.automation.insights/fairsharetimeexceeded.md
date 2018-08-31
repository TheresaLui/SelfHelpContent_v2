<properties
pageTitle="Runbook failed because it exceeded the fair share time limit"
description="Runbook failed because it exceeded the fair share time limit"
infoBubbleText="Found a failed runbook due to exceeding the fair share time limit. See details on the right."
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
# Runbook failed because it exceeded the fair share time limit
## **The runbook, <!--$RunbookName-->[RunbookName]<!--/$RunbookName-->, failed after exceeding the fair share time limit**
We have investigated and identified that your runbook, <!--$RunbookName-->[RunbookName]<!--/$RunbookName-->, failed <!--$FailedJobs-->[FailedJobs]<!--/$FailedJobs--> times in the last 5 days. It exceeded the 180-minute [fair share](https://docs.microsoft.com/azure/automation/automation-runbook-execution#fair-share).
### Recommended Steps
In order to avoid runbook failures caused by fair share consumption, we recommend one of the following methods to resolve this problem:
#### 1) Execute the runbook using a Hybrid Worker
For long-running tasks, it is recommended to use a [Hybrid Runbook Worker](https://docs.microsoft.com/azure/automation/automation-hybrid-runbook-worker). Hybrid Runbook Workers are not limited by fair share, and do not have a limitation on how long a runbook can execute.
#### 2) Optimize the runbook
If you would like to execute the runbook in the cloud rather than using a Hybrid Worker, you need to optimize the runbook.

One option is to create child runbooks. If your runbook loops through the same function on a number of resources, such as a database operation on several databases, you can move that function to a [child runbook](https://docs.microsoft.com/azure/automation/automation-child-runbooks). Each of these child runbooks executes in parallel in separate processes decreasing the total amount of time for the parent runbook to complete running.

The PowerShell cmdlets that enable this scenario are:

- [Start-AzureRMAutomationRunbook](https://docs.microsoft.com/powershell/module/azurerm.automation/start-azurermautomationrunbook) This cmdlet allows you to start a runbook and pass parameters to the runbook.
- [Get-AzureRmAutomationJob](https://docs.microsoft.com/powershell/module/azurerm.automation/Get-AzureRmAutomationJob) This cmdlet allows you to check the job status for each child if there are operations that need to be performed after the child runbook completes.

### Additional references

- [Fair Share documentation](https://docs.microsoft.com/azure/automation/automation-runbook-execution#fair-share)
- [Automation Service Limits](https://docs.microsoft.com/azure/azure-subscription-service-limits#automation-limits)
- [Runbook Troubleshooting Guide](https://docs.microsoft.com/azure/automation/troubleshoot/runbooks)
