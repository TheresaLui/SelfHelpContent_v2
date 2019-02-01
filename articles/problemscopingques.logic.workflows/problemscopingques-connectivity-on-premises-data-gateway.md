<properties
	articleId="problemscopingques-on-premises-data-gateway"
	pageTitle="Connectivity - On-Premises Data Gateway"
	description="Connectivity - On-Premises Data Gateway"
	supportTopicIds="32588741"
	authors="khaled-zayed"
	ms.author="khzayed"
	selfHelpType="problemScopingQuestions"
	productPesIds="15791"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# On-Premises Data Gateway
---
{
	"resourceRequired": false,
	"title": "Connectivity - On-Premises Data Gateway",
	"fileAttachmentHint": "Please export and attach the On-Premises Data Gateway log",
	"formElements": [{
			"id": "problem_start_date",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "Incident time",
			"required": true
		},
		{
			"id": "2",
			"order": 2,
			"controlType": "dropdown",
			"displayLabel": "Was this Logic App working previously?",
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
			"id": "3",
			"order": 3,
			"controlType": "textbox",
			"displayLabel": "Please provide one or more Run IDs related to this incident.",
			"watermarkText": "Run IDs...",
			"required": false,
		}, 
		{
			"id": "4",
			"order": 4,
			"controlType": "textbox",
			"displayLabel": "Please provide the resource IDs of Logic Apps with similar symptoms.",
			"watermarkText": "Resource IDs...",
			"required": false,
		},
		{
			"id": "5",
			"order": 5,
			"controlType": "textbox",
			"displayLabel": "Please provide the resource IDs of Logic Apps with the same overall structure and connectors that are not experiencing the same symptoms.",
			"watermarkText": "Resource IDs...",
			"required": false,
		},
		{
			"id": "problem_description",
			"order": 6,
			"controlType": "multilinetextbox",
			"displayLabel": "Details",
			"watermarkText": "Provide additional information about your issue including any error messages you are seeing.",
			"required": false,
			"useAsAdditionalDetails": true
		}
	]
}
---
