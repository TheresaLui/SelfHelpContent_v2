<properties
	pageTitle="Azure Information Client - Can't apply this label error"
	description="Azure Information Client - Can't apply this label error"
	service="microsoft.aip"
	resource="aip"
	authors="nihendle"
	ms.author="nihendle, orbarak"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32584334"
	resourceTags=""
	productPesIds="14997"
	cloudEnvironments="public"
	articleId="a2e21818-3554-4ea5-bde3-5a02a3241ada"
/>

# Azure Information Protection client - can't apply this label error

## **Recommended Steps**

* If you created a new label that applies protection, it can take up to 15 minutes for a computer running the Azure Information Protection client to get these changed settings. Behind the scenes, this configuration creates a [protection template](https://docs.microsoft.com/azure/information-protection/deploy-use/refresh-templates).
* If you wait 15 minutes and still can't apply this label, select **Reset Settings** from the **Protect** button on the Office ribbon, then **Help and feedback**. This action signs out the user, deletes the currently downloaded Azure Information Protection policy, and resets the user settings for the Azure Rights Management service.
* If you are still experiencing the issue, collect Azure Information Protection client logs and attach the exported logs to this ticket

## Export Azure Information Protection logs

1. Open an Office document or create a new email in Outlook
2. Select the **Protect** button -> **Help and feedback**
3. Select **Export Logs**
4. Save the logs to your choice of location, and attach them to this service request

## **Recommended Documents**

* [Review Azure Information Protection documentation](https://docs.microsoft.com/azure/information-protection/what-is-information-protection)<br>
* [Review Azure Information Protection subscriptions and features](https://azure.microsoft.com/pricing/details/information-protection)<br>
* [Requirements for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/get-started/requirements)<br>
* [Quick start tutorial for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/get-started/infoprotect-quick-start-tutorial)<br>
* [Download Azure Information Protection client](https://www.microsoft.com/download/details.aspx?id=53018)<br>
