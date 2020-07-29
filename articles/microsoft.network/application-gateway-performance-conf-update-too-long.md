<properties
    pageTitle="Application Gateway Configuration update taking too long"
    description="Self-help content for Performance - Application Gateway Configuration update taking too long"
    service="microsoft.network"
    resource="applicationgateways"
    authors="abshamsft"
    ms.author="absha"
    displayOrder="22"
	selfHelpType="resource"
    articleId="application-gateway-performance-conf-update-too-long"
 	resourceTags=""
	productPesIds="15922"
    supportTopicIds="32680756"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
 	ownershipId="CloudNet_AzureApplicationGateway"
/>

# Configuration update taking too long
Once a configuration change has been made, for an existing Application Gateway of v1 SKU, it is expected to take up to 5 to 20 minutes for the update process to be completed. For v2 SKU, it is expected to take up to 1 to 2 minutes. If your update or PUT operation on the Application Gateway is taking significantly longer than expected, there are possibilities of update failures.

If your update operation failed and the Application Gateway is in a failed state, it might still be running and serving the client requests but you cannot make any changes to the configuration until it is recovered from the failed state. To recover, please follow the recommended steps below.

## **Recommended Steps**

4 out of 5 customers resolved their configuration update issue using the steps listed below.

* Using Azure PowerShell try executing the [Get Application Gateway](https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgateway?view=azps-1.7.0) and a [Set Application Gateway](https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgateway?view=azps-1.7.0) commands in sequence and check if it recovers from the Failed state
* If it doesn't recover from the Failed state, proceed with the support ticket