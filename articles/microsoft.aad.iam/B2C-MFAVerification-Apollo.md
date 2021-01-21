<properties 

pageTitle="MFA or email verification issues" 

description="Content on how to handle MFA or email verification issues" 

ms.author="nivi" 

displayOrder="" 

articleId="419cb94b-16cb-471e-bdf6-43f7b9178f6f" 

selfHelpType="Apollo" 

supportTopicIds="ba3cf1bc-f9fd-552e-8376-fe151bde7d37" 

productPesIds="16580" 

cloudEnvironments="public" 

ownershipId="AzureIdentity_B2C" 

/> 

## Welcome to our new guided troubleshooting experience for MFA or email verification issues. This experience integrates important documents and relevant results from the web. 

:::Section Recommended Solutions::: 

### **Enable multi-factor authentication in Azure Active Directory B2C** 

Azure Active Directory B2C (Azure AD B2C) integrates directly with Azure AD Multi-Factor Authentication so that you can add a second layer of security to sign-up and sign-in experiences in your applications. You enable multi-factor authentication without writing a single line of code. [Steps to enable multi-factor authentication](https://docs.microsoft.com/azure/active-directory-b2c/multi-factor-authentication?pivots=b2c-custom-policy) without writing a single line of code. 

<br> 

### **Can I send customized email to users that sign up to use my applications?** 

Yes, you can use the company branding feature to customize the content of verification emails. [Learn how elements of the email can be customized](https://docs.microsoft.com/azure/active-directory-b2c/faq?tabs=app-reg-ga#how-do-i-customize-verification-emails-the-content-and-the-from-field-sent-by-azure-ad-b2c). 

Also, by using <code> DisplayControls </code>(currently in preview) and the third-party email provider [SendGrid](https://docs.microsoft.com/azure/active-directory-b2c/custom-email-sendgrid) or [Mailjet](https://docs.microsoft.com/azure/active-directory-b2c/custom-email-mailjet), you can use your own email template and From: address and subject, as well as support localization and custom One-Time Password (OTP) settings. 

<br>  

### **For my customers, can I generate and send a code to a phone number, and then verify the code?** 

Azure Active Directory B2C (Azure AD B2C) provides support for verifying a phone number by using Azure AD Multi-Factor Authentication (MFA). [Steps to define an Azure AD MFA technical profile ](https://docs.microsoft.com/azure/active-directory-b2c/multi-factor-auth-technical-profile) technical profile to generate and send a code to a phone number, and then verify the code.  

 <br> 

### **Can I customize end user sign up/sign in flows?** 

Yes, to help you set up the most common identity tasks for your applications, the Azure AD B2C includes predefined, configurable policies called User flows. Get started by [creating a User Flow](https://docs.microsoft.com/azure/active-directory-b2c/user-flow-overview). 

Custom policies are configuration files that define the behavior of your Azure AD B2C tenant. They are fully edited by an identity developer to complete many different tasks. Get started by [creating a Custom Policy](https://docs.microsoft.com/azure/active-directory-b2c/custom-policy-get-started). 

<br> 

:::Section Additional resources:::  

## **Useful Links** 

* Learn [best practices and recommendations](https://docs.microsoft.com/azure/active-directory-b2c/best-practices) for integrating Azure AD B2C into existing or new application environments.  

* Click here to learn [Frequently asked questions](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-faqs) about the Azure Active Directory B2C. 

* Ask your question to our developer community at  [Stack Overflow](http://stackoverflow.com/questions/tagged/azure-ad-b2c). 

 
:::Section Instant answers::: 

## Here are some articles from the web that may help you 

<azureKB> 

<client>Portal</client> 

</azureKB> 
