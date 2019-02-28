<properties
	pageTitle="Azure Information Protection - Labels are not being applied as expected"
	description="Azure Information Protection - Labels are not being applied as expected"
	service="microsoft.aip"
	resource="aip"
	authors="orbarak-ms"
	ms.author="orbarak"
	articleId="Scanner_Labels_are_not_being_applied_as_expected"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32629560"
	resourceTags=""
	productPesIds="14997"
	cloudEnvironments="public"
/>

# Azure Information Protection - Labels are not being applied as expected

## **Recommended Steps**

1. Make sure your [policies are set](https://docs.microsoft.com/azure/information-protection/configure-policy) to automatic labeling or have a default label in the policy
2. Open the relevant document in Office and verify if the intended label is being applied
3. If you're still experiencing the issue, collect Azure Information Protection scanner logs and attach the exported logs to a support ticket

### Export Azure Information Protection Scanner logs

1. Navigate to `%localappdata%\Microsoft\MSIP` under the user context running the scanner service
2. Zip all the contents under the MSIP folder
3. Save the logs to your choice of location, and attach them to your service request

## **Recommended Documents**

* [How-to guides for common scenarios that use Azure Information Protection](https://docs.microsoft.com/azure/information-protection/how-to-guides)<br>
* [Review Azure Information Protection documentation](https://docs.microsoft.com/azure/information-protection/configure-policy)<br>
* [Deploying the Azure Information Protection scanner to automatically classify and protect files](https://docs.microsoft.com/azure/information-protection/deploy-aip-scanner)<br>
* [Requirements for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/get-started/requirements)<br>
* [Download Azure Information Protection client](https://www.microsoft.com/download/details.aspx?id=53018)
