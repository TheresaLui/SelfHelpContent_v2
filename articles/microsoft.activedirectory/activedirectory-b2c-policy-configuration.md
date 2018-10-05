 <properties
	pageTitle="Business to Consumer (B2C)"
	description="Business to Consumer (B2C)"
	service="microsoft.azureactivedirectory"
	resource="b2cDirectories"
	authors="parakhj"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32422332"
	resourceTags=""
	productPesIds="14785,16580"
	cloudEnvironments="public"
/>

# Business to Consumer (B2C)

## **Recommended steps**

### **Password reset link is not working**

Currently, the combined "Sign-up or Sign-in policy" has a limitation that prevents your users from being able to reset their password from the login page. Azure AD B2C will return an error to your application when a user clicks on the password reset link. There are two different mechanisms to implement password reset in this case:

1. **Use a Sign-in Policy**: No work required by the application, clicking on "I forgot my password" redirects the user automatically to a generic Microsoft-branded password reset page.
1. **Handle the error**: This requires the application to do some extra work. Clicking on "I forgot my password" redirects the user back to the application with an error code. The application needs to detect that the error code in the request and then further redirect the user to the Azure AD B2C password reset policy. The password reset policy can be customized extensively.

### **Session token configuration is not being enforced**

If you use the "Sign-in" policy, your custom session token duration will not be enforced. The workaround is to use a combined "Sign in / Sign up" policy instead. This issue originates from the fact that the "Sign-up or Sign-in" policy leverages a newer and improved policy implementation compared to the older "Sign-in" policy.

### **I am unable to customize the UI**

At this time, we do not support UI customization for "Sign-in" policies. You can use a "Sign-up or Sign-in" policy if you would like to customize your sign-in page. If you would like to see UI customization supported for "Sign-in" policies, we encourage you to vote and/or add comments in our [UserVoice](https://feedback.azure.com/forums/169401-azure-active-directory/suggestions/13062033-b2c-fully-customizable-sign-in-page) forum with your feedback.

## **Recommended documents**

* [Azure AD B2C Policies](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-reference-policies)
* [Frequently asked questions](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-faqs)
* [Stack Overflow](http://stackoverflow.com/questions/tagged/azure-ad-b2c)
* [UserVoice](https://feedback.azure.com/forums/169401-azure-active-directory/category/160596-b2c)