<properties
	articleId="problemscopingques-misroutehandling"
	pageTitle="Azure Firewall Generic"
	description="Azure Firewall Generic"
	authors="spacest"
	ms.author="mariliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32628805,32608919,32608920,32628807,32628806,32608924,32608918,32608921,32608922,32608917"
	productPesIds="16556"
	cloudEnvironments="public"
	schemaVersion="1"
/>
#This file applies to all STs in Azure Firewall to reduce customer and engineer support pain.
---
{
	"formElements": [{
			"id": "is_it_AzureFirewall",
			"order": 1,
			"controlType": "dropdown",
			"displayLabel": "Is this case related to the Azure Firewall service?",
			"dropdownOptions": [{
					"value": "Yes",
					"text": "Yes"
				}, {
					"value": "No",
					"text": "No"
				}, 
			],
			"required": true
		}, {
			"id": "is_it_deployed",
			"order": 2,
			"controlType": "dropdown",
			"displayLabel": "Is Azure Firewall deployed in your subscription?",
			"dropdownOptions": [{
					"value": "Yes",
					"text": "Yes"
				}, {
					"value": "No",
					"text": "No"
				}, 
			],
			"required": true
		}, {
			"id": "problem_start_time",
			"order": 3,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem start?",
			"required": true
		}, {
			"id": "problem_description",
			"order": 4,
			"controlType": "multilinetextbox",
			"displayLabel": "Description",
			"watermarkText": "Provide additional information about your issue",
			"required": true,
			"useAsAdditionalDetails": true,
			
		}
	]
}
---
