<properties
    pageTitle="Application Gateway in Failed state"
    description="Application Gateway in Failed state"
    service="microsoft.network"
    resource="applicationgateways"
    authors="TobyTu"
    ms.author="mariliu"
    displayOrder="39"
    selfHelpType="resource"
    articleId="7640a487-6f9f-4a3c-9e53-5c75862cc1f9"
    resourceTags=""
    productPesIds="15922"
    supportTopicIds="32783359"
    cloudEnvironments="public,fairfax,mooncake,blackforest,ussec,usnat"
    ownershipId="CloudNet_AzureApplicationGateway"
/>

# Application Gateway in Failed state

<!--/issueDescription-->
If you make any changes to your Application Gateway, a PUT operation is performed on the gateway resource to update the configuration. If Application Gateway is in a **Failed** state, this generally means that one or more components of the configuration has issues, but your gateway will continue to serve requests.

- Update or PUT operations can be triggered directly by the user using any of the available methods, such as Azure portal, Azure PowerShell, CLI, or REST API.
- These operations can also be triggered indirectly by another resource. For example:

  - When you have a VMSS in the backend pool of your Application Gateway and it scales out or in, then an internal PUT call is made to the Application Gateway to update the newly added or removed instances.
  - When a VM IP configuration is added to the backend pool, whenever the NIC IP changes, an internal PUT call is made to the Application Gateway to update the new IP address.

If any of the PUT operations is running for a long time (more than an hour), it can eventually fail, making the provisioning state **Failed**. Note that Application Gateway in a **Failed** state just means that there is an issue with the configuration, but your Application Gateway will still be running and serving traffic, and there is no data-path impact.
<!--/issueDescription-->

## **Recommended Steps**

If your Application Gateway is in a **Failed** state, follow these steps to recover it:

1. Check the error message from the previously failed operation. The error message indicates what went wrong in the configuration. For example, there might be a mismatch in the frontend IP address, or the certificate file that you have uploaded is faulty.
2. Based on the error message, you can modify the configuration accordingly and retry the operation.
3. Alternatively, you can try executing the Azure PowerShell [Get-AzApplicationGateway](https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgateway?view=azps-5.3.0&viewFallbackFrom=azps-1.7.0) and [Set-AzApplicationGateway](https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgateway?view=azps-5.3.0&viewFallbackFrom=azps-1.7.0) commands in sequence and check to see if the Application Gateway recovers from the **Failed** state.

## **Recommended Documents**

- [Application Gateways - Create or Update](https://docs.microsoft.com/rest/api/application-gateway/applicationgateways/createorupdate)
