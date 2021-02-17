<properties
  pagetitle="Business to Consumer (B2C)"
  service=""
  resource=""
  ms.author="nishring"
  selfhelptype="Generic"
  supporttopicids="32781154"
  resourcetags=""
  productpesids="16580"
  cloudenvironments="public,fairfax,mooncake,usnat,ussec,blackforest"
  disableclouds=""
  articleid="aa71078e-2b8a-4f9a-bdda-8b4ef19c781b"
  ownershipid="AzureIdentity_B2C" />
# Business to Consumer (B2C)

## **Recommended Steps**

### **Enable multi-factor authentication in Azure Active Directory B2C** 

Azure Active Directory B2C (Azure AD B2C) integrates directly with Azure AD Multi-Factor Authentication so that you can add a second layer of security to sign-up and sign-in experiences in your applications. You can enable multi-factor authentication without writing a single line of code. See [Steps to enable multi-factor authentication](https://docs.microsoft.com/azure/active-directory-b2c/multi-factor-authentication?pivots=b2c-custom-policy). 

### **Can I send customized email to users that sign up to use my applications?** 

Yes, you can use the company branding feature to customize the content of verification emails. [Learn how elements of the email can be customized](https://docs.microsoft.com/azure/active-directory-b2c/faq?tabs=app-reg-ga#how-do-i-customize-verification-emails-the-content-and-the-from-field-sent-by-azure-ad-b2c). 

Also, by using **DisplayControls** (currently in preview) and the third-party email provider [SendGrid](https://docs.microsoft.com/azure/active-directory-b2c/custom-email-sendgrid) or [Mailjet](https://docs.microsoft.com/azure/active-directory-b2c/custom-email-mailjet), you can use your own email template and **From:** address and subject, as well as support localization and custom One-Time Password (OTP) settings. 

### **For my customers, can I generate and send a code to a phone number, and then verify the code?** 

Azure Active Directory B2C (Azure AD B2C) provides support for verifying a phone number by using Azure AD Multi-Factor Authentication (MFA). Review these [Steps to define an Azure AD MFA technical profile](https://docs.microsoft.com/azure/active-directory-b2c/multi-factor-auth-technical-profile).  

### **Conditional Access in B2C requires the configuration of two elements**
1. **User flow.** Must use next generation user flows which support Conditional Access policies. These are labelled as **recommended**.

2. **Conditional Access policy.** [Create a Conditional Access policy](https://docs.microsoft.com/azure/active-directory-b2c/conditional-access-identity-protection-setup) and specify the apps and users in scope for the policy.

When using custom policies, you must refer to the [github sample](https://github.com/azure-ad-b2c/samples/tree/master/policies/conditional-access).

### **How can I test my Conditional Access policy?**  
For testing, reduce the scope of the conditional access policy to one AAD B2C user and one AAD B2C application.  Create a next generation user flow (recommended), making sure that the conditional access box is selected (default).  Use Run Now to test your policy under various situations.

#### **Is report only mode supported?**
Yes

### **How can I tell if the CA policy was active for a given authentication?**
Conditional Access policy activity is reported here: In your B2C tenant, Audit logs., Service: B2C, Category: Identity Protection. Look for Evaluate ….. and  Remediate response. 

### **How can I choose between an MFA with TXT or MFA with email?**

Learn about it at [Resilient end-user experience](https://docs.microsoft.com/azure/active-directory/fundamentals/resilient-end-user-experience)
 

### **Identity Protection**

Your investigation into risk will often include:
* Reports such as [Risky users](https://docs.microsoft.coms/azure/active-directory/identity-protection/howto-identity-protection-investigate-risk?WT.mc_id=Portal-Microsoft_Azure_Support#risky-users) and [Risk detections](https://docs.microsoft.com/azure/active-directory/identity-protection/howto-identity-protection-investigate-risk?WT.mc_id=Portal-Microsoft_Azure_Support#risk-detections)

* Sign-in events in the [B2C Audit Logs](https://docs.microsoft.com//azure/active-directory-b2c/view-audit-logs)

* Configuration settings for your [technical profiles, user flows, custom policies](https://docs.microsoft.com/azure/active-directory-b2c/conditional-access-technical-profile)

* Configuration settings for your Conditional Access policies


### **Useful Links** 

* [Set up Identity Protection and Conditional Access in Azure AD B2C](https://docs.microsoft.com/azure/active-directory-b2c/conditional-access-identity-protection-setup) to provide ongoing risk detection for your Azure AD B2C tenant. 

* [What is risk?](https://docs.microsoft.com/azure/active-directory/identity-protection/concept-identity-protection-risks)

* [Identity Protection policies](https://docs.microsoft.com/azure/active-directory/identity-protection/concept-identity-protection-policies)

* Review [Frequently asked questions](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-faqs) about the Azure Active Directory B2C. 

* Ask your question to our developer community at  [Stack Overflow](http://stackoverflow.com/questions/tagged/azure-ad-b2c).