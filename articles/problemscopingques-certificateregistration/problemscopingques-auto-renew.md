<properties
	pageTitle="Auto-renewal"
	description="Auto-renewal"
	supportTopicIds="32604391"
	authors="khaled-zayed"
	ms.author="khzayed"
	selfHelpType="problemScopingQuestions"
	productPesIds="16512"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="problemscopingques-auto-renew"
	ownershipId="Compute_AppService"
/>
# Auto-renewal
---
{
	"resourceRequired": false,
	"subscriptionRequired": true,
	"$schema": "SelfHelpContent",
	"title": "Auto-renewal",
	"fileAttachmentHint": "Please attach any relevant logs and screenshots",
	"formElements": [{
			"id": "problem_start_time",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "Incident time",
			"required": true
		},
			{
			"id": "2",
			"order": 2,
			"controlType": "textbox",
			"displayLabel": "If you received an email notification from update regarding your certificate, please paste the email here",
			"watermarkText": "...",
			"required": false
		},
		{
			"id": "3",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "Did the App Service Certificate fail to auto-renew?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Yes",
					"text": "Yes"
				}, {
					"value": "No",
					"text": "No"
				}
			],
			"required": false
		},
		{
			"id": "4",
			"order": 4,
			"controlType": "dropdown",
			"displayLabel": "Did the Web App fail to update with the new certificate",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Yes",
					"text": "Yes"
				}, {
					"value": "No",
					"text": "No"
				}
			],
			"required": false
		},
		{
			"id": "problem_description",
			"order": 5,
			"controlType": "multilinetextbox",
			"displayLabel": "Details",
			"watermarkText": "Provide additional information about your incident including any error messages you are seeing.",
			"required": true,
			"useAsAdditionalDetails": true
		}
	]
}
---