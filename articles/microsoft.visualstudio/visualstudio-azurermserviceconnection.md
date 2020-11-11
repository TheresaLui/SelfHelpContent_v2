<properties
	pageTitle="Azure ARM Service Connections"
	description="Issues related to ARM service connection creation, permissions, user interface, different options available in UI or any other guidances related to service connection."
	infoBubbleText="Azure Pipelines issues related to Service Endpoints"
	service="microsoft.visualstudio"
	resource="account"
	authors="v-abiss"
	ms.author="v-abiss"
	articleId="AzureRMServiceConnection"
	supportTopicIds="32742301"
	diagnosticScenario=""
	selfHelpType="generic"
	resourceTags=""
	productPesIds="15543"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Azure_DevOps_Services"
/>

# Azure pipelines issues while making use of Azure Service Connections

## **Recommended Steps**

* I can't assign an azure subscription to a new release

    Ensure you are using a subscription with a resource group to which you are authorized to deploy. To push a release, make sure you have the appropriate [user roles/access](https://docs.microsoft.com/azure/role-based-access-control/rbac-and-directory-admin-roles) to the subscription.

* Unable to select a subscription even if I'm the Admin and Owner of it. I also cannot create a new **Service Connection**.
	
    Check the role of the **App Registration**. Update the role of the **App Registration** manually and retry [Creating a new Service Connection](https://docs.microsoft.com/azure/devops/pipelines/library/service-endpoints?view=azure-devops&tabs=yaml). This often happens if you had an existing service connection and the Service Principal associated with it got expired. While trying to renew it, the App registration may have lost the proper role which might be  causing conflicts when trying to use it.

* I'm unable to authenticate the **Service Principal** in my CI/CD pipeline

    Check your [Azure AD permissions](https://docs.microsoft.com/azure/active-directory/develop/howto-create-service-principal-portal#check-azure-ad-permissions) and [assign the appropriate roles](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-assign-role-azure-portal)

* I'm unable to create a service connection

    Ensure you have the appropriate [user roles/access](https://docs.microsoft.com/azure/role-based-access-control/rbac-and-directory-admin-roles) assigned.

* Failed to authorize the service connection resource for pipeline

    Make sure the right service connection is selected in the pipeline and the necessary [pipeline permissions](https://docs.microsoft.com/azure/devops/pipelines/library/service-endpoints?view=azure-devops&tabs=yaml#pipeline-permissions) are granted to access this service connection.

* I'm unable to see my subscriptions while creating a service connection even after having the necessary permissions

    If you're using some part of Azure DevOps that interacts with Azure and it appears not to be working, we recommend logging out and logging back in from an incognito/inPrivate browse. This will generate a new, valid token that Azure DevOps can use to authenticate the request to Azure, which will query the subscriptions and generate the service connection. 

## **Recommended Documents**

* [Service Connections](https://docs.microsoft.com/azure/devops/pipelines/library/service-endpoints?view=azure-devops&tabs=yaml#use-a-service-connection)
* [Azure Resource Manager Service Connection](https://docs.microsoft.com/azure/devops/pipelines/library/connect-to-azure?view=azure-devops)
* [Troubleshoot Azure Resource Manager service connections](https://docs.microsoft.com/azure/devops/pipelines/release/azure-rm-endpoint?view=azure-devops)
* [Azure Resource Manager service connection using automated security](https://docs.microsoft.com/azure/devops/pipelines/library/connect-to-azure?view=azure-devops)
