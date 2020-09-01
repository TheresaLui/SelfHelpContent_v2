<properties
	pageTitle="Change account owner"
	description="Providing users with information about changing the account owner"
	infoBubbleText=""
	service="microsoft.enterpriseagreement"
	resource="enrollmentmanagement"
  authors="irinakolontaev1"
	ms.author="baolcsva"
	displayOrder=""
	articleId="70c94ee4-9fe0-4f84-8d44-9c15f814a7ef"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32688679"
	resourceTags=""
	productPesIds="16867"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="AzureEA_SelfDeflectionContent"
/>

# Change account owner

Enterprise administrators can use the Azure EA portal to transfer subscription account ownership in an enrollment. The action moves all subscriptions from a source user account a destination user account.

### Important points about transferring user account information

- Transfers from a Work or School account to another Work or School account are supported
- Transfers from a Microsoft account to a Work or School account are supported
- Transfers from a Work or School account to a Microsoft account are not supported
- Transfers from a Microsoft account to another Microsoft account are supported. The target account must be a valid Azure Commerce account to be a valid target for transfers.  For new accounts, you are asked to create an Azure Commerce account when signing in to the Azure EA portal. For existing accounts, you must first create a new Azure subscription before the account is eligible.
- When you complete a subscription transfer, Microsoft updates the account owner

### RBAC Policies

- Only Azure subscription transfers between two organizational ID's in the same tenant preserve existing Azure role-based access control (RBAC) policies, service administrator role assignments, and co-administrator role assignments. Other subscription transfers result in losing your RBAC policies and service administrator co-administrator role assignments. Policies and administrator roles don't transfer across different directories. Service administrators are updated to the owner of destination account.
- When you perform subscription transfers between two organizational ID's in the same tenant, RBAC policies and existing service administrator and co-administrator roles are preserved

### Before changing an account owner

1. View the  **Account**  tab and identify the source account. The source account must be active.
1. Identify the destination account. It must be active.

### To transfer account ownership for all subscriptions

1. In the left navigation area, click  **Manage**
1. Click the  **Account**  tab and hover over an account
1. Click the change account owner symbol on the right
1. Select an eligible account and then click  **Next**
1. Confirm the transfer and click  **Submit**

### To transfer account ownership for a single subscription

1. In the left navigation area, click  **Manage**
1. Click the  **Account**  tab and hover over an account
1. Click the transfer subscriptions symbol on the right
1. Select an eligible subscription and then click  **Next**
1. Confirm the transfer and then click  **Submit**

## **Recommended Documents**

- [Transfer an enterprise account to a new enrollment](https://docs.microsoft.com/azure/billing/billing-ea-portal-administration#transfer-an-enterprise-account-to-a-new-enrollment)
- [Transfer enterprise enrollment to a new one](https://docs.microsoft.com/azure/billing/billing-ea-portal-administration#transfer-enterprise-enrollment-to-a-new-one)
- [Subscription transfer effects](https://docs.microsoft.com/azure/billing/billing-ea-portal-administration#subscription-transfer-effects)
- [Transfer enterprise enrollment to a new one](https://docs.microsoft.com/azure/billing/billing-ea-portal-administration#transfer-enterprise-enrollment-to-a-new-one)
- [Overage offset by customers](https://docs.microsoft.com/azure/billing/billing-ea-portal-enrollment-invoices#overage-offset-by-customers)
