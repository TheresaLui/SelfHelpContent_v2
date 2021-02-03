<properties
  pagetitle="Azure pipelines issues while making use of Approvals, gates, and checks&#xD;"
  service="microsoft.visualstudio"
  resource="account"
  ms.author="v-abiss,vimalt,cathmill"
  selfhelptype="Generic"
  supporttopicids="32742291"
  resourcetags=""
  productpesids="15543"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="azdevops"
  ownershipid="Azure_DevOps_Services" />
# Azure pipelines issues while making use of Approvals, gates, and checks

Most users can resolve issues with Azure Piplines regarding approvals, gates, and checks by using the following information.

## **Recommended Steps**

* Unable to determine how to configure a Release Gate to get the needed Build & WorkItem information <br>
See [deploy using Approvals](https://docs.microsoft.com/azure/devops/pipelines/release/deploy-using-approvals?view=azure-devops).

* How to approve pipeline without navigating to the Azure DevOps portal<br> 
The only way to complete (that is, list or update) approvals without going to the Azure DevOps website is to invoke the REST APIs. You'll need to get approval ID by listing all pending approvals before completing it. Approving from the web page is the simplest way.

* Unable to change the approval and security settings for the pipelines<br>
Ensure that the user has the right permissions. Also, make sure the user is added to the group that has sufficient permissions to change the required settings.

* Revalidation error when the users select **Approve** in the Azure DevOps Pipeline <br>
Clear the cookies and cache on the browser to resolve this issue.

* Unable to see a **gate/check** in the UI <br>
You can add additional gates to your organization by using [marketplace extensions](https://marketplace.visualstudio.com/azuredevops). Installing the correct extension will help you select the missing gate.

We don't have support for adding custom checks through extensions. We recommend modeling an **Invoke REST API** or an **Invoke Azure Function** check to work with the service of your choice.

## **Recommended Documents**

* [Release approvals and gates overview](https://docs.microsoft.com/azure/devops/pipelines/release/approvals/?view=azure-devops)
* [Define approvals and checks](https://docs.microsoft.com/azure/devops/pipelines/process/approvals?view=azure-devops&tabs=check-pass)
* [Release deployment control using gates](https://docs.microsoft.com/azure/devops/pipelines/release/approvals/gates?view=azure-devops)
* [Use approvals and gates to control your deployment](https://docs.microsoft.com/azure/devops/pipelines/release/deploy-using-approvals?view=azure-devops)
* [Release deployment control using approvals](https://docs.microsoft.com/azure/devops/pipelines/release/approvals/approvals?view=azure-devops)
* For service impacting issues, check the [Azure DevOps Services Status](https://status.dev.azure.com)
* For quick answers to common questions and issues, try the [Azure DevOps Virtual Agent](https://azuredevopsvirtualagent.azurewebsites.net/)
