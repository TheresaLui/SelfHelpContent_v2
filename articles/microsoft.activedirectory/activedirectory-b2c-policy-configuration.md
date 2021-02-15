<properties
  pagetitle="Business to Consumer (B2C)"
  service=""
  resource=""
  ms.author="vigunase,nishring"
  selfhelptype="Generic"
  supporttopicids="32633328"
  resourcetags=""
  productpesids="16580"
  cloudenvironments="public,fairfax,mooncake,usnat,ussec,blackforest"
  disableclouds=""
  articleid="0868fb74-803a-4c70-86e8-1f09c7b74cba"
  ownershipid="AzureIdentity_B2C" />
# Business to Consumer (B2C)

## **Recommended Steps**

### **Password reset link is not working**

Currently, the combined **Sign-up or Sign-in policy** has a limitation that prevents your users from being able to reset their password from the login page. Azure AD B2C will return an error to your application when a user selects the password reset link. There are two different mechanisms to implement password reset:

1. **Use a Sign-in Policy**: No work required by the application. Selecting **I forgot my password** redirects the user automatically to a generic Microsoft-branded password reset page.
1. **Handle the error**: This requires the application to do some extra work. Selecting **I forgot my password** redirects the user back to the application with an error code. The application needs to detect that the error code in the request and then further redirect the user to the Azure AD B2C password reset policy. The password reset policy can be customized extensively.

### **Can I customize end user Sign up/Sign in flows?**

Yes, to help you set up the most common identity tasks for your applications, the Azure AD B2C includes predefined, configurable policies called User flows. Get started by [creating a User Flow](https://docs.microsoft.com/azure/active-directory-b2c/user-flow-overview?WT.mc_id=Portal-Microsoft_Azure_Support).

Custom policies are configuration files that define the behavior of your Azure AD B2C tenant. They are fully edited by an identity developer to complete many different tasks. Get started by [creating a Custom Policy](https://docs.microsoft.com/azure/active-directory-b2c/custom-policy-get-started?WT.mc_id=Portal-Microsoft_Azure_Support).

### **Useful Links** 

* Learn [best practices and recommendations](https://docs.microsoft.com/azure/active-directory-b2c/best-practices) for integrating Azure AD B2C into existing or new application environments.  

* Click here to learn [Frequently asked questions](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-faqs) about the Azure Active Directory B2C. 

* Ask your question to our developer community at  [Stack Overflow](http://stackoverflow.com/questions/tagged/azure-ad-b2c).