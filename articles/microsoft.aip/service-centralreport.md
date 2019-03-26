<properties
	pageTitle="Azure Information Service - Central Reporting"
	description="Azure Information Service - Central Reporting"
	service="microsoft.aip"
	resource="aip"
	authors="orbarak-ms"
	ms.author="orbarak"
	articleID="Central_Reporting"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32629568"
	resourceTags=""
	productPesIds="14997"
	cloudEnvironments="public"
/>

# Azure Information Protection service - Central Reporting

1. If you are not seeing data or receiving an error message when trying to access the Analytics Dashboard, please verify that you have the [Permissions required for Azure Information Protection analytics](https://docs.microsoft.com/azure/information-protection/reports-aip#permissions-required-for-azure-information-protection-analytics).
2. Make sure you meet all the [Prerequisites for Azure Information Protection analytics](https://docs.microsoft.com/azure/information-protection/reports-aip#prerequisites-for-azure-information-protection-analytics)
3. If you meet all prerequisites and you don't see any data, perform the steps below:

	1. Open AIP portal and navigate to the Policies blade
	2. For each policy you have, toggle the option of “Send audit data to Azure Information Protection analytics” to “Off” and save the policy
	3. For each policy you have, toggle the option of “Send audit data to Azure Information Protection analytics” to “On” and save the policy
	4. Go to your AIP client and reset settings (via Protect -> Help and Feedback -> Reset Settings)
	5. perform labeling actions, wait few minutes and see if data now arrives to the portal

## **Recommended Documents**

* [Central reporting for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/reports-aip)<br>
* [Prerequisites for Azure Information Protection analytics](https://docs.microsoft.com/azure/information-protection/reports-aip#prerequisites-for-azure-information-protection-analytics)<br>
* [Review Azure Information Protection subscriptions and features](https://azure.microsoft.com/pricing/details/information-protection)<br>
* [Requirements for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/get-started/requirements)<br>
* [Quick start tutorial for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/get-started/infoprotect-quick-start-tutorial)<br>
