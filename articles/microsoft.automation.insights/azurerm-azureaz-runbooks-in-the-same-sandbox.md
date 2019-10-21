<properties
pageTitle="The runbook failed because AzureRm and AzureAz runbooks were executed in the same sandbox."
description="Runbook failed with symptoms that indicate there are a mixture of AzureRm and AzureAz runbooks that executed in the same sandbox."
infoBubbleText="The runbook may have failed because of AzureRm and AzureAz runbooks were executed in the same Sandbox. See details on the right."
service="microsoft.automation"
resource="runbooks"
ms.author="stevechi"
authors="stevechi"
displayOrder=""
articleId="runbookfailedaz-rm-modules-edcf4092-4d6f-405f-ace6-657e789805bb"
diagnosticScenario="AAAzAndRmModulesInSandbox"
selfHelpType="diagnostics"
supportTopicIds="32635012,32599853,32599860,32599908,32615224"
resourceTags="windows"
productPesIds="15607"
cloudEnvironments="public"
/>
# The runbook failed because AzureRm and AzureAz runbooks were executed in the same sandbox.

<!--issueDescription-->
We have investigated and identified that your runbook, <!--$RunbookName-->[Runbook Name]<!--/$RunbookName-->, failed <!--$FailedJobs-->[Failed Jobs]<!--/$FailedJobs--> times in the <!--$TimeRange-->[Time Range]<!--/$TimeRange--> days prior to support case creation. The most likely cause of the failure is that runbooks containing AzureAz cmdlets and runbooks containing AzureRM cmdlets were executed in the same sandbox execution environment.

The most recent failure of <!--$RunbookName-->[Runbook Name]<!--/$RunbookName--> is job Id, <!--$JobId-->[job Id]<!--/$JobId--> on ...

The jobs that executed in the same sandbox as the most recent failure of <!--$RunbookName-->[Runbook Name]<!--/$RunbookName--> are in the following table.

<!--/issueDescription-->

## **Recommended Steps**

This type of failure can occur if the Azure  account contains both runbooks written to use AzureRm cmdlets and runbooks written to use AzureAz cmdlets. Our recommendation is  to upgrade all of the runbooks in the Azure Automation account to use AzureAz cmdlets. If you are converting your runbooks to use AzureAz cmdlets, the safe practice is to create another Azure Automation account which will contain the upgraded runbooks that are using the AzureAz cmdlets. This will keep one account with all AzureRm runbooks and the other with all AzureAz runbooks.

## **Recommended Documents**

- [Az module support in Azure Automation](https://docs.microsoft.com/azure/automation/az-modules)
- [How to update Azure PowerShell modules in Azure Automation](https://docs.microsoft.com/azure/automation/automation-update-azure-modules)
