<properties
    pageTitle="Resolve Update Management issues with Azure Automation - Scheduling"
    description="Resolve Update Management issues with Azure Automation - Scheduling"
    service="microsoft.automation"
    resource="automationaccounts"
    authors="zjalexander"
    ms.author="zachal"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32642183"
    resourceTags=""
    productPesIds="15607,15725"
    cloudEnvironments="public, Fairfax"
    articleId="850c8d7c-5cb0-4932-b7c8-b30e0b36c099"
	ownershipId="Compute_Automation"
/>

# Resolve Update Management issues with Azure Automation - Creating and Scheduling Update Management Deployments

This article will help with several kinds of issues relating scheduling Azure Update Management deployments.

## **Recommended Steps**

First, try running the Update Agent Troubleshooter ([Windows](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues), [Linux](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues-linux)) which addresses many common issues. 

### **Machines aren't showing up in deployment list**

* Only machines that have reported to Log Analytics in the past 24 hours are shown in the machine list
* Ensure the machine is able to connect to the Update Management service by [running the troubleshooter](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues#start-the-troubleshooter)
* Follow the instructions in ["Machines don't show up in the portal under Update Management"](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#nologs) to ensure the machine is correctly configured 

### **Error when creating deployment**

* Follow the instructions in ["Machines don't show up in the portal under Update Management"](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#nologs) to ensure the machine is correctly configured for the correct workspace
* If you recieve the error **"You have requested to create an update configuration on a machine that is not registered for Update Management"**, you may need to [follow step 2 for images that were cloned](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#resolution-2) 
* Ensure you have the correct permissions to create deployments, especially Contributor access on any Azure VMs you are trying to manage, by referencing the ["Update Management"](https://docs.microsoft.com/azure/automation/automation-role-based-access-control#update-management) section of the Automation RBAC documentation

### **Error editing an existing deployment**

* If you see a grey cloud icon when opening an existing update deployment, [the underlying schedule might have been deleted](https://docs.microsoft.com/azure/automation/manage-update-multi#schedule-an-update-deployment). You will need to recreate the deployment. 

### **"No computers match the Update deployment target specification" error received**

* You may see this error if machines are offline when the deployment occurs. Follow the steps in ["Machines don't show up under Update Management" ](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#nologs).
* Review the steps to creating a dynamic deployment, especially the note about permissions, in ["Use Dynamic Groups"](https://docs.microsoft.com/azure/automation/automation-update-management-groups)

### **"You have requested to create an update configuration on a machine that is not registered for Update Management"**

* This issue is commonly related to Scope Configuration:

  * Option 1) [Update the scope configuration](https://docs.microsoft.com/azure/automation/automation-onboard-solutions-from-automation-account#scope-configuration) to add the desired machines
  * Option 2) (Recommended) [Disable Scope Configuration](https://docs.microsoft.com/azure/automation/automation-onboard-solutions-from-automation-account#all-available-and-future-machines) and register all machines in the workspace for Update Management

### **No saved searches appear**

* Saved searches must be saved as computer groups to appear. See [Computer Groups in Azure Monitor](https://docs.microsoft.com/azure/azure-monitor/platform/computer-groups#log-query)

### **Scheduled deployment doesn't occur**

* Check the "Start time" field on the [schedule settings](https://docs.microsoft.com/azure/automation/manage-update-multi#schedule-an-update-deployment). The schedule doesn't start firing until the start time has passed.
* Check the "Recurrence" field to ensure the schedule is correctly configured. The options are the same as described in the [Azure Automation Schedules](https://docs.microsoft.com/azure/automation/shared-resources/schedules) document.
* Check the "Set Expiration" and "Expires" fields to ensure the schedule has not expired. 

## **Recommended Documents**

* [Troubleshoot issues using Update Management](https://docs.microsoft.com/azure/automation/troubleshoot/update-management)
* [Troubleshoot issues onboarding Update Management](https://docs.microsoft.com/azure/automation/troubleshoot/onboarding)
* [Understand the agent check results in Update Management](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues)
* [Update Management Overview](https://docs.microsoft.com/azure/automation/automation-update-management)
* [Update Management Tutorial](https://docs.microsoft.com/azure/automation/automation-tutorial-update-management)
* [Data to gather when opening a case for Azure Automation](https://support.microsoft.com/kb/3178510)
