<properties
  pagetitle="Business to Consumer (B2C)"
  service=""
  resource=""
  ms.author="nishring"
  selfhelptype="Generic"
  supporttopicids="32633320"
  resourcetags=""
  productpesids="16580"
  cloudenvironments="public,fairfax,mooncake,usnat,ussec,blackforest"
  disableclouds=""
  articleid="8c96691c-3571-47b9-8b56-02c76feee40d"
  ownershipid="AzureIdentity_B2C" />
# Business to Consumer (B2C)

## **Recommended Steps**

### **Enable multi-factor authentication in Azure Active Directory B2C** 

Azure Active Directory B2C (AD B2C) integrates directly with Azure AD Multi-Factor Authentication. This allows you to add a second layer of security to the sign-up and sign-in experiences in your applications without writing a single line of code. Review these [Steps to enable multi-factor authentication](https://docs.microsoft.com/azure/active-directory-b2c/multi-factor-authentication?pivots=b2c-custom-policy).


### **Can I send customized email to users that sign up to use my applications?** 

Yes, you can use the company branding feature to customize the content of verification emails. [Learn how elements of the email can be customized](https://docs.microsoft.com/azure/active-directory-b2c/faq?tabs=app-reg-ga#how-do-i-customize-verification-emails-the-content-and-the-from-field-sent-by-azure-ad-b2c). 

Also, by using `DisplayControls` (currently in preview) and the third-party email provider [SendGrid](https://docs.microsoft.com/azure/active-directory-b2c/custom-email-sendgrid) or [Mailjet](https://docs.microsoft.com/azure/active-directory-b2c/custom-email-mailjet), you can use your own email template, From: address, and subject, as well as support localization and custom One-Time Password (OTP) settings. 


### **For my customers, can I generate and send a code to a phone number, and then verify the code?** 

Azure Active Directory B2C (Azure AD B2C) provides support for verifying a phone number by using Azure AD Multi-Factor Authentication (MFA). Review [Steps to define an Azure AD MFA technical profile ](https://docs.microsoft.com/azure/active-directory-b2c/multi-factor-auth-technical-profile) to do this. 


### **Can I customize end user sign up/sign in flows?** 

Yes, to help you set up the most common identity tasks for your applications, the Azure AD B2C includes predefined, configurable policies called User flows. Get started by [creating a User Flow](https://docs.microsoft.com/azure/active-directory-b2c/user-flow-overview). 

Custom policies are configuration files that define the behavior of your Azure AD B2C tenant. They are fully edited by an identity developer to complete many different tasks. Get started by [creating a Custom Policy](https://docs.microsoft.com/azure/active-directory-b2c/custom-policy-get-started). 

### **Useful Links**

* Learn [Best practices](https://docs.microsoft.com/azure/active-directory-b2c/best-practices)
* Review these [Frequently asked questions](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-faqs)
* Ask your question to our developer community at [Stack Overflow](http://stackoverflow.com/questions/tagged/azure-ad-b2c)
