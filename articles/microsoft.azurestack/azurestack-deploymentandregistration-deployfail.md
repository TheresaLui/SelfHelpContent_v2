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
    cloudEnvironments="public"
    articleId="azurestack-deployment-failure"
/>

# Azure Stack Deployment Failure

## **Recommended Steps**

1. If you experience a failure during installation, you can restart the deployment from the failed step by using the -Rerun option of the deployment script
2. Check for issues in the [Known issues: Deployment](https://docs.microsoft.com/azure/azure-stack/azure-stack-troubleshooting#deployment) article
3. Check Azure Stack [Release Notes](https://docs.microsoft.com/azure/azure-stack/azure-stack-servicing-policy#update-package-release-cadence) to check any late breaking changes or known issues that may be causing your installation failure
4. For a partially-completed deployment, validate the status of your Azure Stack by [running **Test-AzureStack**](https://docs.microsoft.com/azure/azure-stack/azure-stack-diagnostic-test) from the privileged endpoint
5. Check Azure Stack logs using the [Azure Stack log collection tool](https://docs.microsoft.com/azure/azure-stack/azure-stack-diagnostics#log-collection-tool)

## **Recommended Documents**

* [Azure connected Azure Stack deployment decisions](https://docs.microsoft.com/azure/azure-stack/azure-stack-connected-deployment)<br>
* [Azure disconnected Azure Stack deployment decisions](https://docs.microsoft.com/azure/azure-stack/azure-stack-disconnected-deployment)<br>
* [About deployment network traffic](https://docs.microsoft.com/azure/azure-stack/deployment-networking)<br>
* [Microsoft Azure Stack troubleshooting](https://docs.microsoft.com/azure/azure-stack/azure-stack-troubleshooting)<br>
* [Azure Stack servicing policy](https://docs.microsoft.com/azure/azure-stack/azure-stack-servicing-policy#update-package-release-cadence)
