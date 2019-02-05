<properties
    pageTitle="Azure Automation - Some VMs Don't Start/Stop"
    description="Azure Automation - Some VMs Don't Start/Stop"
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

# Azure Automation - Some VMs fail to start or stop
Here are some common issues which might cause some, but not all, VMs to start or stop on schedule. 

## **Recommended Steps**






**Review excluded VMs**
You can control what VMs are started/stopped by the solution by configuring the following Automation Account variables:
* External_Start_ResourceGroupNames
* External_Stop_ResourceGroupNames
* External_ExcludeVMNames
Review the "External_ExcludeVMNames" to ensure the VMs with the undesired behavior are not listed.
Further information can be found in the [Start/Stop VMs on a Schedule document](https://docs.microsoft.com/en-us/azure/automation/automation-solution-vm-management#scenario-1-startstop-vms-on-a-schedule)

**Review VM Permissions**
???


**Reasons a VM otherwise might not start/stop** 
Virtual machines might not start/stop as expected indepdently of the start/stop solution.
Review the [Virtual Machine troubleshooter](https://docs.microsoft.com/en-us/azure/virtual-machines/troubleshooting/boot-error-troubleshoot) to ensure there are not external causes for your VMs to stop working

**Review sequential VMs**
It is possible to configure the Start/Stop VM Solution to go through VMs in sequence. 
If your VMs are missing specific tags, they will not be start/stopped.
* Review the **VMList** automation account variable to make sure it is correctly configured
* Review the VMs which are not starting/stopping for the correct "**sequencestart**"/"**sequencestop**" tags. 
* Review the [Start-Stop VMs in Sequence document](https://docs.microsoft.com/en-us/azure/automation/automation-solution-vm-management#scenario-2-startstop-vms-in-sequence-by-using-tags) 

## **Recommended Documents** ##

* [Deployment documentation for Start-Stop VM Solution](https://docs.microsoft.com/azure/automation/automation-solution-vm-management#deploy-the-solution)

