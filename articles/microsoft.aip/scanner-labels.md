<properties
	pageTitle="Azure Information Protection - Labels are not being applied as expected"
	description="Azure Information Protection - Labels are not being applied as expected"
	service="microsoft.aip"
	resource="aip"
	authors="orbarak"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32629560"
	resourceTags=""
	productPesIds="14997"
	cloudEnvironments="public"
/>

# Azure Information Protection - Labels are not being applied as expected

## Recommended troubleshooting steps

1. Make sure your policies are set to automatic labeling or have a default label in the policy [Configuring the Azure Information Protection policy] (https://docs.microsoft.com/en-us/azure/information-protection/configure-policy)
2. Open the relevant document in Office and verify if the intended label is being applied

If you still experience the issue, collect Azure Information Protection scanner logs and attach the exported logs to this ticket.

## How to export Azure Information Protection Scanner logs

1. Navigate to %localappdata%\Microsoft\MSIP under the user context running the scanner service
2. Zip all the contents under the MSIP folder
3. Save the logs to your choice of location, and attach them to this service request

## **Recommended documents**

[Review Azure Information Protection documentation](https://aka.ms/aipdocs)<br>
[Deploying the Azure Information Protection scanner to automatically classify and protect files](https://docs.microsoft.com/en-us/azure/information-protection/deploy-aip-scanner)<br>
[Requirements for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/get-started/requirements)<br>
[Download Azure Information Protection client](http://aka.ms/aipclient)<br>