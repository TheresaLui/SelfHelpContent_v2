<properties
    pageTitle="Azure Stack billing and usage CSP support recommendations"
    description=""
    service="microsoft.azurestack"
    resource="azurestack"
    authors=""
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32567962, 32567905"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public"
/>

# Azure Stack CSP billing and usage 

As a Cloud Provider (CSP), you work with diverse customers using your Azure Stack. Each customer has a CSP subscription in Azure. You'll need to direct usage from your Azure Stack to each user subscription. For more information, see [Add tenant for usage and billing to Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-csp-howto-register-tenants).

## **Recommended steps**

1. In Partner Center, create a new Azure subscription for the customer. For instructions, see [Add a new customer](https://msdn.microsoft.com/partner-center/add-a-new-customer).<br>
2. After you've created a record of your customer in Partner Center, you can sell them subscriptions to products in the catalog. For instructions, see [Create, suspend, or cancel customer subscriptions](https://msdn.microsoft.com/partner-center/create-a-new-subscription).<br>
3. If the end customer will manage their own account, create a guest user in their directory, and send them the information. The end user will then add the guest and elevate the guest permission to **Owner** to the Azure Stack CSP account.<br>
4. Update the registration with the end customer subscription:<br>
```
New-AzureRmResource -ResourceId "subscriptions/{registrationSubscriptionId}/resourceGroups/{resourceGroup}/providers/Microsoft.AzureStack/registrations/{registrationName}/customerSubscriptions/{customerSubscriptionId}" -ApiVersion 2017-06-01 -Properties <PSObject>
```

## **Recommended documents**

[Add tenant for usage and billing to Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-csp-howto-register-tenants)<br>
[Manage tenant registration in Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-csp-ref-operations)