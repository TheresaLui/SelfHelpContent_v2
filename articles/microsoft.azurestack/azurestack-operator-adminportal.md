<properties
    pageTitle="Azure Stack Administration portal"
    description="Issues related to Azure Stack Admin Portal"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629245"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public"
    articleId="azurestack-operator-adminportal"
/>

# Azure Stack Administration Portal

There are two portals in Azure Stack: the administration portal and the user portal (sometimes referred to as the tenant portal). As an Azure Stack operator, you can use the administration portal for day-to-day management and operations of Azure Stack.

## **Recommended Steps**

To access the administrator portal, browse to the portal URL and sign in by using the credentials of an Azure Stack operator.

* For single-node ASDK environments, the admin portal is hosted at- `https://adminportal.local.azurestack.external`.
* For multi-node integrated systems, the portal address varies based on the region name and fully-qualified domain name (FQDN) of your Azure Stack deployment. It will match the pattern- `https://adminportal.<REGION>.<FQDN>`.
* Subscriptions are created by users in the user portal based on the plans and offers you create for them. However, the user portal doesn't provide access to any of the administrative or operational capabilities of the administration portal.

## **Recommended Documents**

* [Using the administrator portal in Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-manage-portals)
