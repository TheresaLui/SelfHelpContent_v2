<properties
	pageTitle="Permissions are not granted after activating a role"
	description="After you activate a role in Azure AD Privileged Identity Management (PIM), you don't have the assigned permissions."
	service="microsoft.aad"
	resource="Microsoft_Azure_PIM"
	authors="rolyon"
	ms.author="rolyon"
	displayOrder="1"
	selfHelpType="resource"
	supportTopicIds="32462545"
	resourceTags="privilegedidentitymanagement_overview"
	productPesIds="16577"
	cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	articleId="b64b291b-35e2-4cfa-8925-4dbe26427262"
	ownershipId="AzureIdentity_ComplianceAndReporting"
/>

# Permissions are not granted after activating a role

When you activate a role in Azure AD Privileged Identity Management (PIM), the activation may not instantly propagate to all portals that require the privileged role. Sometimes, even if the change is propagated, web caching in a portal may result in the change not taking effect immediately. If your activation is delayed, here are the steps you should follow.

## **Recommended Steps**

1. Sign out of the Azure portal and then sign back in. When you activate an Azure AD role or an Azure resource role, you will see the stages of your activation. Once all the stages are complete, you will see a **Sign out** link. You can use this link to sign out. This will solve most cases for activation delay.

1. In PIM, verify that you are listed as the member of the role

1. If you are activating the Exchange Administrator role, make sure you sign out and sign back in. If the problem persists, open a support ticket and raise this as an issue. If you are using your Exchange Administrator role to access the Security and Compliance Center, see the next step.

1. If you activating a role to access the Security and Compliance Center or if you activating the SharePoint Administrator role, you will experience some activation delay from a few minutes up to a few hours. This is a known issue and we are actively working with these teams to resolve this issue as soon as possible.

## **Recommended Documents**

* [Activate my Azure AD roles in PIM](https://docs.microsoft.com/azure/active-directory/privileged-identity-management/pim-how-to-activate-role)
* [Activate my Azure resource roles in PIM](https://docs.microsoft.com/azure/active-directory/privileged-identity-management/pim-resource-roles-activate-your-roles)
