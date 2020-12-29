<properties
  pagetitle="Azure pipelines issues while making use of Approvals, gates, and checks&#xD;"
  service="microsoft.visualstudio"
  resource="account"
  ms.author="v-abiss,vimalt"
  selfhelptype="Generic"
  supporttopicids="32742291"
  resourcetags=""
  productpesids="15543"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="azdevops"
  ownershipid="Azure_DevOps_Services" />
# Azure pipelines issues while making use of Approvals, gates, and checks

## **Recommended Steps**

Are you facing one of these common problems?

* Unable to determine how to configure a Release Gate to get the needed Build & WorkItem information? [Refer to this document](https://docs.microsoft.com/azure/devops/pipelines/release/deploy-using-approvals?view=azure-devops).

* How to approve pipeline without navigating to the Azure DevOps portal? Invoking the **REST APIs** to list/update approvals is the only way to complete approvals without going to the Azure DevOps website. You'll need to get approval ID by listing all pending approvals before completing it. Approving from the web page is the simplest way.

* Unable to change the approval and security settings for the pipelines? Ensure that the concerned user has the right permissions and also make sure the user is added to the right group which has sufficient permissions to change the required settings.

* Revalidation Error when the users click **Approve** in Azure DevOps Pipeline? Clearing the cookies & cache on the browser should resolve this issue.

* Unable to see a **gate/check** in the UI? You can add additional Gates to your organization using [marketplace extensions](https://marketplace.visualstudio.com/azuredevops). Installing the right extension would help you select the missing gate.

We do not have support for adding custom checks through extensions. We recommend modelling **Invoke REST API** or **Invoke Azure Function** check to work with the service of your choice.

## **Recommended Documents**

* [Release approvals and gates overview](https://docs.microsoft.com/azure/devops/pipelines/release/approvals/?view=azure-devops)
* [Define approvals and checks](https://docs.microsoft.com/azure/devops/pipelines/process/approvals?view=azure-devops&tabs=check-pass)
* [Release deployment control using gates](https://docs.microsoft.com/azure/devops/pipelines/release/approvals/gates?view=azure-devops)
* [Use approvals and gates to control your deployment](https://docs.microsoft.com/azure/devops/pipelines/release/deploy-using-approvals?view=azure-devops)
* [Release deployment control using approvals](https://docs.microsoft.com/azure/devops/pipelines/release/approvals/approvals?view=azure-devops)
* Want a quicker answer? For quick answers to common questions and issues, try the [Azure DevOps Virtual Agent](https://azuredevopsvirtualagent.azurewebsites.net/)