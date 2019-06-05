<properties
pageTitle="Runbook(s) failure(s) detected with recent module updates"
description="Runbooks failing and recent module updates may be the cause"
infoBubbleText="See list of affected Runbooks below"
service="microsoft.automation"
resource="runbooks"
authors="adoyle"
authorAlias="adoyle"
displayOrder=""
articleId="rbmUpdate-48a86414-6e14-4785-8beb-33269666cc3e"
diagnosticScenario="AAModuleUpdateDetection"
selfHelpType="diagnostics"
supportTopicIds="32599853,32628003,32628005,32628006,32628008,32628009,32628012,32599860,32599906,32599907,32599908,32615224,32599909,32599923,32599854,32599917,32615220,32615221,32615222,32615223"
resourceTags="windows"
productPesIds="15607"
cloudEnvironments="public"
/>

# There are Runbook jobs failing and a recent update of Modules may be the cause.
## Runbook jobs can be impacted by module version changes

We have detected runbook failures occurring after an update of module versions. Module updates can contain breaking changes, resulting in scripts behaving unexpectedly. We recommend maintaining a separate automation account to test module updates before deploying them to production.

To resolve this issue ,you can roll back to a previous module version by navigating to the "Modules" page under your Automation Account, selecting modules that have been recently updated, and choosing "Delete". Then you can re-import a previous version of the module following the instructions at [Import Modules](https://docs.microsoft.com/en-us/azure/automation/shared-resources/modules#import-modules). 
The following is a list of the Runbook failures we have detected in your Automation Account:
<!--$Jobfailures-->[Jobfailures]<!--/$Jobfailures-->

## Resolution

To learn more about updating your modules, see Update Azure modules in Azure Automation. To troubleshoot common failures for runbook execution see [Troubleshooting Runbooks](https://docs.microsoft.com/azure/automation/troubleshoot/runbooks)

The Azure PowerShell modules are updated frequently to include fixes and improvements and it is a good practice to stay current when possible.
If you are experiencing problems with a particular module you can try upgrading only that module to the latest Azure PowerShell modules to correct your problem. To learn how to do this, see [alternative ways to update your modules](https://docs.microsoft.com/azure/automation/automation-update-azure-modules#considerations)
However, if the change in the modules would result in a major version upgrade, such as from 3.x to 4.x or 5.x to 6.x then you would need to be aware that these major version updates include breaking changes. These changes can be to the way that cmdlets work which may result in broken scripts until they are adapted to use the changes that have been introduced.
You would need to carefully review the breaking changes guidance for the version of the modules, such as for [major version 6.x](https://github.com/Azure/azure-powershell/blob/preview/documentation/migration-guides/migration-guide.6.0.0.md) to determine if you need to update any of your runbook scripts to accommodate changes in the cmdlets they call.
Each major update has its own upgrade guidance. You would need to review all the guides for the version you are upgrading from before you make any changes.

* [Breaking changes for Microsoft Azure PowerShell 2.0.0](https://github.com/Azure/azure-powershell/blob/preview/documentation/migration-guides/migration-guide.2.0.0.md)

* [Breaking changes for Microsoft Azure PowerShell 3.0.0](https://github.com/Azure/azure-powershell/blob/preview/documentation/migration-guides/migration-guide.3.0.0.md)

* [Breaking changes for Microsoft Azure PowerShell 4.0.0](https://github.com/Azure/azure-powershell/blob/preview/documentation/migration-guides/migration-guide.4.0.0.md)

* [Breaking changes for Microsoft Azure PowerShell 5.0.0](https://github.com/Azure/azure-powershell/blob/preview/documentation/migration-guides/migration-guide.5.0.0.md)

* [Breaking changes for Microsoft Azure PowerShell 6.0.0](https://github.com/Azure/azure-powershell/blob/preview/documentation/migration-guides/migration-guide.6.0.0.md)
