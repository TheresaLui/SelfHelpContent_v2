<properties
	pageTitle="Subscription transfer effects"
	description="Providing user with information about subscription transfer effects"
	infoBubbleText=""
	service="microsoft.enterpriseagreement"
	resource="enrollmentmanagement"
    authors="irinakolontaev1"
	ms.author="baolcsva"
	displayOrder=""
	articleId="84025713-8bfa-4a09-ba72-e76cfb885b36"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32688693"
	resourceTags=""
	productPesIds="16867"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="AzureEA_SelfDeflectionContent"
/>

# Subscription transfer effects

When an Azure subscription is transferred to an account in the same Azure Active Directory tenant, then all users, groups, and service principals that had [role-based access control (RBAC)](https://docs.microsoft.com/azure/role-based-access-control/overview) to manage resources retain their access.

To view users with RBAC access to the subscription:

1. In the Azure portal, open **Subscriptions**
1. Select the subscription you want to view, and then select **Access control (IAM)**
1. Select **Role assignments**. The role assignments page lists all users who have RBAC access to the subscription.

If the subscription is transferred to an account in a different Azure AD tenant, then all users, groups, and service principals that had [RBAC](https://docs.microsoft.com/azure/role-based-access-control/overview) to manage resources _lose_ their access. Although RBAC access is not present, access to the subscription might be available through security mechanisms, including:

- [Management certificates](https://docs.microsoft.com/azure/cloud-services/cloud-services-certs-create) that grant the user admin rights to subscription resources
- Access keys for services such as [Storage](https://docs.microsoft.com/azure/storage/common/storage-account-overview)
- Remote Access credentials for services such as Azure Virtual Machines

If the recipient needs to restrict access to their Azure resources, they should consider updating any secrets associated with the service. Most resources are be updated by using the following steps:

1. Sign in to the [Azure portal](https://portal.azure.com/)
1. On the Hub menu, select **All resources**
1. Select the resource
1. On the resource page, click **Settings** to view and update existing secrets

## **Recommended Documents**

- [Transfer an enterprise account to a new enrollment](https://docs.microsoft.com/azure/billing/billing-ea-portal-administration#transfer-an-enterprise-account-to-a-new-enrollment)
- [Transfer enterprise enrollment to a new one](https://docs.microsoft.com/azure/billing/billing-ea-portal-administration#transfer-enterprise-enrollment-to-a-new-one)
- [Change account owner](https://docs.microsoft.com/azure/billing/billing-ea-portal-administration#change-account-owner)
- [Azure EA portal administration](https://docs.microsoft.com/azure/billing/billing-ea-portal-administration)
