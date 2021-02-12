<properties
    pageTitle="Run Azure Stack validation tool to identify failures"
    description="Run Azure Stack validation tool to identify failures"
    service="microsoft.azurestack"
    resource="registrations"
    authors="TobyTu"
    ms.author="mquian"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629270"
    resourceTags=""
    productPesIds="16226, 17058, 17131, 17057"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="ebdc3983-705d-401c-b984-f433c12f1e9f"
	ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# Identify failures by using Azure Stack validation tool

## **Recommended Steps**

* Run the [validation tool](https://docs.microsoft.com/azure-stack/operator/azure-stack-diagnostic-test) (Test-AzureStack) and resolve identified issues
* If Test-AzureStack output says to run the -Repair option to remediate an inaccessible VM, you can include the role name listed in the output, but only for the AsScaleUnitResources, AzsInfraRoleSummary, or AzsPortalAPISummary roles and only if no other update is in progress.


## **Recommended Documents**

* [Azure Stack Recent Updates and Release Notes](https://docs.microsoft.com/azure-stack/operator/azure-stack-servicing-policy#update-package-release-cadence)
