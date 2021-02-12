<properties
	pageTitle="Manage users"
	description="Providing users with information enterprise user roles and the permissions of each role"
	infoBubbleText=""
	service="microsoft.enterpriseagreement"
	resource="enrollmentmanagement"
  authors="irinakolontaev1"
	ms.author="baolcsva"
	displayOrder=""
	articleId="035e20b1-5ef0-428f-a509-b054233f86d6"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32688685"
	resourceTags=""
	productPesIds="16867"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="AzureEA_SelfDeflectionContent"
/>

# Manage users

### Enterprise user roles

To administer the Azure services in your enrollment, there are four distinct enterprise administrative user roles:

- Enterprise administrator
- Department administrator
- Account owner
- Service administrator

Roles are used to complete tasks in two different Microsoft Azure portals. The [Azure EA portal](https://ea.azure.com) is used to help you to manage billing and costs. The [Azure portal](https://portal.azure.com) is used to manage Azure services.

User roles are associated with a user account. To validate user authenticity, each user must have a valid work, school, or Microsoft account. Ensure that each account is associated with an email address that's actively monitored. Account notifications are sent to the email address.

When setting up users, you can assign multiple work, school, or Microsoft accounts to the enterprise administrator role. However, you can assign only one work, school, or Microsoft account to the account owner role. Additionally, a single work, school, or Microsoft account can have both the enterprise administrator and account owner roles applied to it.

### Enterprise administrator

The enterprise administrator role has the highest level of access. Users with the role can:

- Manage accounts and account owners
- Manage other enterprise administrators
- Manage department administrators
- Manage notification contacts
- View usage across all accounts
- View unbilled charges across all accounts

You can have multiple enterprise administrators in an enterprise enrollment. You can grant read-only access to enterprise administrators. They all inherit the department administrator role.

### Department administrator

Users with the role can:

- Create and manage departments
- Create new account owners
- View usage details for the departments that they manage
- View costs, if granted necessary permissions

You can have multiple department administrators for each enterprise enrollment.

You can grant department administrators read-only access. To grant read-only access, edit or create a new department administrator and set the read-only option to  **Yes**.

### Account Owner

Users with the role can:

- Create and manage subscriptions
- Manage service administrators
- View usage for subscriptions

Each account requires a unique work, school, or Microsoft account. For more information about Azure EA Portal administrative roles, see [Understand Azure Enterprise Agreement administrative roles in Azure](https://docs.microsoft.com/azure/billing/billing-understand-ea-roles).

### Service administrator

The service administrator has permissions to manage services in the Azure portal and assign users to the co-administrator role. Each role has a different level of access and authority.

## **Recommended Documents**

- [Understand Azure Enterprise Agreement administrative roles in Azure](https://docs.microsoft.com/azure/billing/billing-understand-ea-roles).
- [Azure EA portal administration](https://docs.microsoft.com/azure/billing/billing-ea-portal-administration)
- [Azure EA portal hierarchy](https://docs.microsoft.com/azure/billing/billing-ea-portal-get-started#azure-ea-portal-hierarchy)
- [Create another enterprise admin](https://docs.microsoft.com/azure/billing/billing-ea-portal-get-started#create-another-enterprise-admin)
- [Add a department admin](https://docs.microsoft.com/azure/billing/billing-ea-portal-get-started#add-a-department-admin)
- [Add an account](https://docs.microsoft.com/azure/billing/billing-ea-portal-get-started#add-an-account)
- [Enrollment status](https://docs.microsoft.com/azure/billing/billing-ea-portal-agreements#enrollment-status)
- [Get started with the Azure EA portal](https://docs.microsoft.com/azure/billing/billing-ea-portal-get-started)
