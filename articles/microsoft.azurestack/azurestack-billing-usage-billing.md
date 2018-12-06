<properties
    pageTitle="Azure Stack billing and usage support recommendations"
    description=""
    service="microsoft.azurestack"
    resource="azurestack"
    authors=""
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32567924"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public"
/>

# Azure Stack billing and usage 

Azure Stack collects and groups usage data for resources that are used. Then Azure Stack forwards this data to Azure Commerce. Azure Commerce bills you for Azure Stack usage in the same way it bills you for Azure usage.

## **Recommended steps**

Each customer has their identity represented by a different Azure Active Directory (Azure AD) tenant. Azure Stack supports assigning one CSP subscription to each Azure AD tenant. You can add tenants and their subscriptions to the base Azure Stack registration. The base registration is done for all Azure Stacks. If a subscription is not registered for a tenant, the user can still use Azure Stack, and their usage will be sent to the subscription used for the base registration. 

## **Recommended documents**

[Report Azure Stack usage data to Azure](https://docs.microsoft.com/azure/azure-stack/azure-stack-usage-reporting)<br>
[Add tenant for usage and billing to Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-csp-howto-register-tenants)