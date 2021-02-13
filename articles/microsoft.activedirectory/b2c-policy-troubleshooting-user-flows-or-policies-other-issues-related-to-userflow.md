<properties
  pagetitle="Business to Consumer (B2C)"
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

### **User flows in Azure Active Directory B2C** 

To help you set up the most common identity tasks for your applications, the Azure AD B2C includes predefined, configurable policies called User flows. Get started by  [creating a User Flow](https://docs.microsoft.com/azure/active-directory-b2c/user-flow-overview).


### **Recommended user flows vs Standard user flows** 

We've changed the way we reference user flow versions. Previously, we offered V1 (production-ready) versions, and V1.1 and V2 (preview) versions. Now, we've consolidated user flows into two versions. [Find out more details about User Flow Version](https://docs.microsoft.com/azure/active-directory-b2c/user-flow-versions).

### **Can I customize end-user sign up/sign in flows?** 

Yes, to help you set up the most common identity tasks for your applications, the Azure AD B2C includes predefined, configurable policies called User flows. Get started by [creating a User Flow](https://docs.microsoft.com/azure/active-directory-b2c/user-flow-overview). 

Custom policies are configuration files that define the behavior of your Azure AD B2C tenant. They are fully edited by an identity developer to complete many different tasks. Get started by [creating a Custom Policy](https://docs.microsoft.com/azure/active-directory-b2c/custom-policy-get-started). 

### **Password reset link is not working**

Currently, the combined **Sign-up or Sign-in** policy has a limitation that prevents your users from resetting their password on the login page. Azure AD B2C will return an error to your application when a user selects the password reset link. There are two different mechanisms to implement password reset:

1. **Use a Sign-in Policy**: No work required by the application. Selecting **I forgot my password** automatically redirects you to a generic Microsoft  password reset page.

1. **Handle the error**: This requires the application to do some extra work. Selecting **I forgot my password** redirects you back to the application with an error code. The application needs to detect the error code in the request and then redirects the user to the Azure AD B2C password reset policy. The password reset policy can be customized extensively.


### **Useful Links** 

* Learn [best practices and recommendations](https://docs.microsoft.com/azure/active-directory-b2c/best-practices) for integrating Azure AD B2C into existing or new application environments.  

* Click here to learn [Frequently asked questions](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-faqs) about the Azure Active Directory B2C. 

* Ask your question to our developer community at [Stack Overflow](http://stackoverflow.com/questions/tagged/azure-ad-b2c).
