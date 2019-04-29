<properties
	articleId="336607b3-1ad8-402f-932e-15f027d257b0"
	pageTitle="Scoping for cannot trigger failover"
	description="Cannot trigger failover scoping"
	authors="Archana-MSFT"
	ms.author="armukk"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630496"
	productPesIds="15438"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# VM Performance
---
{
	"resourceRequired": true,
	"subscriptionRequired": true,
	"title": "cannot trigger failover",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "failover_component",
			"order": 1,
			"controlType": "dropdown",
			"displayLabel": "Which component are your trying to failover",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Volume container",
					"text": "Volume container"
				}, {
					"value": "Device",
					"text": "Device"
				},
		],
			"required": false
		}, {
			"id": "failover_to",
			"order": 2,
			"controlType": "dropdown",
			"displayLabel": "What is the destination of the failover",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Physical Device",
					"text": "Physical Device"
				}, {
					"value": "Cloud Appliance",
					"text": "Cloud Appliance"
				},
		],
			"required": false
		},{
			"id": "problem_start_time",
			"order": 3,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
		},  {
			"id": "problem_description",
			"order": 4,
			"controlType": "multilinetextbox",
			"displayLabel": "Details",
			"watermarkText": "Provide additional information about your issue",
			"required": true,
			"useAsAdditionalDetails": true
		},
	]
}
---
