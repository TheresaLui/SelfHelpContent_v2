<properties
    pageTitle="Azure Stack Hub hardware"
    description="General Azure Stack Hub hardware issues that do not fit storage or networking"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629221,32629256,32630573,32629220"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="a32f2a3c-f0bb-4fbf-bf17-4ad15f6ffe7b"
	ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# Azure Stack Hub Hardware Issues

**NOTE**: Before you create a support ticket, review [**Release notes**](https://docs.microsoft.com/azure-stack/operator/release-notes) and [**Known issues**](https://docs.microsoft.com/azure-stack/operator/known-issues) for the update you are applying (choose from the Version drop-down menu). This may save you time and effort.

## **Recommended Steps**

The Administrator portal shows the status of a scale unit and associated nodes, and how to use the available node actions to power on, power off, drain, resume, and repair. Typically, you use these node actions during field replacement of parts, or for node recovery scenarios.

To view the status of a scale unit:

1. On the **Region Management** tile, select the **Region**
2. Under **Infrastructure Resources**, select **Scale Units**
3. In the results, select the **Scale Unit** to view the current status

See your vendor’s field replaceable unit (FRU) documentation for detailed steps that are specific to your Azure Stack integrated system.

## **Recommended Documents**

* [Scale unit node actions in Azure Stack Hub](https://docs.microsoft.com/azure/azure-stack/azure-stack-node-actions)
* [Replace a hardware component on an Azure Stack Hub scale unit node](https://docs.microsoft.com/azure/azure-stack/azure-stack-replace-component)
