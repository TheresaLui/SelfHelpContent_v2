<properties
    pageTitle="I could not enable Update Management"
    description="Onboarding an automation account to a solution"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="khughes, zjalexander"
    ms.author="khughes, zachal"
    displayOrder="55"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="windows, linux, windowsSQL, redhat, Ubuntu"
    productPesIds=""
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    articleId="d530b6fe-3096-40c1-9ef0-2bc37364bee5"
	ownershipId="Compute_VirtualMachines"
/>

# I could not enable Update Management

## **Recommended Steps**

**Machine isn't onboarding after waiting 15 minutes**

* Refer to ["Components enabled but not working"](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#components-enabled-not-working)

**Machine shows as "not assessed"**

Information can take a few minutes to propagate through Log Analytics, but if machines still show "not assessed":

* Check for a [Log Analytics heartbeat](https://docs.microsoft.com/azure/automation/automation-update-management#confirm-that-non-azure-machines-are-onboarded)
* If there is no heartbeat, check the [Solution Scoping](https://docs.microsoft.com/azure/automation/automation-onboard-solutions-from-automation-account#scope-configuration) is correct
* If there is a heartbeat, follow the steps in [Data not Showing in Log Analytics](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#nologs)

## **Recommended Documents**

* [Troubleshooting solution onboarding issues](https://aka.ms/troubleshootsolutiononboarding)
* [Troubleshoot issues onboarding Update Management](https://docs.microsoft.com/azure/automation/troubleshoot/onboarding)
* [Understand the agent check results in Update Management](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues)
* [Update Management Overview](https://docs.microsoft.com/azure/automation/automation-update-management)
* [Update Management Tutorial](https://docs.microsoft.com/azure/automation/automation-tutorial-update-management)
