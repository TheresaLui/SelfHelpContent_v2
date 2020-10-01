<properties 
    pageTitle="Application Gateway frontend private IP address conflict"
    description="Application Gateway frontend private IP address conflict"
    infoBubbleText="Some suggestions have been found to help solve your frontend private IP address conflict issue quicker."
    service="microsoft.network"
    resource="applicationgateways"
    authors="surajmb"
    ms.author="surmb"
    selfHelpType="diagnostics"
    articleId="application-gateway-privateip-conflict-insight"
    diagnosticScenario="ApplicationGatewayPrivateIPConflictError"
    supportTopicIds="32639110,32680756"
	productPesIds="15922"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
 	ownershipId="CloudNet_AzureApplicationGateway"
/>

# Application Gateway frontend private IP address conflict
<!--issueDescription-->
We ran several diagnostics on your resource and have found the below issues that could be the cause of your configuration failure.

## **Issues Identified**

The frontend IP address in user configuration conflicts with an Application Gateway instance's private IP address.

## **Recommended steps**

You can resolve the issue in one of the following ways -

* Option 1 - Delete the existing private frontendIpConfiguration, and create a new one with a different IpAddress from the Azure portal or PowerShell. Note that, to remove the IP configuration, it shouldn't be associated to any listener.

    Using Azure portal -
    1. Navigate to the Frontend IP configurations of your Application Gateway and find the IP configuration with type Private and click to select it
    1. Select delete option on the top
    1. Once it's removed, go back to the Frontend IP configurations blade and click on the Private IP configuration to create a new one
    1. Enter the name and select the "Choose a specific IP address" to enter a non-conflicting IP address, preferably from the end of the subnet address space and click Save
    
    Using Azure PowerShell -
    You can use the [Remove-AzApplicationGatewayFrontendIPConfig](https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayfrontendipconfig) command to remove it.

* Option 2 - [Stop](https://docs.microsoft.com/powershell/module/Az.Network/Stop-AzApplicationGateway) the Application Gateway, create a Listener and RequestRoutingRules with private frontendIpConfig, then [Start](https://docs.microsoft.com/powershell/module/az.network/start-azapplicationgateway) the Application Gateway so that all instance IP addresses are reassigned based on the new configuration.

## **Recommended Documents**

* [Create Application Gateway with private frontend IP configuration using Azure portal](https://docs.microsoft.com/azure/application-gateway/configure-application-gateway-with-private-frontend-ip)
* [Create Application Gateway with private frontend IP configuration using Azure PowerShell](https://docs.microsoft.com/azure/application-gateway/application-gateway-ilb-arm)
* [Stop an Application Gateway](https://docs.microsoft.com/powershell/module/Az.Network/Stop-AzApplicationGateway)
* [Start an Application Gateway](https://docs.microsoft.com/powershell/module/az.network/start-azapplicationgateway)
* [Learn more about Application Gateway frontend IP configuration](https://docs.microsoft.com/azure/application-gateway/configuration-front-end-ip)