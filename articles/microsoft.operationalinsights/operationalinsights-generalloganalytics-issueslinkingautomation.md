
<properties
pageTitle="Issues linking Automation account"
description="Issues linking Automation account"
service="microsoft.operationalinsights"
resource="workspaces"
symptomID=""
infoBubbleText=""
authors="yossiy"
displayorder="500"
selfHelpType="resource"
supportTopicIds="32612473"
resourceTags=""
productPesIds="15725"
cloudEnvironments="Public, Fairfax"
/>
# Issues linking Automation account
Linking Automation account to Log Analytics workspace requires that both resources are placed in the same “Resource Group”.
The Automation account and workspace link is created with the installation of *Automation & Control* solution in the workspace.
## **Recommended steps**
To link Automation account to Log Analytics workspace, follow these steps:
* [Create Automation account](https://docs.microsoft.com/azure/automation/automation-quickstart-create-account)
* Install *Automation & Control* solution
    * Click the '+' icon in Azure portal to create a resource
    * Start typing *Automation & Control*, select it from the list and click *Create*
    * Select the workspace to install the solution in and click *Create*
* Automation account is now linked to your workspace.
 
 If you want to verify that Automation account is linked to your workspace, follow these steps:
* From Automation account, click Linked workspace* on the left pane
* A view with a linked workspace is presented (if linked)
* When needed, you can unlink the workspace by clicking *Unlink workspace* on the ribbon

> The removal of *Automation & Control* solution from workspace doesn't remove the link to Automation account. To remove the link, follow the steps in 'Automation account link verification' above.
## **Recommended documents**
* [Unlink workspace](https://docs.microsoft.com/azure/automation/automation-onboard-solutions-from-browse#unlink-workspace)
* [Azure Automation User Documentation](https://docs.microsoft.com/azure/automation/)
* [Forward job status and job streams from Automation to Log Analytics](https://docs.microsoft.com/azure/automation/automation-manage-send-joblogs-log-analytics)