<properties
    pageTitle="Copy activity failed due to ADAL service unavailable"
    description="Your copy activity failed with 'ADAL error: service_unavailable, The remote server returned an error: (503) Server Unavailable'."
    infoBubbleText="Your copy activity failed with 'ADAL error: service_unavailable, The remote server returned an error: (503) Server Unavailable'."
    service="microsoft.datafactory"
    resource="factories"
    authors="shelfeng"
    ms.author="shelfeng"
    displayOrder=""
    articleId="DataFactoryADALServiceUnavailableInsight"
    diagnosticScenario="DataFactoryADALServiceUnavailableInsight"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="15613"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_DataFactory"
/>

# Copy activity failed due to ADAL service unavailable'

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->
Your Data Factory resource <!--$FactoryName-->[FactoryName]<!--/$FactoryName--> has detected run failures.  One possible cause is that the Service Token Server (STS) owned by Azure Active Directory is not available.
<!--/issueDescription-->

## **Recommended Steps**

Rerun the copy activity after several minutes.

## **Recommended Documents**

For more information on this error please follow our troubleshooting doc:

* [Troubleshoot Azure Data Factory Connectors](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#error-message-failed-to-get-access-token-by-using-service-principal-adal-error-service_unavailable)
