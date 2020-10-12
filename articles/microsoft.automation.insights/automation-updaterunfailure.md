<properties
pageTitle="An update run failed because the update scan failed to complete"
description="The update run failed because the update scan failed to complete due to an error"
infoBubbleText="Update run failed because a scan was unable to complete. See details on the right."
service="microsoft.automation"
resource="automationaccounts"
authors="georgewallace"
ms.author="gwallace"
displayOrder=""
articleId="Update_AE3E2A15-F80C-4034-AA00-08E04F72ACFF"
diagnosticScenario="AAUpdateRunFailedInsights"
selfHelpType="diagnostics"
supportTopicIds="32599861,32599878,32599924,32599864,32599866,32599868,32599870,32599903,32599925,32599936,32599937"
productPesIds="15607"
cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_Automation"
/>

# Microsoft Monitoring Agent needs to be upgraded

<!--/issueDescription-->
We have detected that an update run has failed to query Windows Update for the patches in an update deployment. Without being able to query Windows Update, we can not determine what patches are needed to be installed.
<!--/issueDescription-->

## **Recommended Steps**

* Search for the HRESULT <!--$HRESULTCode-->[HRESULTCode]<!--/$HRESULTCode--> in the [Windows Update error code list](https://support.microsoft.com/help/938205/windows-update-error-code-list) to find the description of the failure. This description provides insight into the possible problem with updates.

## **Recommended Documents**

* [Configure alerts for update deployments](https://docs.microsoft.com/azure/automation/automation-tutorial-update-management#configure-alerts)
