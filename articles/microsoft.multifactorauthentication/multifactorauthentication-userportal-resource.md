<properties
	pageTitle="MFA Server (On-premises)/User portal"
	description="MFA Server (On-premises)/User portal"
	service="microsoft.aad"
	resource="Microsoft_AAD_IAM"
	authors="kgremban"
	displayOrder="220"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="mfa_overview"
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="d05af26c-effe-4dd8-9914-9047d4f785f4"
	ownershipId="AzureIdentity_User"
/>

# Troubleshoot the user portal and mobile app web service

## **Recommended steps**

If you're troubleshooting the user portal, test it by browsing to the web service SDK (like https://hostname/MultiFactorAuthWebServiceSdk/PfWsSdk.asmx). If the page loads, then everything is working. If not, one of the following configuration problems may apply to you.

If you're troubleshooting the mobile app web service, test it by browsing to the PfPaWs URL (like https://hostname/pa/PfPaWs.asmx). Click the **TestPfWsSdkConnection** link, then **Invoke**. If you get a success message, then everything is working. If not, one of the following configuration problems may apply to you:

1. The username or password is incorrect.
2. The PfWsSdk URL in the PfPaWs web.config file is incorrect or not reachable.
3. The hostname of the PfWsSdk URL in the PfPaWs web.config file is incorrect or not reachable.
4. The connection to PfWsSdk is successful, but that PfWsSdk cannot connect to the MultiFactorAuth service.

## **Recommended documents**

- [Deploy the user portal for the Azure Multi-Factor Authentication Server](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started-portal)  
- [Enable mobile app authentication with Azure Multi-Factor Authentication Server](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started-server-webservice)  
