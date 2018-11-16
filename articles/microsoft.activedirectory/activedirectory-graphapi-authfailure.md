<properties
	pageTitle="Troubleshooting 401 and 403 authorization errors"
	description="How to resolve Microsoft Graph 401 and 403 authorization errors"
	service="microsoft.aad"
	resource="Microsoft_AAD_IAM"
	authors="dkershaw10"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32134056"
	resourceTags=""
	productPesIds="16575"
	cloudEnvironments="public"
/>

# Troubleshooting 401 and 403 authorization failures

Authorization failures can be a result of several different issues, and generally your app will receive either a 401 or 403 error. Incorrect [access token acquisition flows](https://docs.microsoft.com/azure/active-directory/develop/active-directory-authentication-scenarios), poorly configured [permission scopes](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-scopes), and lack of [consent](https://docs.microsoft.com/azure/active-directory/develop/active-directory-devhowto-multi-tenant-overview#understanding-user-and-admin-consent), can all lead to authorization errors.

## **Recommended steps**

To resolve common authorization errors, try the steps provided below that most closely matches the error you are receiving. Note that more than one may apply. You can also check the answers already available in StackOverflow for [401 errors](https://stackoverflow.com/search?q=%5Bmicrosoft-graph%5D+401+isanswered%3Ayes+views%3A50) and [403 errors](https://stackoverflow.com/search?q=%5Bmicrosoft-graph%5D+403+isanswered%3Ayes+views%3A50). If you can't find a solution to your problem, [ask a new question on StackOverflow](https://stackoverflow.com/questions/ask) and tag with *microsoft-graph*.

**401 unauthorized error: Has consent been granted**? <br>

Make sure that your application has been granted permission to access Microsoft Graph resources and that you are presenting a valid access token to Microsoft Graph as part of the request. Granting permissions normally happens through a user or admin granting consent through a consent page or by granting permissions using the Azure Portal application registration blade. From the **Settings** blade for the application, click **Required Permissions** and click on the **Grant Permissions** button. <br>
[Understanding Azure AD permissions and consent](https://docs.microsoft.com/azure/active-directory/develop/v2-permissions-and-consent) <br>

**401 unauthorized error: Have you chosen the right set of permissions?**<br>

Check that you have requested the correct set of permissions based on the Microsoft Graph APIs your app calls. Recommended least privileged permissions are provided in all the Microsoft Graph API reference method topics. <br>
[Microsoft Graph permissions](https://developer.microsoft.com/graph/docs/authorization/permission_scopes) <br>

**401 unauthorized error: Did your app acquire a token to match chosen permissions?** <br>

Make sure that the type of permissions requested or granted matches the type of access token that your app acquires. You might be requesting and granting application permissions, but using delegated interactive code flow tokens, instead of client credential flow tokens.  Or you might be requesting and granting delegated permissions, but using client credential flow tokens, instead of delegated code flow tokens. <br>
[Get access on behalf of users - and delegated permissions](https://developer.microsoft.com/graph/docs/concepts/auth_v2_user) <br>
[Azure AD v2.0 - OAuth 2.0 authorization code flow](https://docs.microsoft.com/azure/active-directory/develop/v2-oauth2-auth-code-flow) <br>
[Get access without a user (daemon service) - and application permissions](https://developer.microsoft.com/graph/docs/concepts/auth_v2_service) <br>
[Azure AD v2.0 - OAuth 2.0 client credentials flow](https://docs.microsoft.com/azure/active-directory/develop/v2-oauth2-client-creds-grant-flow) <br>

**401 unauthorized error: Resetting password or adding a user to a directory role**? <br>

Currently, there are no application permission daemon service-to-service permissions that allow resetting user passwords or directory role membership changes (or other highly privileged operations today). These APIs are only supported using the interactive delegated code flows with a signed-in administrator. <br>
[Microsoft Graph permissions](https://developer.microsoft.com/graph/docs/authorization/permission_scopes) <br>

**403 Forbidden: Does the user have access?** <br>

For delegated interactive code flows, Microsoft Graph evaluates if the request is allowed based on the permissions granted to the app and the permissions that the signed-in user has. Generally, this error indicates that the user is not privileged enough to perform the request **or** the user is not licensed for the data being accessed. Only users with the required permissions or licensed will be able to make the request successfully.

**403 Forbidden: Did you select the correct resource API?** <br>

API services like Microsoft Graph check that the *aud* claim (audience) in the received access token matches the value it expects for itself, and if not, it will result in a 403 Forbidden error. A common mistake resulting in this error is trying to use a token acquired for Azure AD Graph API, to call Microsoft Graph (or vice versa). Ensure that the resource your app is acquiring a token for matches the API that the app is calling.

**400 Bad Request or 403 Forbidden: Does the user comply with their organization's conditional access (CA) policies?**<br>

Based on an organization's CA policies, a user accessing Microsoft Graph resources via your app may need to be challenged for additional information that is not present in the access token your app originally acquired. In this case, your app will receive a 400 with an *interaction_required* error or a 403 with *insufficient_claims* error, and additional information that can be presented to the authorize endpoint to challenge the user for additional information (like multi-factor authentication).<br>
[Developer guidance for Azure Active Directory conditional access](https://docs.microsoft.com/azure/active-directory/develop/conditional-access-dev-guide)
