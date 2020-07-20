<properties
	pageTitle="help with user manangement"
	description="help with user manangement"
	service="azure-billing"
	resource="billing"
	authors="prdasneo"
	ms.author="prdasneo"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32615296"
	resourceTags=""
	productPesIds="15659"
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
	articleId="174d5df1-d595-4db0-af84-3620c24dfa93"
	ownershipId="ASMS_Billing"
/>

# Help with User Management

To use Cloudyn you must have an Azure account and either a trial registration or paid subscription for Cloudyn. There two types of access:

* **Admin:** Allows a user unrestricted use of all functions in the Cloudyn portal, including: user management, recipient lists management and root entity access to all entity data
* **User:** Intended for end users to view reports and create reports using the access they have to entity data

Learn more:

* [How to add multiple accounts and entities to an existing Cloudyn subscription]https://social.msdn.microsoft.com/Forums/en-US/6245ebd8-643c-4061-b167-01e7b6ea0ca1/faq-how-to-add-multiple-accounts-and-entities-to-an-existing-cloudyn-subscription?forum=Cloudyn)
* [How to enable additional users to access Cloudyn (and resolve account lockout issues)](https://social.msdn.microsoft.com/Forums/en-US/30afd40c-2a1d-44a7-b8d3-bc788ce36229/faq-how-to-enable-additional-azure-users-to-use-cloudyn-and-resolve-account-lockout-issues?forum=Cloudyn)<br>

**Reasons for cost discrepancy between CSP and Cloudyn**<br>

There will be some difference in cost for CSP subscription in Cloudyn portal. In partner center portal, cost has been calculated as per local currency.<br>

There are some more reasons for cost discrepancy for CSP accounts in Cloudyn portal:

* CSP billing cycle may start anywhere during the month. Cloudyn’s month is always from the 1st of the month until the last month day (inclusive).
* CSP closes the cost calculation at some point during the last month day, so the monthly bill will always include some leftovers from the previous month and will always miss some cost from the end of the billing month. Cloudyn always calculates full day usage since at the time of Cloudyn’s calculation full usage data is already available.
* Partner Center presents costs according to CSP’s time zone. Cloudyn always calculates daily costs in UTC time.
* CSP may be charged in local currency. Cloudyn will always calculate costs in USD and the pricing differences may be more than the exchange rate differences.

Learn more: [FAQ: How to resolve apparent billing discrepancies between an Azure bill and Cloudyn reports](https://social.msdn.microsoft.com/Forums/azure/en-US/780bb6d5-99da-487f-96bb-849a83b45add/faq-how-to-resolve-apparent-billing-discrepancies-between-an-azure-bill-and-cloudyn-reports?forum=Cloudyn)


## **Recommended Documents**

* How to [Assign access to Cloudyn data](https://docs.microsoft.com/azure/cost-management/tutorial-user-access)
* [Video: Adding Users to Cloudyn](https://youtu.be/Nzn7GLahx30)<br>
* [Video: Creating a Cost Entity Hierarchy in Cloudyn](https://youtu.be/dAd9G7u0FmU)<br>
* [Cloudyn Overview](https://docs.microsoft.com/azure/cost-management/overview)<br>
* [Cloudyn Pricing](https://azure.microsoft.com/pricing/details/cost-management)<br>
* [Cloudyn regional availability](https://azure.microsoft.com/global-infrastructure/services/)<br>
* [Cloudyn Training videos](https://docs.microsoft.com/azure/cost-management/ref-videos)<br>
