<properties
pageTitle="The Update Management solution failed to deploy correctly"
description="The Update Management solution failed to deploy correctly"
infoBubbleText="The Update Management solution did not deploy successfully. See details on the right."
service="microsoft.automation"
resource="automationaccounts"
authors="georgewallace"
ms.author="gwallace"
displayOrder=""
articleId="Update_0875B566-AF30-4581-830F-B49426C05164"
diagnosticScenario="AAUpdateSolutionFailedInsights"
selfHelpType="diagnostics"
supportTopicIds="32599861,32599878,32599924,32599864,32599866,32599868,32599870,32599903,32599925,32599936,32599937"
productPesIds="15607"
cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_Automation"
/>

# Update management solution failed to deploy correctly

<!--/issueDescription-->
We have detected that update management solution didn't properly deploy on the following machines:

<!--$computerList-->[computerList]<!--/$computerList-->

Because the machines don't have the update management solution deployed, they are unable to perform scans or patching.
<!--/issueDescription-->

## **Recommended Steps**

* [Re-install the Hybrid Runbook worker[(https://docs.microsoft.com/azure/automation/automation-hybrid-runbook-worker#install-a-hybrid-runbook-worker)] and onboard the VM again
