<properties
    pageTitle="Azure Automation - State Configuration (DSC) - Compilation"
    description="Azure Automation - State Configuration (DSC)"
    service="microsoft.automation"
    resource="automationaccounts"
    authors="zjalexander"
    ms.author="zachal"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32628001"
    resourceTags=""
    productPesIds="15607"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="2d29a6eb-da07-4c39-a026-5ad589bb53fb"
	ownershipId="Compute_Automation"
/>

# Azure Automation - State Configuration (DSC) - Problem Compiling a Configuration

## **Recommended Steps**

1. [Compile the configuration locally ](https://docs.microsoft.com/powershell/scripting/dsc/configurations/configurations?view=powershell-5.1#compiling-the-configuration) to understand if the issue is with the configuration itself or with how it is used in Azure Automation
2. [Collect diagnostic logs](https://docs.microsoft.com/azure/automation/troubleshoot/desired-state-configuration#steps-to-troubleshoot-desired-state-configuration-dsc)

### **Possible Issues:**

### **Import-DSC Resource needs to be on new line**

* If importing multiple DSC resources, [list each Import-DscResource statement on a new line](https://docs.microsoft.com/powershell/scripting/dsc/configurations/import-dscresource?view=powershell-5.1)

### **Using composite resources**

* Composite resources have specific syntax. Review [the overview documentation for Composite Resources ](https://docs.microsoft.com/powershell/scripting/dsc/resources/authoringresourcecomposite?view=powershell-5.1).
* The [CompositeResource package on PowerShell Gallery](https://www.powershellgallery.com/packages/compositeresource/) can help create new composite resources

### **Using custom resources in State Configuration**

* Ensure your [module is uploaded to Azure Automation](https://docs.microsoft.com/azure/automation/shared-resources/modules) and the version is consistent with any local testing you have done

### **Review any errors from the compilation job**

* Follow the instructions in ["Viewing a compilation job"](https://docs.microsoft.com/azure/automation/automation-dsc-getting-started#viewing-a-compilation-job) to see error messages emitted by the configuration

### **No node configurations were produced after compilation**

* Review the ["No node configurations were produced when a configuration is compiled" section of the State Configuration troubleshooter](https://docs.microsoft.com/azure/automation/troubleshoot/desired-state-configuration#no-mof-files)

### **Using credentials with State Configuration**

* If your compilation job was suspended with the error "System.InvalidOperationException error processing property 'Credential' of type...", consult the ["Unable to use a credential" section of the State Configuration troubleshooter](https://docs.microsoft.com/azure/automation/troubleshoot/desired-state-configuration#issue-using-credential)

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
