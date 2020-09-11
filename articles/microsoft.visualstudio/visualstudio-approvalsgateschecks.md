<properties
	pageTitle="Approvals, gates, and checks"
	description="Issues related to setting up approvals, gates, or checks in classic release or multi-stage YAML pipelines, errors with their usage, and permissions"
	infoBubbleText="Azure Pipelines issues related to Approvals, gates, and checks"
	service="microsoft.visualstudio"
	resource="account"
	authors="v-abiss"
	ms.author="v-abiss"
	articleId="AZDevOps"
	supportTopicIds="32742291"
	diagnosticScenario=""
	selfHelpType="generic"
	resourceTags=""
	productPesIds="15543"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Azure_DevOps_Services"
/>

# Azure pipelines issues while making use of Approvals, gates, and checks

## **Recommended Steps**

Are you facing one of these common problems?

* Unable to determine how to configure a Release Gate to get the needed Build & WorkItem information

    [Refer to this document](https://docs.microsoft.com/azure/devops/pipelines/release/deploy-using-approvals?view=azure-devops).

* How to approve pipeline without navigating to the Azure DevOps portal
	
    Currently, we don’t have a feature to allow the approvers to approve directly through an email notification. We do have **Rest APIs** to list/update approvals so that we don’t need to go to Azure DevOps website. However, the Rest API method is more complicated because, before we update approvals, we have to get the approval ID first by listing all pending approvals. Approving from the web page is the simplest way.

* Unable to change the approval and security settings for the pipelines.

    Ensure that the concerned user has the right permissions and also make sure the user is added to the right group which has sufficient permissions to change the required settings

* Revalidation Error when the users click **Approve** in Azure DevOps Pipeline

    Clearing the cookies & cache on the browser should resolve this issue


## **Recommended Documents**

* [Release approvals and gates overview](https://docs.microsoft.com/azure/devops/pipelines/release/approvals/?view=azure-devops)
* [Define approvals and checks](https://docs.microsoft.com/azure/devops/pipelines/process/approvals?view=azure-devops&tabs=check-pass)
* [Release deployment control using gates](https://docs.microsoft.com/azure/devops/pipelines/release/approvals/gates?view=azure-devops)
* [Use approvals and gates to control your deployment](https://docs.microsoft.com/azure/devops/pipelines/release/deploy-using-approvals?view=azure-devops)
* [Release deployment control using approvals](https://docs.microsoft.com/azure/devops/pipelines/release/approvals/approvals?view=azure-devops)