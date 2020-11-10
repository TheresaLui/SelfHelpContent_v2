<properties
	pageTitle="Transfer an enterprise account to a new enrollment"
	description="Provides user with information about transferring enterprise account to new enrollment"
	infoBubbleText=""
	service="microsoft.enterpriseagreement"
	resource="enrollmentmanagement"
  authors="irinakolontaev1"
	ms.author="baolcsva"
	displayOrder=""
	articleId="df7a5f8b-aded-4305-92d1-4bc19ef0eb40"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32688695"
	resourceTags=""
	productPesIds="16867"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="AzureEA_SelfDeflectionContent"
/>

# Transfer an enterprise account to a new enrollment

Keep the following points in mind when you transfer an enterprise account to a new enrollment:
- Only the accounts specified in the request are transferred. If all accounts are chosen, then they are all transferred.
- The source enrollment retains its status as active or extended. You can continue using the enrollment until it expires.

### Effective transfer date

The effective transfer date can be a date on or after the start date of the enrollment that you want transfer to. The enrollment that you're transferring to is the _target enrollment_. After the account transfer, all usage information in the account before the effective transfer date stays in the enrollment you're transferring from. The enrollment that you're transferring from is the _source enrollment_.  The source enrollment usage is charged against monetary commitment or as overage. Usage that occurs after the effective transfer date is transferred to the new enrollment and charged accordingly.

You can backdate an account transfer as far back as the start date of the target enrollment. Or, as far as the source enrollment effective start date.

### Monetary commitment

Monetary commitment isn't transferrable between enrollments. Monetary commitment balances are tied contractually to the enrollment where it was ordered. Monetary commitment isn't transferred as part of the account or enrollment transfer process.

### Services affected

There's no downtime during the account transfer. It can be completed on the same day of your request if all required information is provided.

### Prerequisites

When you request an account transfer, provide the following information:

- Account name and account owner ID of account to transfer
- For the source enrollment, the enrollment number and account to transfer
- For the target enrollment, the enrollment number to transfer to
- For the account transfer effective date, it can be a date on or after the start date of the target enrollment

Other points to keep in mind before an account transfer:

- Approval from an EA Administrator is required for the target and source enrollment
  - In some cases, Microsoft might request additional approval from an EA administrator of the source enrollment
- If an account transfer doesn't meet your requirements, consider an enrollment transfer
- The account transfer transfers all services and subscriptions related to specific accounts
- After the transfer is complete, the transferred account appears inactive under the source enrollment
- An account transfer can be backdated to any date within the target enrollment start date
- The account shows the end date corresponding to the effective transfer date on the source enrollment and as a start date on the target enrollment
- Any usage occurred for the account prior to the effective transfer date remains under the source enrollment  

## **Recommended Documents**

- [Transfer enterprise enrollment to a new one](https://docs.microsoft.com/azure/billing/billing-ea-portal-administration#transfer-enterprise-enrollment-to-a-new-one)
- [Change account owner](https://docs.microsoft.com/azure/billing/billing-ea-portal-administration#change-account-owner)
- [Subscription transfer effects](https://docs.microsoft.com/azure/billing/billing-ea-portal-administration#subscription-transfer-effects)
- [Overage offset by customers](https://docs.microsoft.com/azure/billing/billing-ea-portal-enrollment-invoices#overage-offset-by-customers)
- [Enrollment status](https://docs.microsoft.com/azure/billing/billing-ea-portal-agreements#enrollment-status)
