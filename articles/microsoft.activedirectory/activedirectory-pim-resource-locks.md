<properties
	pageTitle="Delays when activating or deactivating a role"
	description="After you activate a role in Azure AD Privileged Identity Management (PIM), you don't have the assigned permissions. Or after you deactivate a role in PIM, permissions are not removed."
	service="microsoft.aad"
	resource="Microsoft_Azure_PIM"
	authors="rolyon"
	ms.author="rolyon"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32462545"
	resourceTags=""
	productPesIds="16577"
	cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	articleId="bcb5dde1-bae9-4225-857e-9316ea7ac7f3"
	ownershipId="AzureIdentity_ComplianceAndReporting"
/>

# Delays when activating or deactivating a role

## Permissions are not granted after activating a role

When you activate a role in Azure AD Privileged Identity Management (PIM), the activation may not instantly propagate to all portals that require the privileged role. Sometimes, even if the change is propagated, web caching in a portal may result in the change not taking effect immediately. If your activation is delayed, here are the steps you should follow.

## **Recommended Steps**

1. Sign out of the Azure portal and then sign back in. When you activate an Azure AD role or an Azure resource role, you will see the stages of your activation. Once all the stages are complete, you will see a **Sign out** link. You can use this link to sign out. This will solve most cases for activation delay.

1. In PIM, verify that you are listed as the member of the role

1. If you are activating the Exchange Administrator role, make sure you sign out and sign back in. If the problem persists, open a support ticket and raise this as an issue. If you are using your Exchange Administrator role to access the Security and Compliance Center, see the next step.

1. If you activating a role to access the Security and Compliance Center or if you activating the SharePoint Administrator role, you will experience some activation delay from a few minutes up to a few hours. This is a known issue and we are actively working with these teams to resolve this issue as soon as possible.

## **Recommended Documents**

* [Activate my Azure AD roles in PIM](https://docs.microsoft.com/azure/active-directory/privileged-identity-management/pim-how-to-activate-role)
* [Activate my Azure resource roles in PIM](https://docs.microsoft.com/azure/active-directory/privileged-identity-management/pim-resource-roles-activate-your-roles)

## Permissions are not removed after deactivating a role or the role activation expires

When you deactivate a role in Azure AD Privileged Identity Management (PIM) or when a role activation period expires, there might be a delay where you continue to have access. The following scenarios are two possible delays.

## **Recommended Steps**

1. If you are deactivating the Exchange Administrator role or the role activation period expires, and you notice a significant delay before the permissions are removed, open a support ticket and tell your support engineer to help you file a ticket with the privileged access management (PAM) team inside Office about this issue

1. If the activation period has expired, but you still have the browser session open, close your browser. You can continue to use the role until you close that session. This is a known issue and we are looking at a potential fix to actively revoke each session once activation has expired.

1. If your delay is different than these two scenarios, please open a support ticket

## **Recommended Documents**

* [Deactivate an Azure AD roles in PIM](https://docs.microsoft.com/azure/active-directory/privileged-identity-management/pim-how-to-activate-role#deactivate-a-role)
