
<properties
pageTitle="Issues linking Automation account"
description="Issues linking Automation account"
service="microsoft.operationalinsights"
resource="workspaces"
articleId="a89bf446-83cb-4993-a918-7dbd139cf6d8"
symptomID=""
infoBubbleText=""
authors="yossiy"
ms.author="yossiy"
displayorder="9"
selfHelpType="Generic"
supportTopicIds="32612473"
resourceTags=""
productPesIds="15725"
cloudEnvironments="Public, Fairfax, usnat, ussec"
ownershipId="AzureMonitoring_LogAnalytics"
/>

# Issues linking Automation account
Linking Automation account to Log Analytics workspace requires that both resources are placed in the same “Resource Group”.
The Automation account and workspace link is created with the installation of *Automation & Control* solution in the workspace.
## **Recommended steps**
To link an Automation account to a Log Analytics workspace, follow these steps:<br>
* [Create Automation account](https://docs.microsoft.com/azure/automation/automation-quickstart-create-account)
* Install *Automation & Control* solution<br>
    * Click the '+' icon in Azure portal to create a resource
    * Start typing *Automation & Control*, select it from the list and click *Create*
    * Select the workspace to install the solution in and click *Create*<br>
* Automation account is now linked to your workspace.
 
 To verify that the Automation account is linked to your workspace, follow these steps:<br>
 * From Automation account, click Linked workspace* on the left pane
* A view with a linked workspace is presented (if linked)
* When needed, you can unlink the workspace by clicking *Unlink workspace* on the ribbon<br>

**Important:** The removal of Automation & Control solution from workspace doesn't remove the link to the Automation account. To remove the link, follow the steps in 'Automation account link verification' above.

## **Recommended documents**
* [Unlink workspace](https://docs.microsoft.com/azure/automation/automation-onboard-solutions-from-browse#unlink-workspace)
* [Azure Automation User Documentation](https://docs.microsoft.com/azure/automation/)
* [Forward job status and job streams from Automation to Log Analytics](https://docs.microsoft.com/azure/automation/automation-manage-send-joblogs-log-analytics)