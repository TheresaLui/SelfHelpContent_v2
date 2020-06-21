<properties
pageTitle="The Hybrid Runbook Worker needs to be updated"
description="The Hybrid Runbook Worker needs to be updated for update assessments to be functional"
infoBubbleText="Found older versions of the Hybrid Runbook Worker. See details on the right."
service="microsoft.automation"
resource="automationaccounts"
authors="georgewallace"
ms.author="gwallace"
displayOrder=""
articleId="Update_11154F5E-B93A-4F37-9C02-5A6133392FCC"
diagnosticScenario="AAOldHybridInsights"
selfHelpType="diagnostics"
supportTopicIds="32599861,32599878,32599924,32599864,32599866,32599868,32599870,32599903,32599925,32599936,32599937"
productPesIds="15607"
cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_Automation"
/>

# Hybrid Runbook Worker needs to be updated to the latest version
<!--/issueDescription-->
We have detected that you have machines that do not have the latest hybrid runbook worker installed on them. Update Management uses the hybrid runbook worker to perform update assessments and to patch your machines.
<!--/issueDescription-->

Here is a list of machines that need to be updated to the latest hybrid runbook worker:

<!--$computerList-->[computerList]<!--/$computerList-->

## **Recommended Steps**

* [Update your hybrid runbook workers](https://docs.microsoft.com/azure/automation/automation-hybrid-runbook-worker#install-a-hybrid-runbook-worker) on these machines to the latest version: <!--$LatestVersionofAgent-->[LatestVersionofAgent]<!--/$LatestVersionofAgent-->
