<properties
  pagetitle="Azure pipelines issues while making use of Azure Service Connections&#xD;"
  service="microsoft.visualstudio"
  resource="account"
  ms.author="v-abiss,cathmill"
  selfhelptype="Generic"
  supporttopicids="32742301"
  resourcetags=""
  productpesids="15543"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="azurermserviceconnection"
  ownershipid="Azure_DevOps_Services" />
# Azure pipelines issues while making use of Azure Service Connections

## **Recommended Steps**

* I can't assign an Azure subscription to a new release

    Ensure you are using a subscription with a resource group to which you're authorized to deploy. To push a release, make sure you have the appropriate [user roles/access](https://docs.microsoft.com/azure/role-based-access-control/rbac-and-directory-admin-roles) to the subscription.

* Unable to select a subscription even if I'm the Admin and Owner of it. I also can't create a new **Service Connection**.
	
    Check the role of the **App Registration**. Update the role of the **App Registration** manually and retry [Creating a new Service Connection](https://docs.microsoft.com/azure/devops/pipelines/library/service-endpoints?view=azure-devops&tabs=yaml). This often happens if you had an existing service connection and the Service Principal associated with it was expired. While trying to renew it, the App registration may have lost the proper role, which might cause conflicts when you try to use it.

* I'm unable to authenticate the **Service Principal** in my CI/CD pipeline

    Check your [Azure AD permissions](https://docs.microsoft.com/azure/active-directory/develop/howto-create-service-principal-portal#check-azure-ad-permissions) and [assign the appropriate roles](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-assign-role-azure-portal)

* I'm unable to create a service connection

    Ensure you have the appropriate [user roles/access](https://docs.microsoft.com/azure/role-based-access-control/rbac-and-directory-admin-roles) assigned.

* Failed to authorize the service connection resource for the pipeline

    Make sure the right service connection is selected in the pipeline and the necessary [pipeline permissions](https://docs.microsoft.com/azure/devops/pipelines/library/service-endpoints?view=azure-devops&tabs=yaml#pipeline-permissions) are granted to access this service connection.

* I'm unable to see my subscriptions while creating a service connection even after having the necessary permissions

    If you're using some part of Azure DevOps that interacts with Azure and it appears not to be working, we recommend logging out and logging back in from an incognito/inPrivate browse. This will generate a new, valid token that Azure DevOps can use to authenticate the request to Azure, which will query the subscriptions and generate the service connection. 

## **Recommended Documents**

* [Service Connections](https://docs.microsoft.com/azure/devops/pipelines/library/service-endpoints?view=azure-devops&tabs=yaml#use-a-service-connection)
* [Azure Resource Manager Service Connection](https://docs.microsoft.com/azure/devops/pipelines/library/connect-to-azure?view=azure-devops)
* [Troubleshoot Azure Resource Manager service connections](https://docs.microsoft.com/azure/devops/pipelines/release/azure-rm-endpoint?view=azure-devops)
* [Azure Resource Manager service connection using automated security](https://docs.microsoft.com/azure/devops/pipelines/library/connect-to-azure?view=azure-devops)
* For service-impacting issues, see [Azure DevOps Services Status](https://status.dev.azure.com/)
* For quick answers to common questions and issues, try the [Azure DevOps Virtual Agent](https://azuredevopsvirtualagent.azurewebsites.net/)
