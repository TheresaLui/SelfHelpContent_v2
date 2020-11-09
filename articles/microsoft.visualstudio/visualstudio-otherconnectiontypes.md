<properties
	pageTitle="Azure Service Fabric"
	description="Issues related to any other type of service connections not listed here, creation, permissions, user interface, different options available in UI or any other guidances related to service connection."
	infoBubbleText="Azure Pipelines issues related to other Azure service connections"
	service="microsoft.visualstudio"
	resource="account"
	authors="v-abiss"
	ms.author="v-abiss"
	articleId="AzureOtherConnectionTypes"
	supportTopicIds="32742325"
	diagnosticScenario=""
	selfHelpType="generic"
	resourceTags=""
	productPesIds="15543"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Azure_DevOps_Services"
/>

# Azure pipelines issues while using other Azure services connections

## **Recommended Steps**

Are you facing one of these common problems?

****

* **I'm unable to link Azure DevOps with Bitbucket**

    Ensure that you have the sufficient permissions on the subscription so that you can make a connection.

* **Unable to create service connection using Azure ML with the error :"Failed to create an app in Azure Active Directory"**

    Ensure that you have sufficient permissions to create an Azure Active Directory Application. [Refer to this document](https://docs.microsoft.com/azure/active-directory/fundamentals/add-users-azure-active-directory?context=azure/active-directory/users-groups-roles/context/ugr-context).

* **I'm unable to connect to another GIT Repo from Pipeline. Git clone failed with the error code 128**

    Create an "[Other Git](https://docs.microsoft.com/en-us/azure/devops/pipelines/library/service-endpoints?view=azure-devops&tabs=yaml#sep-extgit)" service connection and provide the right the username and password.

* **The Github release agent is not able to view the "Private" repo even though the Github service connection has all access.**

    Ensure your build pipeline is compiled from the corresponding GitHub repo and in the Release pipeline, make use of the variable **$(Build.SourceVersion)**. If you are making use of the build from a different repo, then you'll have to manually pass the commit id.

* **I'm unable to generate a Service Principal for data factory using powershell script**

    If it is an issue related to the Service Principal permission in AAD, Service Principal by default has no permission to read AAD data. In such cases, assign the [Directory Readers](https://docs.microsoft.com/azure/active-directory/roles/permissions-reference#directory-readers) role to the Service Principal used in Azure DevOps.


## **Recommended Documents**

* [Access to Bitbucket repositories](https://docs.microsoft.com/azure/devops/pipelines/repos/bitbucket?view=azure-devops&tabs=yaml#access-to-bitbucket-repositories)
* [Administrator role permissions in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/roles/permissions-reference)
* [Create a service hook for Azure DevOps Services and TFS with Jenkins](https://docs.microsoft.com/azure/devops/service-hooks/services/jenkins?view=azure-devops)
* [Connect on-premises Bitbucket repositories](https://docs.microsoft.com/azure/devops/pipelines/repos/on-premises-bitbucket?view=azure-devops)
