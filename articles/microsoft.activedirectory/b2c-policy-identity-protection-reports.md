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

Azure Active Directory B2C (Azure AD B2C) provides support for verifying a phone number by using Azure AD Multi-Factor Authentication (MFA). Review these [Steps to define an Azure AD MFA technical profile ](https://docs.microsoft.com/azure/active-directory-b2c/multi-factor-auth-technical-profile).  


### **Can I use Conditional Access Policies for my Azure Active Directory B2C tenant?** 

Yes, you can create Conditional Access policies that use these risk detections to determine actions and enforce organizational policies. [Set up Identity Protection and Conditional Access for Azure AD B2C](https://docs.microsoft.com/azure/active-directory-b2c/conditional-access-identity-protection-setup).

### **Can I integrate Conditional Access with user flows and custom policies?** 

[Learn how to Add Conditional Access to custom policy in Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/conditional-access-user-flow?pivots=b2c-custom-policy). 


### **Identity Protection dashboard**
Your investigation into risk will typically start with the Identity Protection dashboard. <br>
The dashboard gives you access to:<br>

* Reports such as [Risky users](https://docs.microsoft.com/azure/active-directory/identity-protection/howto-identity-protection-investigate-risk?WT.mc_id=Portal-Microsoft_Azure_Support#risky-users), [Risky sign-ins](https://docs.microsoft.com/azure/active-directory/identity-protection/howto-identity-protection-investigate-risk?WT.mc_id=Portal-Microsoft_Azure_Support#risky-sign-ins), and [Risk detections](https://docs.microsoft.com/azure/active-directory/identity-protection/howto-identity-protection-investigate-risk?WT.mc_id=Portal-Microsoft_Azure_Support#risk-detections)

* Configuration settings for your Security Policies, [Notifications](https://docs.microsoft.com/azure/active-directory/identity-protection/howto-identity-protection-configure-notifications?WT.mc_id=Portal-Microsoft_Azure_Support), and [multi-factor authentication registration](https://docs.microsoft.com/azure/active-directory/identity-protection/howto-identity-protection-configure-mfa-policy?WT.mc_id=Portal-Microsoft_Azure_Support)

In addition to investigation, you can configure an automated response for specific sign-in risk levels through the [sign-in risk policy](https://docs.microsoft.com/azure/active-directory-b2c/conditional-access-identity-protection-setup#to-create-a-conditional-access-policy). In your response, you can block access to your resources or require passing a [multi-factor authentication (MFA) challenge](https://docs.microsoft.com/azure/active-directory/identity-protection/howto-identity-protection-configure-mfa-policy?WT.mc_id=Portal-Microsoft_Azure_Support) to gain access.


### **Useful Links** 

* [Set up Identity Protection and Conditional Access in Azure AD B2C](https://docs.microsoft.com/azure/active-directory-b2c/conditional-access-identity-protection-setup) to provide ongoing risk detection for your Azure AD B2C tenant. 

* Learn [best practices and recommendations](https://docs.microsoft.com/azure/active-directory-b2c/best-practices) for integrating Azure AD B2C into existing or new application environments.  

* Review [Frequently asked questions](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-faqs) about the Azure Active Directory B2C. 

* Ask your question to our developer community at  [Stack Overflow](http://stackoverflow.com/questions/tagged/azure-ad-b2c).
