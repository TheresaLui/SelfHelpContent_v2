<properties
    pageTitle="Azure Stack App Service resource provider"
    description="Azure Stack App Service deployment, update and operational issues"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="v-miegge"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629190,32629191"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="38c5358c-c63b-4043-9126-4b0839179085"
	ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# Azure Stack App Service Resource Provider

Azure App Service on Azure Stack is a platform-as-a-service (PaaS) offering that enables your customers to create web, API, and Azure Functions applications for any platform or device. They can integrate your apps with on-premises applications and automate their business processes. Azure Stack cloud operators can run customer apps on fully managed virtual machines (VMs), with their choice of shared VM resources or dedicated VMs.

**Please note:** Some tenant portal user experiences for App Service are affected by an incompatibility with the portal framework in Azure Stack 1903 Update; principally, the user interface for deployment slots, testing in production, and site extensions. To work around this issue, use the [Azure App Service PowerShell](https://docs.microsoft.com/azure/app-service/deploy-staging-slots#automate-with-powershell) module or the [Azure CLI](https://docs.microsoft.com/cli/azure/webapp/deployment/slot?view=azure-cli-latest). The portal experience will be restored in the upcoming release of Azure App Service on Azure Stack 1.6 (Update 6).

## **Recommended Steps**

Deploy App Service in Azure Stack

1. To set up a production ready deployment, first perform [capacity planning for Azure App Service](https://docs.microsoft.com/azure/azure-stack/azure-stack-app-service-capacity-planning)
2. Complete the App Service resource provider deployment prerequisite steps
3. Ensure you have the required [App Service certificates for Azure Stack](https://docs.microsoft.com/azure-stack/operator/azure-stack-app-service-before-you-get-started#certificates-required-for-azure-stack-production-deployment-of-azure-app-service)
4. [Deploy the App Service resource provider](https://docs.microsoft.com/azure/azure-stack/azure-stack-app-service-deploy) as per the instructions (optional offline steps are provided)
5. Review the release notes for your version of App Services provider for latest features, fixes, optional steps, and known issues
6. [Update Azure App Service](https://docs.microsoft.com/azure/azure-stack/azure-stack-app-service-update) provider when new versions are released

Use Azure Stack marketplace items to [deploy App Service for Azure Stack in a highly available configuration](https://docs.microsoft.com/azure-stack/operator/app-service-deploy-ha?view=azs-1908).

## **Recommended Documents**

* [Capacity planning for Azure App Service](https://docs.microsoft.com/azure/azure-stack/azure-stack-app-service-capacity-planning)
* [Before you get started with App Service](https://docs.microsoft.com/azure/azure-stack/azure-stack-app-service-before-you-get-started)
* [Deploy the App Service resource provider](https://docs.microsoft.com/azure/azure-stack/azure-stack-app-service-deploy)
* [Deploy the App Service resource provider offline](https://docs.microsoft.com/azure/azure-stack/azure-stack-app-service-deploy-offline)
* [Update Azure App Service](https://docs.microsoft.com/azure/azure-stack/azure-stack-app-service-update)
* [Update Azure App Service offline](https://docs.microsoft.com/azure/azure-stack/azure-stack-app-service-update-offline)
* [Scale infrastructure and worker roles in App Service](https://docs.microsoft.com/azure-stack/operator/azure-stack-app-service-add-worker-roles)
* [Use API version profiles](https://docs.microsoft.com/azure-stack/user/azure-stack-version-profiles?view=azs-1910)

