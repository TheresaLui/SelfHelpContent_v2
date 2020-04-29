<properties
    pageTitle="Azure Stack hardware"
    description="General Azure Stack hardware issues that do not fit storage or networking"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629237,32629221,32629256,32630573,32629220"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="a32f2a3c-f0bb-4fbf-bf17-4ad15f6ffe7b"
	ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# Azure Stack Hardware Issues

## **Known Issue**

After applying the 2002 update, an alert for an "Invalid Time Source" may incorrectly appear in the Administrator portal. This false-positive alert can be ignored and will be fixed in an upcoming release. For more information, see [Azure Stack Hub known issues](https://docs.microsoft.com/azure-stack/operator/known-issues?view=azs-2002).  

## **Recommended Steps**

The Administrator portal shows the status of a scale unit and associated nodes, and how to use the available node actions to power on, power off, drain, resume, and repair. Typically, you use these node actions during field replacement of parts, or for node recovery scenarios.

To view the status of a scale unit:

1. On the **Region Management** tile, select the **Region**
2. Under **Infrastructure Resources**, select **Scale Units**
3. In the results, select the **Scale Unit** to view the current status

See your vendor’s field replaceable unit (FRU) documentation for detailed steps that are specific to your Azure Stack integrated system.

## **Recommended Documents**

* [Scale unit node actions in Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-node-actions)
* [Replace a hardware component on an Azure Stack scale unit node](https://docs.microsoft.com/azure/azure-stack/azure-stack-replace-component)
