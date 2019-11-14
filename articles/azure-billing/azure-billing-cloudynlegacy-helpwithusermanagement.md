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
	cloudEnvironments="public"
	articleId="174d5df1-d595-4db0-af84-3620c24dfa93"
/>

# Help with User Management

To use Cloudyn you must have an Azure account and either a trial registration or paid subscription for Cloudyn.There two types of access:

* **Admin:** Allows a user unrestricted use of all functions in the Cloudyn portal, including: user management, recipient lists management and root entity access to all entity data.
* **User:** Intended for end users to view reports and create reports using the access they have to entity data. 

Learn more:<br>
[How to add multiple accounts and entities to an existing Cloudyn subscription](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fsocial.msdn.microsoft.com%2FForums%2Fen-US%2F6245ebd8-643c-4061-b167-01e7b6ea0ca1%2Ffaq-how-to-add-additional-entities-and-accounts-to-an-existing-cloudyn-subscription%3Fforum%3DCloudyn&data=02%7C01%7Cv-adchi%40microsoft.com%7C38db3ba29a1b446ddbdd08d72f918173%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637030174332184510&sdata=N9qN33pLErlATM%2F3kwkYCNbVgFf1LinruwausO1V5ys%3D&reserved=0)<br>
[How to enable additional users to access Cloudyn (and resolve account lockout issues)](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fsocial.msdn.microsoft.com%2FForums%2Fen-US%2F30afd40c-2a1d-44a7-b8d3-bc788ce36229%2Ffaq-how-to-enable-an-azure-user-to-use-cloudyn-when-you-receive-an-alert-requesting-to-allow-access%3Fforum%3DCloudyn&data=02%7C01%7Cv-adchi%40microsoft.com%7C38db3ba29a1b446ddbdd08d72f918173%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637030174332194504&sdata=nzTB%2F53VOWDzSmSx%2FG3lePv%2BQcFkHL6ehqJtYl%2FEPnk%3D&reserved=0)<br>

**Reasons for cost discrepancy between CSP and Cloudyn**<br>

There will be some difference in cost for CSP subscription in Cloudyn portal. In partner center portal, cost has been calculated as per local currency.<br>

There are some more reasons for cost discrepancy for CSP accounts in Cloudyn portal:

* CSP billing cycle may start anywhere during the month. Cloudyn’s month is always from the 1st of the month until the last month day (inclusive).
* CSP closes the cost calculation at some point during the last month day. So the monthly bill will always include some leftovers from the previous month and will always miss some cost from the end of the billing month. Cloudyn always calculates full day usage since at the time of Cloudyn’s calculation full usage data is already available.
* Partner Center presents costs according to CSP’s time zone. Cloudyn always calculates daily costs in UTC time.
* CSP may be charged in local currency. Cloudyn will always calculate costs in USD and the pricing differences may be more than the exchange rate differences.

Learn more: [FAQ: How to resolve apparent billing discrepancies between an Azure bill and Cloudyn reports](https://social.msdn.microsoft.com/Forums/azure/en-US/780bb6d5-99da-487f-96bb-849a83b45add/faq-how-to-resolve-apparent-billing-discrepancies-between-an-azure-bill-and-cloudyn-reports?forum=Cloudyn)


## **Recommended documents**

* How to [Assign access to Cloudyn data](https://docs.microsoft.com/azure/cost-management/tutorial-user-access)
* [Video: Adding Users to Cloudyn](https://youtu.be/Nzn7GLahx30)<br>
* [Video: Creating a Cost Entity Hierarchy in Cloudyn](https://youtu.be/dAd9G7u0FmU)<br>
* [Cloudyn Overview](https://docs.microsoft.com/azure/cost-management/overview)<br>
* [Cloudyn Pricing](https://azure.microsoft.com/pricing/details/cost-management)<br>
* [Cloudyn regional availability](https://azure.microsoft.com/global-infrastructure/services/)<br>
* [Cloudyn Training videos](https://docs.microsoft.com/azure/cost-management/ref-videos)<br>
