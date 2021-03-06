<properties
  pagetitle="Resolve Update Management issues with Azure Automation - Creating and Scheduling Update Management Deployments&#xD;"
  description="Resolve Update Management issues with Azure Automation - Scheduling"
  service="microsoft.automation"
  resource="automationaccounts"
  ms.author="zachal,riyadav"
  selfhelptype="Generic"
  supporttopicids="32642183"
  resourcetags=""
  productpesids="15607,15725"
  cloudenvironments="public,fairfax,usnat,ussec,blackforest,mooncake"
  articleid="850c8d7c-5cb0-4932-b7c8-b30e0b36c099"
  ownershipid="Compute_Automation" />
# Resolve Update Management issues with Azure Automation - Creating and Scheduling Update Management Deployments

Most users can resolve issues related to scheduling Azure Update Management deployments by using the following information.

## **Recommended Steps**

First, try running the Update Agent Troubleshooter for ([Windows](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues) and for [Linux](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues-linux) on any machines which are not running update deployments. This will uncover configuration issues and ensure that the systems are healthy. 


### **Machines aren't showing up in deployment list**

* Only machines that have reported to Log Analytics in the past 24 hours appear in the machine list
* Ensure that the machine is able to connect to the Update Management service by [running the troubleshooter](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues#start-the-troubleshooter)
* Follow the instructions in ["Machines don't show up in the portal under Update Management"](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#nologs) to ensure the machine is correctly configured 
* Follow the instructions in ["Machines don't appear in preview"](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#machines-not-in-preview) to ensure that you have access on selected scopes, and that the ARG query retrieves the expected machines 

### **Error when creating deployment**

* Ensure that you have the correct permissions to create deployments, especially Contributor access on any Azure VMs you are trying to manage, by reviewing the ["Update Management"](https://docs.microsoft.com/azure/automation/automation-role-based-access-control#update-management) section of the Automation RBAC documentation
* If you receive the error message **"You have requested to create an update configuration on a machine that is not registered for Update Management"**, follow the steps in ["Machines don't show up"](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#nologs) to ensure scope configuration is correct and machines are reporting to Log Analytics properly.
* If you receive an error message like **"The client has permission to perform action [...]], however the current tenant is not authorized to access linked subscription .."**, you need to schedule the update as defined in the [linked subscription troubleshooting guide](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#multi-tenant)
* If you receive an error message like **"No computers match the Update deployment target specification"**, the machines are not reporting to the workspace presently. You can work around this by using [dynamic groups](https://docs.microsoft.com/azure/automation/update-management/update-mgmt-groups). 

### **Error editing an existing deployment**

* If you see a gray cloud icon when opening an existing update deployment, the underlying [schedule](https://docs.microsoft.com/azure/automation/update-management/deploy-updates#schedule-an-update-deployment) might have been deleted. You will need to re-create the deployment. 

### **No saved searches appear**

* Saved searches must be saved as computer groups to appear. See [Computer Groups in Azure Monitor](https://docs.microsoft.com/azure/azure-monitor/platform/computer-groups#log-query)

### **Scheduled deployment doesn't occur**

* Check the **Start time** field on the [schedule settings](https://docs.microsoft.com/azure/automation/update-management/deploy-updates#schedule-an-update-deployment). The schedule doesn't start firing until the start time has passed.
* Check the **Recurrence** field to ensure the schedule is correctly configured. The options are the same as described in the [Azure Automation Schedules](https://docs.microsoft.com/azure/automation/shared-resources/schedules) document.
* Check the **Set Expiration** and **Expires** fields to ensure the schedule has not expired. 

## **Recommended Documents**

* [Troubleshoot issues using Update Management](https://docs.microsoft.com/azure/automation/troubleshoot/update-management)
* [Update Management Overview - Supported Clients, Permissions and Network Requirements](https://docs.microsoft.com/azure/automation/update-management/update-mgmt-overview)
* [Configure Windows Update Client Settings for Update Management](https://docs.microsoft.com/azure/automation/update-management/update-mgmt-configure-wuagent)
* [Manage Schedules in Azure Automation](https://docs.microsoft.com/azure/automation/shared-resources/schedules)
