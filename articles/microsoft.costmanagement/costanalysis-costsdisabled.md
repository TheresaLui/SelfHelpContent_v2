<properties
	articleId="costanalysis-costsdisabled"
	articleTags="access"
	pageTitle="What does costs are disabled for your organization mean?"
	description="Cost disabled"
	displayOrder="4"
	authors="flanakin"
	ms.author="micflan"
	selfHelpType="resource"
	service="microsoft.costmanagement"
	resource="costanalysis"
	resourceTags=""
	productPesIds="15659"
	supportTopicIds="32615286"
	cloudEnvironments="public,fairfax, usnat, ussec"
	ownershipId="ASMS_Billing"
/>

# What does 'costs are disabled for your organization' mean?

Organizations using Enterprise Agreement (EA) or Microsoft Customer Agreement (MCA) accounts can disable access to cost and pricing information. When this access has been disabled, you may see a "Costs disabled for your organization" message. Contact a billing account or billing profile owner to enable access to costs.

EA billing accounts have two options: "Department admin can view charges" allows department admins to see costs for their departments and "Account owners can view charges" allows enrollment account admins and subscription users to see costs for their subscriptions.

MCA billing profiles have a single "View charges" option, which allows subscription users to see costs. 

When costs are enabled for subscription users, access to costs is determined by Azure RBAC roles, which can be assigned at a resource group, subscription, or management group level.

Whether you are using an EA or MCA account, all cost visibility settings are recommended to be enabled to ensure everyone within the organization is aware of the fiscal impact they're making with their cloud architecture choices and has an opportunity to optimize them.<br>

CSPs and Indirect EAs have their reseller enable Markup for them to be able to view costs in Azure Cost Management.<br>

## **Recommended Steps**

To enable access to cost and pricing information within the organization, a billing account or billing profile owner must complete the following steps:

1. Go to **Cost Management + Billing**
2. Select a billing account or billing profile
3. If available, go to **Billing profiles** and select a billing profile (only applies to MCA accounts)
4. Go to **Policies**
5. Enable each of the "view charges" options to ensure everyone can see costs

## **Recommended Documents**

* [Explore and analyze costs with cost analysis](https://docs.microsoft.com/azure/cost-management/quick-acm-cost-analysis)
* [Query API for rich reporting](https://docs.microsoft.com/rest/api/cost-management/query)
* [UsageDetails API for all cost and usage data](https://docs.microsoft.com/rest/api/consumption/usagedetails/list)
* [Understanding and working with scopes](https://docs.microsoft.com/azure/cost-management/understand-work-scopes)
* [Understanding cost and usage data](https://docs.microsoft.com/azure/cost-management/understand-cost-mgt-data)
