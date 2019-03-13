<properties
    pageTitle="Azure Stack Deployment Failure"
    description="Azure Stack Deployment Failure"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629194,32629205"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public"
    articleId="azurestack-deployment-failure"
/>

# Azure Stack installation failure

If you experience a failure during installation, you can restart the deployment from the failed step by using the -rerun option of the deployment script.<br>

## **Recommended steps**

1. If you experience a failure during installation, you can restart the deployment from the failed step by using the -rerun option of the deployment script.<br>
2. If at the end of ASDK deployment, the PowerShell session is still open and doesn’t show any output, follow the instruction in the [Known issues](https://docs.microsoft.com/azure/azure-stack/azure-stack-troubleshooting) article. <br>
3. Check the [release notes](https://docs.microsoft.com/azure/azure-stack/azure-stack-servicing-policy#update-package-release-cadence) for any late breaking changes, known issues, hotfixes, or other actions you need to take that may be causing your installation failure.<br>
4. Review the logs to see if you can identify the issue. For instructions, see [Azure Stack diagnostics tools](https://docs.microsoft.com/azure-stack/azure-stack-diagnostics).<br>
5. If you can, validate the status of your Azure Stack by running **Test-AzureStack** from the privileged endpoint. For instructions, see [Run Test-AzureStack](https://docs.microsoft.com/azure/azure-stack/azure-stack-diagnostic-test).<br>

## **Recommended documents**

[Azure Stack servicing policy](https://docs.microsoft.com/azure/azure-stack/azure-stack-servicing-policy#update-package-release-cadence)<br>
[Microsoft Azure Stack troubleshooting](https://docs.microsoft.com/azure/azure-stack/azure-stack-troubleshooting)