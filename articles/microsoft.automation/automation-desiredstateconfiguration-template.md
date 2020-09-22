<properties
    pageTitle="Azure Automation - State Configuration (DSC) - Templates"
    description="Azure Automation - State Configuration (DSC)"
    service="microsoft.automation"
    resource="automationaccounts"
    authors="zjalexander"
    ms.author="zachal"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32628000"
    resourceTags=""
    productPesIds="15607"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="8be9ca20-2f4d-4bc7-a480-4236a23104e6"
	ownershipId="Compute_Automation"
/>

# Azure Automation - State Configuration (DSC) - My Template Failed to Deploy
This article will discuss specific deployment failures that can occur with DSC templates.

## **Recommended Steps**

### **Sample ARM template**

* To deploy DSC with ARM templates, see [Onboarding Machines for Management](https://docs.microsoft.com/azure/automation/automation-dsc-onboarding#azure-resource-manager-templates)

### **DSC and VMSS**

* To deploy DSC with VMSS, consult the sample template ["VMSS Configuration managed by Azure Automation"](https://azure.microsoft.com/resources/templates/201-vmss-automation-dsc/)

### **Import-DscResource: Could not find the module**

* You must upload modules included in your DSC configuration to the automation account. See [Adding required DSC resources to Pull Server](https://docs.microsoft.com/azure/automation/automation-dsc-cd-chocolatey#step-3-adding-required-dsc-resources-to-the-pull-server).

## **Recommended Documents**

* [Troubleshoot issues with Automation DSC](https://docs.microsoft.com/azure/automation/troubleshoot/desired-state-configuration)<br>
* [Automation State Configuration (DSC) QuickStart](https://docs.microsoft.com/azure/automation/automation-quickstart-dsc-configuration)<br>
* [Automation DSC Overview](https://docs.microsoft.com/azure/automation/automation-dsc-overview)<br>
* [Getting Started with Automation DSC](https://docs.microsoft.com/azure/automation/automation-dsc-getting-started) <br>
* [Videos on how to setup Automation DSC](https://channel9.msdn.com/Blogs/MVP-Azure/Azure-Automation-DSC-Part-1-Introduction) <br>
* [Onboarding machines to Automation DSC](https://docs.microsoft.com/azure/automation/automation-dsc-onboarding)<br>
* [Configure servers to a desired state](https://docs.microsoft.com/azure/automation/tutorial-configure-servers-desired-state) <br>
* [Compiling Configurations in Automation DSC](https://docs.microsoft.com/azure/automation/automation-dsc-compile) <br>
* [Data to gather when opening a case for Azure Automation](https://docs.microsoft.com/azure/automation/troubleshoot/collect-data-microsoft-azure-automation-case)
