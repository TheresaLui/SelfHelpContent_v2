<properties
    pageTitle="Stored Procedure Common Solutions"
    description="Stored Procedure Common Solutions"
    service=""
    resource=""
    authors="jaserano, v-miegge"
    ms.author="jaserano"
    authorAlias="jaserano"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32680904"
    resourceTags=""
    productPesIds="15613"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="d7bb0bbe-5679-4c5d-b4a7-d22ea545bbf6"
    ownershipId="AzureData_DataFactory"
/>

# Stored Procedure Common Solutions

## **Recommended Steps**

When a stored procedure fails and returns error details, you can't capture the error info directly in the activity output. However, Data Factory pumps all of its activity run events to Azure Monitor. Among the events that Data Factory pumps to Azure Monitor, it pushes error details there. You can, for example, set up email alerts from those events. For more info, see [Alert and Monitor data factories using Azure Monitor](https://docs.microsoft.com/azure/data-factory/monitor-using-azure-monitor).

## **Recommended Documents**

- [Stored Procedure Activity in Azure Data Factory](https://docs.microsoft.com/azure/data-factory/transform-data-using-stored-procedure)
