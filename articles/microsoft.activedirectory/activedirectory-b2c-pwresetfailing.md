 <properties
	pageTitle="Business to Consumer (B2C)/Password reset failing"
	description="Business to Consumer (B2C)/Password reset failing"
	service="microsoft.azureactivedirectory"
	resource="b2cDirectories"
	authors="parakhj"
	displayOrder="4"
	selfHelpType="resource"
	supportTopicIds="32416703"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>

# Password reset link is not working

Currently, the combined "Sign-up or Sign-in policy" has a limitation that prevents your users from being able to reset their password from the login page. Azure AD B2C will return an error to your application when a user clicks on the password reset link. There are two different mechanisms to implement password reset in this case:

1. **Use a Sign-in Policy**: No work required by the application, clicking on "I forgot my password" redirects the user automatically to a generic Microsoft-branded password reset page.
1. **Handle the error**: This requires the application to do some extra work. Clicking on "I forgot my password" redirects the user back to the application with an error code. The application needs to detect that the error code in the request and then further redirect the user to the Azure AD B2C password reset policy. The password reset policy can be customized extensively.

## **Recommended documents**

[Sample using Sign-up or Sign-in policy](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-devquickstarts-web-dotnet-susi)