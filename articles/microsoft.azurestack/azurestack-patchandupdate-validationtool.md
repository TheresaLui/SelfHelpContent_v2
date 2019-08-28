<properties
    pageTitle="Register a disconnected Azure Stack"
    description="Register a disconnected Azure Stack"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="TobyTu"
    ms.author="mquian"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629240"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public"
    articleId="abdc2tg3-706d-401c-b984-f996c12frf9f"
/>

# Azure Stack validation tool

As an Azure Stack operator, being able to determine the health and status of your system on-demand is essential. The Azure Stack validation tool (Test-AzureStack) is a PowerShell cadet that lets you run a series of tests on your system to identify failures if present. You will typically be asked to run this tool through the [privileged end point (PEP)](https://docs.microsoft.com/azure-stack/operator/azure-stack-privileged-endpoint) when you contact Microsoft Customer Services Support (CSS) with an issue. With the system-wide health and status information at hand, CSS can collect and analyze detailed logs, focus on the area where the error occurred, and work with you to resolve the issue.

## **Recommended Documents**

* [Microsoft Azure Stack troubleshooting](https://docs.microsoft.com/azure-stack/operator/azure-stack-troubleshooting)
* [Tests available](https://docs.microsoft.com/azure-stack/operator/azure-stack-diagnostic-test#tests-available)
