<properties
    pageTitle="Azure Stack Deployment Failure"
    description="Azure Stack Deployment Failure"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629194"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="azurestack-deployment-failure"
	ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# Azure Stack Deployment Failure

Before deployment starts, there are some [minimum requirements](https://docs.microsoft.com/azure-stack/operator/deployment-networking#deployment-requirements) that can be validated by your OEM to ensure deployment completes successfully, including:

* Certificates
* Azure subscription
* Required Internet access and endpoints
* DNS
* NTP

**Please note:** If your deployment issue is related to an add-on resource provider like AppServices, SQL or MySQL, please go back and choose the corresponding topic under *Add-on Resource Providers and Marketplace*.

## **Recommended Steps**

1. Use the Azure Stack Readiness Checker tool ([AzsReadinessChecker](https://docs.microsoft.com/azure-stack/operator/azure-stack-validate-registration)) to validate that your Azure subscription is ready to use with Azure Stack before you begin an Azure Stack deployment
2. Ensure that the customer network permits all inbound and outbound [ports and protocols used by Azure Stack endpoints](https://docs.microsoft.com/azure-stack/operator/azure-stack-integrate-endpoints)
    * Azure Stack supports only transparent proxy servers
    * [SSL traffic interception is not supported](https://docs.microsoft.com/azure-stack/operator/azure-stack-firewall#ssl-interception) and can lead to service failures when accessing endpoints
    * The deployment VM (DVM) has special requirements listed under [Deployment network traffic
](https://docs.microsoft.com/azure-stack/operator/deployment-networking#deployment-network-traffic)
3. Check Azure Stack [Release Notes](https://docs.microsoft.com/azure-stack/operator/release-notes) and [Known Issues](https://docs.microsoft.com/azure-stack/operator/known-issues) for any late breaking changes or known issues that may be causing the deployment failure
4. For a partially-completed deployment, validate the status of your Azure Stack by running the [Test-AzureStack validation tool](https://docs.microsoft.com/azure/azure-stack/azure-stack-diagnostic-test) from the privileged endpoint, and check Azure Stack logs using the [Azure Stack log collection tool](https://docs.microsoft.com/azure/azure-stack/azure-stack-diagnostics#log-collection-tool)
5. After deployment completes, follow steps for [Post-deployment datacenter integration](https://docs.microsoft.com/azure-stack/operator/azure-stack-customer-journey#post-deployment)

## **Recommended Documents**

* [Azure connected Azure Stack deployment decisions](https://docs.microsoft.com/azure/azure-stack/azure-stack-connected-deployment)<br>
* [Azure disconnected Azure Stack deployment decisions](https://docs.microsoft.com/azure/azure-stack/azure-stack-disconnected-deployment)<br>
* [Network integration planning for Azure Stack](https://docs.microsoft.com/azure-stack/operator/azure-stack-network)<br>
* [About deployment network traffic](https://docs.microsoft.com/azure/azure-stack/deployment-networking)<br>
* [Microsoft Azure Stack troubleshooting](https://docs.microsoft.com/azure/azure-stack/azure-stack-troubleshooting)<br>
* [Azure Stack servicing policy](https://docs.microsoft.com/azure/azure-stack/azure-stack-servicing-policy#update-package-release-cadence)
