<properties
	pageTitle="Azure automation error when processing AS server"
	description="Azure automation error when processing AS server"
	service="microsoft.analysisservices"
	resource="servers"
	authors="bnmaa"
	displayOrder="5"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="MoonCake"
/>

# Azure automation error when processing AS server

## **Recommended steps**
1. If you see an error like **Invoke-ProcessASDatabase : Exception has been thrown by the target of an invocation.** <br />
    Check the credentials used to run AS commands, it shouldn't be an MFA (multi-factor authentication) account, try another account without interactive requirements.
2. If you see an error like **Add-AzureAsAccount : unknown_user_type** <br />
    The account name of the credential shouldn't contain any special characters.  Try another account without special characters. [(reference)](https://social.msdn.microsoft.com/Forums/en-US/a4f5ac38-db33-4082-a3de-b4b8d501b35a/addazureaccount-unknownusertype?forum=azureautomation)

## **Recommended documents**
[Automating Azure Analysis Services](https://blogs.msdn.microsoft.com/dataaccesstechnologies/2017/09/01/automating-azure-analysis-service-processing-using-azure-automation-account/)
