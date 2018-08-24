<properties
pageTitle="The Update Management solution failed to deploy correctly"
description="The Update Management solution failed to deploy correctly"
infoBubbleText="The Update Management solution did not deploy successfully. See details on the right."
service="microsoft.automation"
resource="automationaccounts"
authors="georgewallace"
displayOrder=""
articleId="Update_0875B566-AF30-4581-830F-B49426C05164"
diagnosticScenario="AAUpdateSolutionFailedInsights"
selfHelpType="diagnostics"
supportTopicIds="32599861,32599878,32599924,32599864,32599866,32599868,32599870,32599903,32599925,32599936,32599937"
productPesIds="15607"
cloudEnvironments="public"
/>
# Update Management solution failed to deploy correctly

We have detected that Update Management solution didn't properly deploy on the following machines:

<!--$computerList-->[computerList]<!--/$computerList-->

Because the machines don't have the Update Management solution deployed, they are unable to perform scans or patching.

## Recommended action

To correct this issue, please re-install the Hybrid Runbook worker and onboard the VM again. You can find the instructions on how to install a Hybrid Runbook Worker at - [Install a Hybrid Runbook Worker](https://docs.microsoft.com/azure/automation/automation-hybrid-runbook-worker#install-a-hybrid-runbook-worker)".
