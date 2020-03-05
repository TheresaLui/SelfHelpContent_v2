<properties
	pageTitle="Sign In Issues - other"
	description="Sign In Issues - other"
	infoBubbleText="Sign In Issues - other "
	service="microsoft.visualstudio"
	resource="account"
	authors="chrisjco"
	ms.author="ccoop"
	articleId="AZDevOpsSignInIssues401andother"
	supportTopicIds="32572367, 32572368"
	diagnosticScenario=""
	selfHelpType="generic"
	resourceTags=""
	productPesIds="15543"
	cloudEnvironments="public"
	ownershipId="ASEP_ContentService_Placeholder"
/> 

# Common causes of sign-in issues 

## **Recommended Steps** 

### Troubleshooting Connectivity

As a first step in resolving connectivity issues with Azure DevOps, complete the following steps: 

1. Sign out of your browser. To do so, select the Visual Studio sign out link. 
2. Delete the cookies in your browser. To delete cookies in most browsers, press Ctrl+Shift+Del. 
3. Open Internet Explorer and delete the browser cookies. The Visual Studio IDE uses Internet Explorer cookies. 
4. Close all browsers and close the Visual Studio IDE
5. Use a private browser session to retry the connection. If the issue is with the Visual Studio IDE, remove the connection and re-add it.<br> 

### Troubleshoot signing in 

Two types of identities can sign in: Microsoft accounts and Azure Active Directory (Azure AD) accounts. Depending on your account, you might experience one of the following errors:<br>
 
**401 - Not Authorized**

The most common error page is the 401 Not Authorized error, which occurs when your identity doesn't have permissions to enter an organization. Common reasons for the error include:<br> 

* Your identity isn't a member of the organization
* Your identity has an invalid or missing license assignment

If you think you're a member of the organization but are blocked by this error page, [contact customer support](https://support.microsoft.com/).<br> 

**Scenario 1**

Your work or school Azure AD account doesn't have access, but your personal Microsoft account does. 

**401 - Work or school, or Personal account**

A highly specific 401 error case. In this case, both a personal Microsoft account and a work or school account (Azure AD) that have the same sign-in address exist. You've signed in with your work or school account, but your personal account is the identity with access to the organization.<br> 

**Mitigation**

In some cases, you might not know you have two identities with the same sign in address. The work or school Azure AD account might have been created by an administrator when you were added to Office365 or Azure AD. 

To sign out of your current work or school Azure AD account, select Sign in with your personal MSA account, and then sign in by using your personal Microsoft account. After authentication, you should have access to the organization.<br>
 
**Note**: To avoid seeing this prompt, you can rename your Microsoft account. Then, only one identity (your work or school account, or Azure AD account) uses your sign-in address.<br> 

**Scenario 2**

Your personal Microsoft account doesn't have access, but your Azure AD account does. This scenario is an opposite version of the 401 error page. In this case, the personal account (Microsoft account identity) doesn't have access to the organization and the work or school account (Azure AD identity) does. The same guidance from Scenario 1 applies, but in reverse. 

**401 - Work or school, or Personal account**

**Mitigaton**

If you enter your credentials correctly, but are redirected back to the original sign-in page, we recommend clearing all cookies, and then reattempting to sign in. If that doesn't fix the issue, [contact customer support](https://support.microsoft.com/).<br> 

## **Recommended Documents**

* [Resolve connection issues](https://docs.microsoft.com/azure/devops/user-guide/troubleshoot-connection?view=azure-devops)<br> 
* Want a quicker answer? Check out the [Azure DevOps Virtual Agent](https://azuredevopsvirtualagent.azurewebsites.net/) 
* To check the status of Azure DevOps Services or to see service impacting issues, please see the [Azure DevOps Service Status](https://status.dev.azure.com/) page.
