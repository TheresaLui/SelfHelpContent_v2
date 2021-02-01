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

Refer to the following solutions to resolve issues in Azure pipeline when using other Auzre services connections. 

## **Common issues with Azure pipelines**

* **Unable to link Azure DevOps with Bitbucket**

    Ensure that you have the sufficient permissions on the subscription to make a connection.<br><br>
    

* **Error when creating service connection using Azure ML: "Failed to create an app in Azure Active Directory"**

    Ensure that you have sufficient permissions to create an Azure Active Directory Application. [Refer to this document](https://docs.microsoft.com/azure/active-directory/fundamentals/add-users-azure-active-directory?context=azure/active-directory/users-groups-roles/context/ugr-context).<br><br>
    

* **Unable to connect to another GIT Repo from Pipeline: "Git clone failed with the error code 128"**

    Create another **[external Git service connection](https://docs.microsoft.com/azure/devops/pipelines/library/service-endpoints?view=azure-devops&tabs=yaml#sep-extgit)** and provide the right the username and password.<br><br>
    

* **Unable to generate a Service Principal for data factory using powershell script**

    If the issue is related to the Service Principal permission in AAD, Service Principal by default has no permission to read AAD data. In such cases, assign the [Directory Readers](https://docs.microsoft.com/azure/active-directory/roles/permissions-reference#directory-readers) role to the Service Principal used in Azure DevOps.<br><br>


## **Recommended Documents**

* [Access to Bitbucket repositories](https://docs.microsoft.com/azure/devops/pipelines/repos/bitbucket?view=azure-devops&tabs=yaml#access-to-bitbucket-repositories)
* [Administrator role permissions in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/roles/permissions-reference)
* [Create a service hook for Azure DevOps Services and TFS with Jenkins](https://docs.microsoft.com/azure/devops/service-hooks/services/jenkins?view=azure-devops)
* [Connect on-premises Bitbucket repositories](https://docs.microsoft.com/azure/devops/pipelines/repos/on-premises-bitbucket?view=azure-devops)
* For service-impacting issues, see [Azure DevOps Services Status](https://status.dev.azure.com/)
* Want a quicker answer? For quick answers to common questions and issues, try the [Azure DevOps Virtual Agent](https://azuredevopsvirtualagent.azurewebsites.net/)
