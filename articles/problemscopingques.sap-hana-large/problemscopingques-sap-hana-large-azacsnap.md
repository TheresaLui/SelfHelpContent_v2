<properties
    pageTitle="Azure Application Consistent Snapshot tool (AzAcSnap)"
    description="Azure Application Consistent Snapshot tool (AzAcSnap) on SAP HANA on Azure Large Instances"
    authors="johnnygetHub"
    ms.author="johnnyc"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32784500"
    productPesIds="16208"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="0ab72ddc-ebc5-4e7d-b1bf-889645dab2b2"
	ownershipId="AzureKeyVault_MHSM"
/>


# SAP HANA on Azure Large Instances
---
{
	"subscriptionRequired": true,
	"resourceRequired": false,
	"title": "Azure Application Consistent Snapshot tool (AzAcSnap)",
	"fileAttachmentHint": "Creating AzAcSnap Log File: https://docs.microsoft.com/azure/azure-netapp-files/azacsnap-troubleshoot#log-files",
	"formElements": [
		{
			"id": "problem_start_time",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
		},
		{
			"id": "problem_description",
			"order": 2,
			"controlType": "multilinetextbox",
			"displayLabel": "Please provide additional details",
			"required": true,
			"useAsAdditionalDetails": true,
			"hints": [
				{
					"text": "Please provide a brief description of the problem."
				},
				{
					"text": "Note: Make sure you have selected the subscription which contains the SAP HANA Instance while creating this case"
				}
			]
		},
		{
			"id": "radio_button",
			"order": 3,
			"controlType": "radioButtonGroup",
			"infoBalloonText": "Creating AzAcSnap Log File: https://docs.microsoft.com/azure/azure-netapp-files/azacsnap-troubleshoot#log-files",
			"watermarkText": "Upload Log File",
			"displayLabel": "Did you upload Log File here",
			"radioButtonOptions": [{
					"value": "NoLog",
					"text": "No"
				},
				{
					"value": "YesLog",
					"text": "Yes"
				}
			],
			"required": true
		}
	],
	"$schema": "SelfHelpContent"
}
---
