<properties
  pagetitle="Configuring with Azure Active Directory or Office 365"
  service=""
  resource=""
  ms.author="vimalt,cathmill"
  selfhelptype="Generic"
  supporttopicids="32452997"
  resourcetags=""
  productpesids="15543"
  cloudenvironments="public,fairfax,mooncake,blackforest,ussec,usnat"
  articleid="aad1dbb9-672c-45a1-90cc-fb78d4d5aefd"
  ownershipid="Azure_DevOps_Services" />
# Configuring with Azure Active Directory or Office 365

## Common issues and questions about Azure Active Directory (AD) and Office 365

* **Where can I find general information on how Azure AD integration works with Azure DevOps?**<br>
Start with [accessing your organization via Azure AD](https://docs.microsoft.com/azure/devops/organizations/accounts/access-with-azure-ad?view=azure-devops)

* **After connecting to Azure AD, some users are disconnected, but they have matching identities in Azure AD.**<br>
See [this document](https://docs.microsoft.com/azure/devops/organizations/accounts/faq-azure-access?view=azure-devops#q-some-users-are-disconnected-but-they-have-matching-identities-in-azure-ad-what-should-i-do) for guidance on what to do in this scenario.

* **I have less than 200 users in my organization. Do I need to contact support before connecting to Azure AD?**<br>
Probably not. You'll have an opportunity to resolve any user mapping issues during the connection process. If you’ve tried to resolve the mapping issues yourself, but are still seeing issues, start a support ticket.

* **I have more than 200 users in my organization. Can I connect to Azure AD?**<br>
You can still connect on your own, but you should continue contacting support for help with disconnected users

* **Why are no identities found when I try to add users from Azure AD to my Azure DevOps Organization?** <br>
Are you an Azure AD guest user? See details about why [Azure AD guests can't search the Azure AD in the manner required by Azure DevOps](https://docs.microsoft.com/azure/devops/organizations/accounts/faq-azure-access?view=azure-devops#q-why-are-no-identities-found-when-i-try-to-add-users-from-azure-ad-to-my-azure-devops-organization).

## **Recommended Documents**

* [Connect your organization to Azure Active Directory](https://docs.microsoft.com/azure/devops/organizations/accounts/connect-organization-to-azure-ad?view=azure-devops)
* [Disconnect your organization from Azure Active Directory](https://docs.microsoft.com/azure/devops/organizations/accounts/disconnect-organization-from-azure-ad?view=azure-devops)
* [Change your organization connection to another Azure AD](https://docs.microsoft.com/azure/devops/organizations/accounts/change-azure-ad-connection?view=azure-devops)
* [Get list of organizations backed by Azure AD](https://docs.microsoft.com/azure/devops/organizations/accounts/get-list-of-organizations-connected-to-azure-active-directory?view=azure-devops)
* [Access via Azure AD FAQs](https://docs.microsoft.com/azure/devops/organizations/accounts/faq-azure-access?view=azure-devops#faq-connect)
* For service impacting issues, see [Azure DevOps Services Status](https://status.dev.azure.com)
* For quick answers to common questions and issues, try the [Azure DevOps Virtual Agent](https://azuredevopsvirtualagent.azurewebsites.net/)
