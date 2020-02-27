<properties
    pageTitle="Resolve Update Management issues with Azure Automation - Agent Not Ready"
    description="Resolve Update Management issues with Azure Automation"
    service="microsoft.automation"
    resource="automationaccounts"
    authors="zjalexander"
    ms.author="zachal"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32615229"
    resourceTags=""
    productPesIds="15607,15725"
    cloudEnvironments="public, Fairfax"
    articleId="011a511c-8c9b-4df3-8d11-47d2b477f92e"
/>

# Resolve Update Management issues with Azure Automation - Agent Not Ready

This article will help with the built-in Update Management Troubleshooting

## **Recommended Steps**

### **Update Agent Readiness doesn't show "ready"**

* For Azure VMs: run the troubleshooter from the "troubleshoot" link in the agent health report
* For non-Azure VMs, or if the troubleshooter doesn't work, see the ["Troubleshoot Offline"](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues#troubleshoot-offline) section of the Update Agent troubleshooter guide
* Consult the [Update Agent Troubleshooter document](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues#prerequisite-checks) for any checks that failed in order to remediate issues

### **Machine shows as "not assessed"**

Information can take a few minutes to propagate through Log Analytics, but if machines still show "not assessed", then:

* Follow the steps in ["Machines don't show up under Update Management" ](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#nologs)
* If you see an error code like "Exception from HRESULT 0x...", see the [list of potential errors in the troubleshooting guide](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#hresult)

## **Recommended Documents**

* [Troubleshoot issues using Update Management](https://docs.microsoft.com/azure/automation/troubleshoot/update-management)
* [Troubleshoot issues onboarding Update Management](https://docs.microsoft.com/azure/automation/troubleshoot/onboarding)
* [Understand the agent check results in Update Management](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues)
* [Update Management Overview](https://docs.microsoft.com/azure/automation/automation-update-management)
* [Update Management Tutorial](https://docs.microsoft.com/azure/automation/automation-tutorial-update-management)
* [Data to gather when opening a case for Azure Automation](https://support.microsoft.com/kb/3178510)
