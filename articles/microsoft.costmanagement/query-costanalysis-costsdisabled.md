<properties
	articleId="query-costanalysis-costsdisabled"
	articleTags="costanalysis,views"
	pageTitle="What does costs are disabled for your organization mean?"
	description="Cost by resource"
	displayOrder="1"
	authors="flanakin"
	ms.author="micflan"
	selfHelpType="resource"
	service="microsoft.costmanagement"
	resource="query"
	resourceTags=""
	productPesIds="15659"
	supportTopicIds="32615286"
	cloudEnvironments="public,fairfax"
/>

# What does "costs are disabled for your organization" mean?

Organizations using Enterprise Agreement (EA) or Microsoft Customer Agreement (MCA) accounts 
can disable access to cost and pricing information. 

EA billing account admins can review and update cost visibility by going to 
**Cost Management + Billing** > (select a billing account) > **Policies**. 
"Department admin can view charges" determines whether a department admin can see costs for their departments.
"Account owner can view charges" determines whether enrollment account admins and RBAC users can see costs 
for the specific scopes they have access to. 
"RBAC users" accounts for anyone who has Azure RBAC access to a resource group, subscription, or management group.

MCA billing account owners can toggle cost visibility ("View charges") from 
**Cost Management + Billing** > **Billing profiles** > (select profile) > **Policies**. 
Billing profile owners will open their billing profile directly from **Cost Management + Billing**. 
Within MCA, cost visibility can be granularly enabled or disabled per billing profile.

Whether you are using an EA or MCA account, all cost visibility settings are recommended to be enabled 
to ensure everyone within the organization is aware of the fiscal impact they're making with their 
cloud architecture choices and has an opportunity to optimize them.


## Recommended documents

* [Explore and analyze costs with cost analysis](https://aka.ms/costanalysis/docs)
* [Query API for rich reporting](https://aka.ms/costanalysis/api)
* [UsageDetails API for all cost and usage data](https://aka.ms/costmgmt/usagedetails)
* [Understanding and working with scopes](https://aka.ms/costmgmt/scopes)
* [Understanding cost and usage data](https://aka.ms/costmgmt/data)
