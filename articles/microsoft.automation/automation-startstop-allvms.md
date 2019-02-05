<properties
    pageTitle="Azure Automation - VMs Don't Start/Stop"
    description="Azure Automation - VMs Don't Start/Stop"
    service="microsoft.automation"
    resource="automationaccounts"
    authors="zjalexander"
    ms.author="zachal"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="xxxxxxxx"
    resourceTags=""
    productPesIds="15607"
    cloudEnvironments="public"
/>

# Azure Automation - All VMs fail to start or stop
Here are some common issues which might cause all VMs to start or stop.
If you have an issue where some, but not all, VMs will not start or stop on schedule, please choose "Some VMs fail to start or stop" as your category to see more relevant information. 

## **Recommended Steps**

Specific problems and their solutions are listed below, but we highly recommend you try these two troubleshooting steps first:

* Check the [job streams]( https://docs.microsoft.com/azure/automation/automation-runbook-output-and-messages#message-streams) for the Start/Stop VM Jobs
* Review [schedules associated with Start/StopVM](https://docs.microsoft.com/en-us/azure/automation/automation-solution-vm-management#schedules) 

**COMMON ERROR 1: Probably runas?**
If you have runAs issues, go to [RunAs troubleshooter](https://docs.microsoft.com/en-us/azure/automation/troubleshoot/shared-resources#run-as-accounts)

**COMMON ERROR 2**

## **Recommended Documents** ##

* [Deployment documentation for Start-Stop VM Solution](https://docs.microsoft.com/azure/automation/automation-solution-vm-management#deploy-the-solution)

