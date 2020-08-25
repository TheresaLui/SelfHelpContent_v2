
<properties
pageTitle="Cannot unlink Automation account"
description="Cannot unlink Automation account"
service="microsoft.operationalinsights"
resource="workspaces"
symptomID=""
infoBubbleText=""
authors="yossiy"
displayorder="10"
selfHelpType="Generic"
supportTopicIds="32612438"
resourceTags=""
productPesIds="15725"
cloudEnvironments="Public, Fairfax, usnat, ussec"
	articleId="17ae1c05-dffc-435d-a9e3-5a0b987cd3a5"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# Cannot unlink Automation account
You need Contributor permission in the Resource Group level to perform this operation.
## **Recommended steps**
To unlink an Automation account from a Log Analytics workspace you must first remove all solutions from the workspace that have dependencies on the Automation account, including:<br>
* Update Management
* Change Tracking
* Start/Stop VMs during off-hours<br>

After you remove these solutions from the workspace, you can continue with the unlinking following these steps:<br>
* From Automation account, select *Linked workspace* on the left pane.
* Click *Unlink workspace* on the ribbon, then *OK*. 

## **Recommended documents**<br>
* [Unlink workspace](https://docs.microsoft.com/azure/automation/automation-onboard-solutions-from-browse#unlink-workspace)
* [Azure Automation User Documentation](https://docs.microsoft.com/azure/automation/)
* [Remove a Hybrid Worker group](https://docs.microsoft.com/azure/automation/automation-hybrid-runbook-worker#remove-a-hybrid-worker-group)
* [Forward job status and job streams from Automation to Log Analytics](https://docs.microsoft.com/azure/automation/automation-manage-send-joblogs-log-analytics)