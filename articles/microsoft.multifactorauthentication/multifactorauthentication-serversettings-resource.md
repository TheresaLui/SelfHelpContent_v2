<properties
  pageTitle="MFA Server (On-Premises)/MFA server settings configuration"
  description="MFA server settings configuration"
  service="microsoft.aad"
  resource="Microsoft_AAD_IAM"
  authors="kgremban"
  displayOrder="210"
  selfHelpType="resource"
  supportTopicIds=""
  resourceTags="mfa_overview"
  productPesIds=""
  cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="f8d7255a-bb40-42bc-93a5-741b7e4fd8dc"
	ownershipId="AzureIdentity_User"
/>

# Problems with Azure MFA Server settings

## **Recommended steps**

1. In the Company Settings section you can change the default settings for a user who is imported and/or added. Note: some settings can be overwritten in other configuration items such as the directory synchronization item. It’s important to note this will change the settings for new users, it will not change anything for users who are already created. You would need to go to Users to change those users.

2. You can customize the text for the SMS messages and/or Mobile App text for each language in the Company Settings section.

3. Limit the data sent to the Azure MFA Backend for reporting purposes in the Reports tab of the Company Settings section of the MFA Server.

## **Recommended documents** 

- [Getting started with the Azure Multi-Factor Authentication Server](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started-server)  
- [Configure Azure Multi-Factor Authentication Settings](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-whats-next)  
- [Upgrade to the latest Azure Multi-Factor Authentication Server](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-server-upgrade) 