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
  ownershipid="AzureIdentity_B2C" 
 />
# Business to Consumer (B2C)

## **Recommended Steps**

### **Enable multi-factor authentication in Azure Active Directory B2C**

Azure Active Directory B2C (Azure AD B2C) integrates directly with Azure AD Multi-Factor Authentication so that you can add a second layer of security to sign-up and sign-in experiences in your applications. You enable multi-factor authentication without writing a single line of code. [Learn more](https://docs.microsoft.com/azure/active-directory-b2c/multi-factor-authentication?pivots=b2c-custom-policy).


### **Can I send customized email to users that sign up to use my applications?**

Yes, by using <code>DisplayControls</code> (currently in preview) and the third-party email provider [SendGrid](https://docs.microsoft.com/azure/active-directory-b2c/custom-email-sendgrid) or [Mailjet](https://docs.microsoft.com/azure/active-directory-b2c/custom-email-mailjet), you can use your own email template and From: address and subject, as well as support localization and custom one-time password (OTP) settings.


### **For my customers, can I generate and send a code to a phone number, and then verify the code?**

Azure Active Directory B2C (Azure AD B2C) provides support for verifying a phone number by using Azure AD Multi-Factor Authentication (MFA). Use [this technical profile](https://docs.microsoft.com/azure/active-directory-b2c/multi-factor-auth-technical-profile) to generate and send a code to a phone number, and then verify the code. 


### **I need to customize behavior of my Azure Active Directory B2C tenant**

Custom policies are configuration files that define the behavior of your Azure AD B2C tenant. User flows are predefined in the Azure AD B2C portal for the most common identity tasks. Custom policies can be fully edited by an identity developer to complete many different tasks. [Learn more](https://docs.microsoft.com/azure/active-directory-b2c/custom-policy-overview)


### **Password reset link is not working**

Currently, the combined **Sign-up or Sign-in policy** has a limitation that prevents your users from being able to reset their password from the login page. Azure AD B2C will return an error to your application when a user selects the password reset link. There are two different mechanisms to implement password reset:

1. **Use a Sign-in Policy**: No work required by the application. Selecting **I forgot my password** redirects the user automatically to a generic Microsoft-branded password reset page.
1. **Handle the error**: This requires the application to do some extra work. Selecting **I forgot my password** redirects the user back to the application with an error code. The application needs to detect that the error code in the request and then further redirect the user to the Azure AD B2C password reset policy. The password reset policy can be customized extensively.


## **Recommended Documents**

* [Azure AD B2C policies](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-reference-policies)
* [Best practices](https://docs.microsoft.com/azure/active-directory-b2c/best-practices)
* [Frequently asked questions](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-faqs)
* [Stack Overflow](http://stackoverflow.com/questions/tagged/azure-ad-b2c)
* [UserVoice](https://feedback.azure.com/forums/169401-azure-active-directory/category/160596-b2c)
