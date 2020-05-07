<properties
	pageTitle="Agent Registration Failures"
	description="Azure AD Connect Health self help for Agent Registration Failures"
	service="microsoft.aad"
	resource="Microsoft_Azure_ADHybridHealth"
	authors="zhiweiw"
	ms.author="zhiweiw"
	displayOrder="100"
	supportTopicIds="32629815"
	productPesIds="16577"
	selfHelpType="resource"
	cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	articleId="1c687109-a9f5-46b8-9de6-fc133a6e73f3"
	ownershipId="AzureIdentity_ComplianceAndReporting"
/>
# Azure AD Connect Health self help for Agent Registration Failures

## **Recommended Steps**

1.	Ensure you are authorized to perform the operation. Global Admins have access by default. Additionally, you can use [Role Based Access Control](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-health-operations#manage-access-with-role-based-access-control) to delegate registration permission to Contributor.
2.	Ensure the required endpoints are enabled, and not blocked due to firewall. See [requirements](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-health-agent-install#requirements) section for details. 
3.	Registration can fail due to outbound communication being subjected to SSL inspection by the network layer

## **Recommended Documents**

* [Common installation questions](https://docs.microsoft.com/azure/active-directory/hybrid/reference-connect-health-faq#installation-questions)
