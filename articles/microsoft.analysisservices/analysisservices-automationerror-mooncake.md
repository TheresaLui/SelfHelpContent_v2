<properties
    pageTitle="Azure automation error when processing AS server"
    description="Azure automation error when processing AS server"
    service="microsoft.analysisservices"
    resource="servers"
    authors="brspie"
    ms.author="chanwa"
    displayOrder="5"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="MoonCake"
    articleId="a0c2491d-b029-4a60-9be6-62da57229b00"
    ownershipId="AzureData_AnalysisServices"
/>

# Azure automation error when processing AS server

## **Recommended Steps**

1. If you see an error such as **Invoke-ProcessASDatabase : Exception has been thrown by the target of an invocation.** Check the credentials used to run AS commands. It should not be an MFA (multi-factor authentication) account - try another account without interactive requirements.

2. If you see an error such as **Add-AzureAsAccount : unknown_user_type** The account name of the credential should not contain any special characters. Try another account without special characters.

## **Recommended Documents**

* [Reference](https://social.msdn.microsoft.com/Forums/en-US/a4f5ac38-db33-4082-a3de-b4b8d501b35a/addazureaccount-unknownusertype?forum=azureautomation)

* [Automating Azure Analysis Services](https://blogs.msdn.microsoft.com/dataaccesstechnologies/2017/09/01/automating-azure-analysis-service-processing-using-azure-automation-account/)
