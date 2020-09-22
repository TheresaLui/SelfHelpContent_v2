<properties
    pageTitle="Data Factory detected dataset name with invalid characters"
    description="Invalid Dataset Name Issue"
    infoBubbleText="Data Factory detected dataset name with invalid characters"
    service="microsoft.datafactory"
    resource="factories"
    authors="samiranshah"
    ms.author="samirans"
    displayOrder=""
    articleId="DataFactoryDatasetNameCharInsight"
    diagnosticScenario="DataFactoryDatasetNameCharInsight"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="15613"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_DataFactory"
/>

# Data Factory detected dataset name with invalid characters

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->
Your Data Factory resource <!--$FactoryName-->[FactoryName]<!--/$FactoryName--> has detected run failures that may be caused by an unexpected character in the name of a parameterized dataset. An example dataset name is <!--$Dataset-->[Dataset]<!--/$Dataset-->. An example correlationId is <!--$correlationId-->[correlationId]<!--/$correlationId-->. An example error message is <!--$ErrorMessage-->[ErrorMessage]<!--/$ErrorMessage-->.
<!--/issueDescription-->

## **Recommended Steps**

* Rename your datasets with invalid characters to start with an alphabetic character and only contain alphanumeric characters and underscores
