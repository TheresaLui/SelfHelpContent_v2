<properties
	pageTitle="I get a 403 forbidden, but I selected all permissions"
	description="I get a 403 forbidden, but I selected all permissions"
	service="microsoft.aad"
	resource=""
	authors="PatAltimore"
	displayOrder="Microsoft_AAD_IAM"
	selfHelpType="generic"
	supportTopicIds="32134056"
	resourceTags=""
	productPesIds="14785"
	cloudEnvironments="public"
/>

# I get a 403 forbidden, but I selected all permissions

## **Recommended steps**
* For delegated interactive code flows, Microsoft Graph evaluates if the request is allowed based on the permissions granted to the app and the permissions that the user has.  A 403 forbidden error indicates that the user is not privileged enough to perform the request.  Only users with the required permissions will be able to make the request successfully.

## **Recommended documents**
[Microsoft Graph permission scopes](https://developer.microsoft.com/en-us/graph/docs/authorization/permission_scopes)