
<properties
pageTitle="Cannot unlink Automation account"
description="Cannot unlink Automation account"
service="microsoft.operationalinsights"
resource="workspaces"
symptomID=""
infoBubbleText=""
authors="yossiy"
displayorder="80"
selfHelpType="resource"
supportTopicIds="32612438"
resourceTags=""
productPesIds="15725"
cloudEnvironments="Public, Fairfax"
/>
# Cannot unlink Automation account
You need Contributor permission in the Resource Group level to perform this operation.
## **Recommended steps**
To unlink Automation account from Log Analytics workspace you must first remove solutions that have dependency on Automation from the workspace.
These are:
* Update Management
* Change Tracking
* Start/Stop VMs during off-hours

After you remove these solutions from the workspace, you can continue with the unlinking following these steps:
* From Automation account, select *Linked workspace* on the left pane.
* Click *Unlink workspace* on the ribbon, then *OK*. 

> Note: If you use the Update Management solution, you may want to remove some items that are no longer needed after you remove the solution.
Update schedules (will have names that match the names of the update deployments you created).
## **Recommended documents**
* [Unlink workspace](https://docs.microsoft.com/azure/automation/automation-onboard-solutions-from-browse#unlink-workspace)
* [Azure Automation User Documentation](https://docs.microsoft.com/azure/automation/)
* [Remove a Hybrid Worker group](https://docs.microsoft.com/azure/automation/automation-hybrid-runbook-worker#remove-a-hybrid-worker-group)
<br>
* [Forward job status and job streams from Automation to Log Analytics](https://docs.microsoft.com/azure/automation/automation-manage-send-joblogs-log-analytics)