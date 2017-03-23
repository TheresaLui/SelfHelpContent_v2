<properties
	pageTitle="I tried to delete users or reset passwords but I get a 401 unauthorized"
	description="I tried to delete users or reset passwords but I get a 401 unauthorized"
	service="microsoft.aad"
	resource="Microsoft_AAD_IAM"
	authors="PatAltimore"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32134056"
	resourceTags=""
	productPesIds="14785"
	cloudEnvironments="public"
/>

# I tried to delete users or reset passwords but I get a 401 unauthorized

## **Recommended steps**
* The application is using daemon service-to-service permissions that do not support these highly privileged operations today.  Please use the interactive code flows with a signed-in administrator.

## **Recommended documents**
[Microsoft Graph permission scopes](https://developer.microsoft.com/graph/docs/authorization/permission_scopes)<br>
