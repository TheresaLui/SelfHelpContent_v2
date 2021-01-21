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
  ownershipid="AzureIdentity_B2C" 
 />
# Business to Consumer (B2C)

## **Recommended Steps**

### **User flows in Azure Active Directory B2C**

To help you set up the most common identity tasks for your applications, the Azure AD B2C portal includes predefined, configurable policies called [user flows](https://docs.microsoft.com/azure/active-directory-b2c/user-flow-overview).


### **Recommended user flows vs Standard user flows**

We've changed the way we reference user flow versions. Previously, we offered V1 (production-ready) versions, and V1.1 and V2 (preview) versions. Now, we've consolidated user flows into two versions. [Learn more](https://docs.microsoft.com/azure/active-directory-b2c/user-flow-versions)

### **I need to customize behavior of my Azure Active Directory B2C tenant**

Custom policies are configuration files that define the behavior of your Azure AD B2C tenant. User flows are predefined in the Azure AD B2C portal for the most common identity tasks. Custom policies can be fully edited by an identity developer to complete many different tasks. [Learn more](https://docs.microsoft.com/azure/active-directory-b2c/custom-policy-overview)

### **Password reset link is not working**

Currently, the combined "Sign-up or Sign-in policy" has a limitation that prevents your users from being able to reset their password from the login page. Azure AD B2C will return an error to your application when a user selects the password reset link. There are two different mechanisms to implement password reset:

1. **Use a Sign-in Policy**: No work required by the application. Selecting "I forgot my password" redirects the user automatically to a generic Microsoft-branded password reset page.
1. **Handle the error**: This requires the application to do some extra work. Selecting "I forgot my password" redirects the user back to the application with an error code. The application needs to detect that the error code in the request and then further redirect the user to the Azure AD B2C password reset policy. The password reset policy can be customized extensively.


## **Recommended Documents**

* [Azure AD B2C policies](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-reference-policies)
* [Best practices](https://docs.microsoft.com/azure/active-directory-b2c/best-practices)
* [Frequently asked questions](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-faqs)
* [Stack Overflow](http://stackoverflow.com/questions/tagged/azure-ad-b2c)
* [UserVoice](https://feedback.azure.com/forums/169401-azure-active-directory/category/160596-b2c)
