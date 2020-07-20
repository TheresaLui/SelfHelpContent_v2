<properties
	pageTitle="Microsoft-change organization owner"
	description="Azure DevOps Change Organization Owner Guidance"
	infoBubbleText="Azure DevOps Change Organization Owner Guidance"
	service="microsoft.visualstudio"
	resource="account"
	authors="chrisjco"
	ms.author="ccoop"
	articleId="AZDevOpsChangeOrgOwner"
	supportTopicIds="32260177"
	diagnosticScenario=""
	selfHelpType="generic"
	resourceTags=""
	productPesIds="15543"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Azure_DevOps_Services"
/>

# Azure DevOps Services Change Org Owner

4 out of every 5 cases related to changing organization owner were resolved using the solutions listed below.

## **Recommended Steps**

Most change organization owner requests fall into the following categories:

1.  I need to change the owner of my organization and either the current organization owner or a project collection administrator is still active. 
    
Prerequisites:
  - Ensure that you are either a project collection [administrator](https://docs.microsoft.com/azure/devops/organizations/accounts/faq-user-and-permissions-management?view=azure-devops#q-how-do-i-find-a-project-collection-administrator) or the organization [owner](https://docs.microsoft.com/azure/devops/organizations/accounts/faq-user-and-permissions-management?view=azure-devops#q-how-do-i-find-the-organization-owner) 
  - Ensure that the account you want to make organization owner has signed into your organization, created a profile and agreed to the Terms of Services
  - Accessed the organization at least once after creating an initial profile

If this is your issue and you meet the above prerequisites, please see [Changing organization owner](https://docs.microsoft.com/azure/devops/organizations/accounts/change-organization-ownership?view=azure-devops#change-organization-owner).
	
2. I need to change the owner of my organization and the organization owner and project collection administrator(s) are no longer active.

Prerequisites: 
  - Your Azure DevOps Services organization must be connected to Azure Active Directory (Azure AD)

If this is your issue and you meet the above prerequisites, please see [How to transfer ownership to another user](https://docs.microsoft.com/azure/devops/organizations/accounts/resolve-orphaned-organization?view=azure-devops).

3. I need to change the owner of my organization. It is not connected to Azure Active Directory (Azure AD) and neither the current organization owner or project collection administrator(s) are still active.
    
If this is your issue or your issue is not listed, please continue to create a support request.

## **Recommended Documents**

* [Change the organization owner](https://docs.microsoft.com/azure/devops/organizations/accounts/change-organization-ownership?view=azure-devops)
* [Assign a new owner to your orphaned organization](https://docs.microsoft.com/azure/devops/organizations/accounts/resolve-orphaned-organization?view=azure-devops)
* [Azure DevOps Virtual Agent](https://azuredevopsvirtualagent.azurewebsites.net/)
* [Azure DevOps Services Status](https://status.dev.azure.com)
