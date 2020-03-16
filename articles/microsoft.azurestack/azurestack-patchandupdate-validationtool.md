<properties
    pageTitle="Precheck questions or Test-AzureStack failures"
    description="Precheck questions or Test-AzureStack failures"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmit"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629240"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public, Fairfax"
    articleId="abdc2tg3-706d-401c-b984-f996c12frf9f"
	ownershipId="ASEP_ContentService_Placeholder"
/>

# Azure Stack validation tool

Before applying an Azure Stack update, make sure you have applied all required hotfixes, security patches, and OEM updates, validated the health of your Azure Stack instance, checked the available capacity, and reviewed the update package.

The [Test-AzureStack validation tool](https://docs.microsoft.com/azure-stack/operator/azure-stack-diagnostic-test) also lets you run a series of tests on your system to identify failures if present, prior to applying an Azure Stack update.
Using the [UpdateReadiness group](https://docs.microsoft.com/azure-stack/operator/azure-stack-diagnostic-test#groups), warnings are displayed as errors in the console output, and should be considered as blockers for the update.

## **Recommended Steps**

1. Ensure you have applied all the required hotfixes, security patches, and OEM updates listed in the update release notes, available from the [list of update packages](https://docs.microsoft.com/azure-stack/operator/azure-stack-servicing-policy#update-package-release-cadence)
2. Review all known issues for the Azure Stack Update you are planning to apply
3. Review active alerts in the Azure Stack Admin Portal, and resolve any that require action
4. Run [Test-AzureStack](https://docs.microsoft.com/azure-stack/operator/azure-stack-diagnostic-test) with  [UpdateReadiness group](https://docs.microsoft.com/azure-stack/operator/azure-stack-diagnostic-test#groups) to validate the status of your Azure Stack and resolve any operational issues before applying an update: `Test-AzureStack -Group UpdateReadiness`

## **Recommended Documents**

* [Test-AzureStack validation tool](https://docs.microsoft.com/azure-stack/operator/azure-stack-diagnostic-test)
* [Validation Tests Available](https://docs.microsoft.com/azure-stack/operator/azure-stack-diagnostic-test#tests-available)
* [Microsoft Azure Stack troubleshooting](https://docs.microsoft.com/azure-stack/operator/azure-stack-troubleshooting)
