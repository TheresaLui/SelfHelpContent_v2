<properties
    pageTitle="Configure SSL policy"
    description="Configure SSL policy"
    service="microsoft.network"
    resource="applicationgateways"
    authors="TobyTu"
    ms.author="mariliu"
    displayOrder="35"
    selfHelpType="resource"
    articleId="7640a487-6f9f-4a3c-9e53-5c75862cc1f5"
    resourceTags=""
    productPesIds="15922"
    supportTopicIds="32783365"
    cloudEnvironments="public,fairfax,mooncake,blackforest,ussec,usnat"
    ownershipId="CloudNet_AzureApplicationGateway"
/>

# Configure SSL policy

## **Recommended Steps**

With Application Gateway, you can either set predefined SSL policies with a minimum TLS version and a set of preselected cipher suites, or you can set your own custom policy with a minimum TLS version and cipher suites of your choice.

To configure SSL policies, follow these steps:

1. Navigate to the **Listeners** tab of your Application Gateway in the Azure portal.
2. Under the **SSL policy** section, select the **change** option.
3. Choose from one of the predefined policies or choose a custom policy.
4. Select **Save**.

After your custom SSL policy is saved, it will be common to all your listeners and you can manage it directly from the portal.

## **Recommended Documents**

- [Application Gateway TLS policy overview](https://docs.microsoft.com/azure/application-gateway/application-gateway-ssl-policy-overview)
- [Configure TLS policy versions and cipher suites on Application Gateway](https://docs.microsoft.com/azure/application-gateway/application-gateway-configure-ssl-policy-powershell)
- [TLS termination and end-to-end TLS with Application Gateway overview](https://docs.microsoft.com/azure/application-gateway/ssl-overview)
