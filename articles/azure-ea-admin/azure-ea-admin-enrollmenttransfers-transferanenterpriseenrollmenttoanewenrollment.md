<properties
	pageTitle="Transfer an enterprise enrollment to a new enrollment"
	description="Providing information for users to transfer an enterprise enrollment to a new enrollment"
	infoBubbleText=""
	service="microsoft.enterpriseagreement"
	resource="enrollmentmanagement"
  authors="irinakolontaev1"
	ms.author="baolcsva"
	displayOrder=""
	articleId="c1b45095-ac0a-4711-8176-c032ee3603a0"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32688696"
	resourceTags=""
	productPesIds="16867"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="AzureEA_SelfDeflectionContent"
/>

# Transfer an enterprise enrollment to a new enrollment

When you request to transfer an entire enterprise enrollment to an enrollment, the following actions occur:

- All Azure services, subscriptions, accounts, departments, and the entire enrollment structure, including all EA department administrators, are transferred
- The enrollment status is set to _Transferred_. The transferred enrollment is available for historic usage reporting purposes only.
- You can't add roles or subscriptions to a transferred enrollment. Transferred status prevents additional usage against the enrollment.
- Any remaining monetary commitment balance in the agreement is lost, including future terms

### Effective transfer date

The effective transfer day can be a date on or after the start date of the enrollment that you want transfer to the target enrollment.

The source enrollment usage is charged against monetary commitment or as overage. Usage that occurs after the effective transfer date is transferred to the new enrollment and charged accordingly.

### Effective transfer date in the past

You can backdate an account transfer as far back as the start date of the target enrollment. Or, as far as the effective start date of the source enrollment.

### Monetary commitment

Monetary commitment isn't transferrable between enrollments. Monetary commitment balances are tied contractually to the enrollment where it was ordered. Monetary commitment isn't transferred as part of the account or enrollment transfer process.

### Services affected

There's no downtime during the account transfer. It can be completed on the same day of your request if all requisite information is provided.

### Prerequisites

When you request an enrollment transfer, provide the following information:

- For the source enrollment, the enrollment number and account to transfer
- For the target enrollment, the enrollment number to transfer to
- For the enrollment transfer effective date, it can be a date on or after the start date of the target enrollment. The chosen date can't impact usage for any overage invoice already issued.

Other points to keep in mind before an enrollment transfer:

- Approval from an EA Administrator is required for the target and source enrollment
  - In some cases, Microsoft might request additional approval from an EA administrator of the source enrollment
- If an enrollment transfer doesn't meet your requirements, consider an account transfer
- Only the accounts that you specify are transferred. You can request to transfer all of your accounts.
- The source enrollment retains its status as active/extended. You can continue using the enrollment until it expires.

## **Recommended Documents**

- [Transfer an enterprise account to a new enrollment](https://docs.microsoft.com/azure/billing/billing-ea-portal-administration#transfer-an-enterprise-account-to-a-new-enrollment)
- [Change account owner](https://docs.microsoft.com/azure/billing/billing-ea-portal-administration#change-account-owner)
- [Subscription transfer effects](https://docs.microsoft.com/azure/billing/billing-ea-portal-administration#subscription-transfer-effects)
- [Overage offset by customers](https://docs.microsoft.com/azure/billing/billing-ea-portal-enrollment-invoices#overage-offset-by-customers)
