<properties
  pagetitle="Configuring with Azure Active Directory or Office 365"
  service=""
  resource=""
  ms.author="vimalt"
  selfhelptype="Generic"
  supporttopicids="32452997"
  resourcetags=""
  productpesids="15543"
  cloudenvironments="public,fairfax,mooncake,blackforest,ussec,usnat"
  articleid="aad1dbb9-672c-45a1-90cc-fb78d4d5aefd"
  ownershipid="Azure_DevOps_Services" />
# Configuring with Azure Active Directory or Office 365

## Common issues and questions about Azure Active Directory (AD) and Office 365

### Where can I find some general information on how Azure AD integration works with Azure DevOps?
Start with [About accessing your organization via Azure AD](https://docs.microsoft.com/azure/devops/organizations/accounts/access-with-azure-ad?view=azure-devops)

### After connecting to Azure AD, some users are disconnected, but they have matching identities in Azure AD.
[This document explains what to do in this scenario](https://docs.microsoft.com/azure/devops/organizations/accounts/faq-azure-access?view=azure-devops#q-some-users-are-disconnected-but-they-have-matching-identities-in-azure-ad-what-should-i-do)

### I have less than 200 users in my organization. Do I need to contact support before connecting to Azure AD?
Probably not! You will have an opportunity to resolve any user mapping issues during the connection process. If you’ve tried to resolve the mapping issues yourself, but are still seeing issues, you should continue contacting support.

### I have more than 200 users in my organization. Can I connect to Azure AD?
You can still connect on your own, but you should continue contacting support for help with disconnected users

### Why are no identities found when I try to add users from Azure AD to my Azure DevOps Organization? 
Are you an Azure AD guest user? [Azure AD guests can't search the Azure AD in the manner required by Azure DevOps](https://docs.microsoft.com/azure/devops/organizations/accounts/faq-azure-access?view=azure-devops#q-why-are-no-identities-found-when-i-try-to-add-users-from-azure-ad-to-my-azure-devops-organization).<br>


* For service impacting issues, see [Azure DevOps Services Status](https://status.dev.azure.com)
* Want a quicker answer to common questions and issues? Try the [Azure DevOps Virtual Agent](https://azuredevopsvirtualagent.azurewebsites.net/)

## **Recommended Documents**

* For general information, start with [About accessing your organization via Azure AD](https://docs.microsoft.com/azure/devops/organizations/accounts/access-with-azure-ad?view=azure-devops)
* [Connect your organization to Azure Active Directory](https://docs.microsoft.com/azure/devops/organizations/accounts/connect-organization-to-azure-ad?view=azure-devops)
* [Disconnect your organization from Azure Active Directory](https://docs.microsoft.com/azure/devops/organizations/accounts/disconnect-organization-from-azure-ad?view=azure-devops)
* [Change your organization connection to another Azure AD](https://docs.microsoft.com/azure/devops/organizations/accounts/change-azure-ad-connection?view=azure-devops)
* [Get list of organizations backed by Azure AD](https://docs.microsoft.com/azure/devops/organizations/accounts/get-list-of-organizations-connected-to-azure-active-directory?view=azure-devops)

### **FAQs**
* [Access via Azure AD FAQs](https://docs.microsoft.com/azure/devops/organizations/accounts/faq-azure-access?view=azure-devops#faq-connect)

### **Additional resources**
* For service impacting issues, see [Azure DevOps Services Status](https://status.dev.azure.com)
* Want a quicker answer? For quick answers to common questions and issues, try the [Azure DevOps Virtual Agent](https://azuredevopsvirtualagent.azurewebsites.net/)
