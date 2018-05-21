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

It looks like your domain name <!--$domain-->[domain]<!--/$domain--> is verified in another tenant <!--$holdingTenant-->[holdingTenant]<!--/$holdingTenant-->. A domain name can be verified in a single directory at a time. If a domain name is currently verified in a different directory (using Office 365 or other Azure services), it cannot be verified in your new directory until it is deleted on other one. If you would like to delete the domain name from your other tenant <!--$holdingTenant-->[holdingTenant]<!--/$holdingTenant--> you can follow the instructions here on how to remove a domain name and it’s references. If you are not aware of the other directory that has this domain registered, please let us know.

To continue with deleting your domain name in the other tenant <!--$holdingTenant-->[holdingTenant]<!--/$holdingTenant--> proceed with the steps outlined in this article: [Delete a domain name and move it to another Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-domains-manage-azure-portal).