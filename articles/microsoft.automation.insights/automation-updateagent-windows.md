<properties
pageTitle="The Microsoft Monitoring Agent needs to be upgraded"
description="The Microsoft Monitoring Agent needs to be upgraded for update assessments to be functional"
infoBubbleText="Found older versions of the Microsoft Monitoring Agent. See details on the right."
service="microsoft.automation"
resource="automationaccounts"
authors="georgewallace"
displayOrder=""
articleId="Update_1FCDCD2C-E096-49C4-8A50-C53020F79757"
diagnosticScenario="AAOldAgentInsights"
selfHelpType="diagnostics"
supportTopicIds="32599861,32599878,32599924,32599864,32599866,32599868,32599870,32599903,32599925,32599936,32599937"
productPesIds="15607"
cloudEnvironments="public"
/>
# Microsoft Monitoring Agent needs to be upgraded

We have detected that you have machines that do not have the latest Windows Microsoft Monitoring Agent installed on them. Update Management uses these agents to perform update assessments and to orchestrate the patching of your systems.

The following is a list of machines missing the latest Windows Microsoft Monitoring Agent:

<!--$computerList-->[computerList]<!--/$computerList-->

It is recommended that you update the agent on your machines to the latest version: <!--$LatestVersionofAgent-->[LatestVersionofAgent]<!--/$LatestVersionofAgent-->.

To update the agent on your machines refer to the steps found at [Install a Hybrid Runbook Worker](https://docs.microsoft.com/azure/automation/automation-hybrid-runbook-worker#install-a-hybrid-runbook-worker).
