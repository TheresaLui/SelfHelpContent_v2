<properties
  pagetitle="Business to Consumer (B2C)&#xD;"
  service=""
  resource=""
  ms.author="nishring"
  selfhelptype="Generic"
  supporttopicids="32633325"
  resourcetags=""
  productpesids="16580"
  cloudenvironments="public,fairfax,mooncake,usnat,ussec,blackforest"
  disableclouds=""
  articleid="f0b113de-55b2-4697-b731-9928eea85c8d"
  ownershipid="AzureIdentity_B2C" />
# Business to Consumer (B2C)

## **Recommended Steps**

### **How can I diagnose problems with my custom policies?**
Application Insights provides a way to diagnose exceptions and visualize application performance issues. Azure AD B2C includes a feature for sending data to Application Insights. Learn how to [Collect Azure Active Directory B2C logs with Application Insights](https://docs.microsoft.com/azure/active-directory-b2c/troubleshoot-with-application-insights#set-up-application-insights).

The community has developed a user journey viewer to help identity developers. It reads from your Application Insights instance and provides a well-structured view of the user journey events. You obtain the source code and deploy it in your own solution.

Find the version of the viewer that reads events from Application Insights on GitHub here: [Azure-Samples/active-directory-b2c-advanced-policies](https://github.com/Azure-Samples/active-directory-b2c-advanced-policies/tree/master/wingtipgamesb2c/src/WingTipUserJourneyPlayerWebApplication).

### **Useful Links**
* Custom policies are fully edited configuration files that define the behavior of your Azure AD B2C tenant. Get started today by [creating a Custom Policy](https://docs.microsoft.com/azure/active-directory-b2c/custom-policy-overview).
* Check our sample on [how to run web tests and monitor results of B2C sign in's, using Azure Application Insights](https://github.com/azure-ad-b2c/samples/tree/master/policies/signin-webtest)
* Learn [best practices and recommendations](https://docs.microsoft.com/azure/active-directory-b2c/best-practices?WT.mc_id=Portal-Microsoft_Azure_Support) for integrating Azure AD B2C into existing or new application environments
* Post your question on [Microsoft Q&A](https://docs.microsoft.com/answers/topics/azure-ad-b2c.html) using the tag `azure-ad-b2c`
