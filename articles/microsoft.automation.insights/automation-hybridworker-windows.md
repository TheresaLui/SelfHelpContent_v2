<properties
pageTitle="The Hybrid Worker needs to be upgraded"
description="The Hybrid Worker needs to be upgraded for update assessments to be functional"
infoBubbleText="Found older versions of the Hybrid Worker. See details on the right."
service="microsoft.automation"
resource="automationaccounts"
authors="georgewallace"
displayOrder=""
articleId="Update_11154F5E-B93A-4F37-9C02-5A6133392FCC"
diagnosticScenario="AAOldHybridInsights"
selfHelpType="diagnostics"
supportTopicIds="32599861,32599878,32599924,32599864,32599866,32599868,32599870,32599903,32599925,32599936,32599937"
productPesIds="15607"
cloudEnvironments="public"
/>
# Hybrid Worker needs to be upgraded

We have detected that you have machines that do not have the latest Hybrid Worker installed on them. Update Management uses the Hybrid Worker to perform update assessments and to orchestrate the patching of your systems.

The following is a list of machines missing the latest Hybrid Worker:

<!--$computerList-->[computerList]<!--/$computerList-->

## Recommended action

It is recommended that you update the agent on your machines to the latest version: <!--$LatestVersionofAgent-->[LatestVersionofAgent]<!--/$LatestVersionofAgent-->.

To update the agent on your machines refer to the steps found at [Install a Hybrid Runbook Worker](https://docs.microsoft.com/azure/automation/automation-hybrid-runbook-worker#install-a-hybrid-runbook-worker).
