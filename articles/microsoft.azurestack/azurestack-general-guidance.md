<properties
    pageTitle="Azure Stack General Guidance"
    description=""
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629177,32629175"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public"
    articleId="azurestack-general-guidance"
/>

# Troubleshooting Azure Stack

The first step in troubleshooting Azure Stack is to review any known issues for troubleshooting Azure Stack components such as deployment, virtual machines, and storage.

Azure Stack is a large collection of components working together and interacting with each other. All these components generate their own unique logs. This can make diagnosing issues a challenging task, especially for errors coming from multiple, interacting Azure Stack components. The Azure Stack diagnostics tools help ensure the log collection mechanism is easy and efficient.

You can validate the status of your Azure Stack. When you have an issue, contact Microsoft Customer Services Support. Support asks you to run Test-AzureStack from your management node. The validation test isolates the failure. Support can then analyze the detailed logs, focus on the area where the error occurred, and work with you in resolving the issue.

## **Recommended steps**

1. Review troubleshooting known issues.
2. Use trace collector and the log collection tool to college log files.
3. Validate your Azure Stack deployment using the Run Test-AzureStack cmdlet.

## **Recommended documents**

[Azure Stack known issues](https://docs.microsoft.com/azure/azure-stack/azure-stack-troubleshooting)<br>
[Azure Stack diagnostics tools](https://docs.microsoft.com/azure/azure-stack/azure-stack-diagnostics)<br>
[Validation for Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-diagnostic-test)