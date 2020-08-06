<properties
pageTitle="Runbook failure may be because there are a mixture AzureRm and AzureAz cmdlets in the runbook."
description="Runbook failed with symptoms that indicate there is a mixture of AzureRm and AzureAz cmdlets in the runbook."
infoBubbleText="The runbook may have failed because of AzureRm and AzureAz cmdlets in the runbook. See details on the right."
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
cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_Automation"
/>
# The runbook failed because there are a mixture of AzureRm and AzureAz cmdlets in the runbook

<!--issueDescription-->
We have investigated and identified that your runbook, <!--$RunbookName-->[Runbook Name]<!--/$RunbookName-->, failed <!--$FailedJobs-->[Failed Jobs]<!--/$FailedJobs--> times in the <!--$TimeRange-->[Time Range]<!--/$TimeRange--> days prior to support case creation. The most likely cause of the failure is because the runbook is using both Azure  Rm and AzureAz cmdlets.

The most recent failure of <!--$RunbookName-->[Runbook Name]<!--/$RunbookName--> is job Id, <!--$JobId-->[job Id]<!--/$JobId-->. It failed at line <!--$ScriptLineNumber-->[Script Line Number]<!--/$ScriptLineNumber--> in the <!--$Cmdlet-->[cmdlet name]<!--/$Cmdlet--> cmdlet in the PowerShell module, <!--$Module-->[module]<!--/$Module--> <!--$Version-->[version number]<!--/$Version-->  The exception we detected is a <!--$Category-->[category]<!--/$Category--> exception. There are also both AzureRm and AzureAz modules loaded in the sandbox execution environment. This normally indicates that the runbook contains both AzureRm and AzureAz cmdlets.
<!--/issueDescription-->

## **Recommended Steps**

To avoid runbook failures the runbook must either use all AzureAz cmdlets or use all AzureRm cmdlets. Our recommendation is to upgrade all AzureRm cmdlets in the runbook to the equivalent AzureAz cmdlets.

Another issue to consider when upgrading your runbooks to use the AzureAz cmdlets is that failures can occur if correctly written runbooks containing all AzureAz cmdlets and correctly written runbooks containing all AzureRm cmdlets are executed in the same Azure Automation account.

You should either convert all of the runbooks using AzureRm cmdlets to use AzureAz cmdlets in your existing Azure Automation account or create a new Azure Automation account to contain the runbooks that have been converted to use AzureAz cmdlets.
## **Recommended Documents**

- [Az module support in Azure Automation](https://docs.microsoft.com/azure/automation/az-modules)
- [How to update Azure PowerShell modules in Azure Automation](https://docs.microsoft.com/azure/automation/automation-update-azure-modules)
