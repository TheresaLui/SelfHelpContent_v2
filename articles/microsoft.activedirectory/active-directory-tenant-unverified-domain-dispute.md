<properties
	pageTitle="Domain Dispute Customer Ready Content"
	description="Domain is verified in another Azure Active Directory tenant"
	infoBubbleText="See details on the right"
	service="microsoft.activedirectory"
	resource=""
	authors="bernawy"
	displayOrder="1"
	articleId="Tenant_Unverified_Domain_Dispute"
	diagnosticScenario="DomainDispute"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>

# Domain is verified in another Azure Active Directory tenant

It looks like your domain name <!--$domain-->[domain]<!--/$domain--> is verified in another directory <!--$holdingTenant-->[holdingTenant]<!--/$holdingTenant-->.

A domain name can be verified in a single directory at a time. Since your domain name is currently verified in a different directory (using Office 365 or other Azure services), it cannot be verified in your current new directory until it is deleted on the other one.

If you would like to delete the domain name from your other directory <!--$holdingTenant-->[holdingTenant]<!--/$holdingTenant--> you can [read](https://docs.microsoft.com/azure/active-directory/active-directory-domains-manage-azure-portal) the instructions on how to remove a domain name and its references. You need to be a global administrator in the other directory <!--$holdingTenant-->[holdingTenant]<!--/$holdingTenant--> to be able to delete the domain.

If you are not aware of the other directory that has this domain registered, please let us know.