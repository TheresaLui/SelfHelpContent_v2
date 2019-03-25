<properties
    pageTitle="Test Azure Stack"
    description="Using the Test-AzureStack command to check the health of the stamp"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629270"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public"
    articleId="azurestack-operator-testazurestack"
/>

# Azure Stack Test-AzureStack

 The Azure Stack validation tool **Test-AzureStack** is a PowerShell cmdlet that lets you run a series of tests on your system to identify failures if present.

## **Recommended Steps**

1. Access the privileged endpoint (PEP) for your environment
2. Once connected, run **Test-AzureStack** command, and refer to the [Parameter considerations](https://docs.microsoft.com/azure/azure-stack/azure-stack-diagnostic-test#parameter-considerations) and [Use case examples](https://docs.microsoft.com/azure/azure-stack/azure-stack-diagnostic-test#use-case-examples) details for which parameters to use
3. Before you start installation of an Azure Stack update, [run the validation tool to test system readiness](https://docs.microsoft.com/azure/azure-stack/azure-stack-diagnostic-test#run-validation-tool-to-test-system-readiness-before-installing-update-or-hotfix) before applying the update or hotfix
    - Starting with 1902 Update, operators can now simply use `Test-AzureStack -Group UpdateReadiness`

## **Recommended Documents**

- [The Azure Stack validation tool (Test-AzureStack)](https://docs.microsoft.com/azure/azure-stack/azure-stack-diagnostic-test)
- [Azure Stack Troubleshooting](https://docs.microsoft.com/azure/azure-stack/azure-stack-troubleshooting)