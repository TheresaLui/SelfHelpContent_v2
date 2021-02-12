<properties
pageTitle="Modules were found that are not current"
description="Modules may need to be updated"
infoBubbleText="See list of affected modules below"
service="microsoft.automation"
resource="runbooks"
authors="adoyle"
ms.author="adoyle"
displayOrder=""
articleId="MoudleUpdate-48a86414-6e14-4785-8beb-33269666cc3e"
diagnosticScenario="AAModuleUpdateDetection"
selfHelpType="diagnostics"
supportTopicIds="32599853,32628003,32628005,32628006,32628008,32628009,32628012,32599860,32599906,32599907,32599908,32615224,32599909,32599923,32599854,32599917,32615220,32615221,32615222,32615223"
resourceTags="windows"
productPesIds="15607"
cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_Automation"
/>


# There are Automation Core Modules that need updating

## Automation Modules that are older or out of date can cause unforeseen issues
<!--issueDescription-->
We have detected that there are older versions of core Azure modules than what is currently available. Using older versions of Azure modules can cause unforeseen issues when running jobs. The following is a list of the modules we have detected in your Automation Account that are not the latest versions:

<!--$Modules Out of date-->[Modules Out of date]<!--/$Modules Out of date-->
<!--/issueDescription-->

## **Recommended Steps**

The Azure PowerShell modules are updated frequently to include fixes and improvements and it is a good practice to stay current when possible. 

* Follow these steps to [update your Automation modules](https://docs.microsoft.com/azure/automation/automation-update-azure-modules)
* Once this has completed, attempt to re-run the runbook that may have been failing previously
* If you are experiencing problems with a particular module you can try [upgrading only that module](https://docs.microsoft.com/azure/automation/automation-update-azure-modules#alternative-ways-to-update-your-modules) to the latest Azure PowerShell modules to correct your problem

**Note**: If the change in the modules would result in a major version upgrade, such as from 3.x to 4.x or 5.x to 6.x, then you would need to be aware that these major version updates include breaking changes. These changes can be to the way that cmdlets work which may result in broken scripts until they are adapted to use the changes that have been introduced. Carefully review the breaking changes guidance for the version of the modules, such as for [major version 6.x](https://github.com/Azure/azure-powershell/blob/preview/documentation/migration-guides/migration-guide.6.0.0.md), to determine if you need to update any of your runbook scripts to accommodate changes in the cmdlets they call.

Each major update has its own upgrade guidance. Review all the guides for the version you are upgrading from before you make any changes.


## **Recommended Documents**

* [Breaking changes for Microsoft Azure PowerShell 2.0.0](https://github.com/Azure/azure-powershell/blob/preview/documentation/migration-guides/migration-guide.2.0.0.md)
* [Breaking changes for Microsoft Azure PowerShell 3.0.0](https://github.com/Azure/azure-powershell/blob/preview/documentation/migration-guides/migration-guide.3.0.0.md)
* [Breaking changes for Microsoft Azure PowerShell 4.0.0](https://github.com/Azure/azure-powershell/blob/preview/documentation/migration-guides/migration-guide.4.0.0.md)
* [Breaking changes for Microsoft Azure PowerShell 5.0.0](https://github.com/Azure/azure-powershell/blob/preview/documentation/migration-guides/migration-guide.5.0.0.md)
* [Breaking changes for Microsoft Azure PowerShell 6.0.0](https://github.com/Azure/azure-powershell/blob/preview/documentation/migration-guides/migration-guide.6.0.0.md)
