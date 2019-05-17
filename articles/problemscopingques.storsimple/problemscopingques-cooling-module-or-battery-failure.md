<properties
	articleId="1fa746d0-22d2-42bf-a404-95fe2ac4da38"
	pageTitle="Scoping cooling module or battery failure"
	description="Cooling module or battery failure scoping"
	authors="Archana-MSFT"
	ms.author="armukk"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630505"
	productPesIds="15438"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Cooling module or battery failure
---
{
	"resourceRequired": true,
	"subscriptionRequired": true,
	"title": "pcm",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "pcm_slot",
			"order": 1,
			"controlType": "dropdown",
			"displayLabel": "Select the PCM that has failed or degraded",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "PCM 0",
					"text": "PCM 0"
				}, {
					"value": "PCM 1",
					"text": "PCM 1"
				}
			],
			"required": false
		}, {
			"id": "battery_slot",
			"order": 2,
			"controlType": "dropdown",
			"displayLabel": "Select the PCM in which the battery has failed or degraded",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "PCM 0",
					"text": "PCM 0"
				}, {
					"value": "PCM 1",
					"text": "PCM 1"
				}
			],
			"required": false
		},{
			"id": "problem_start_time",
			"order": 3,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
		}, {
			"id": "problem_description",
			"order": 4,
			"controlType": "multilinetextbox",
			"displayLabel": "Details",
			"watermarkText": "Provide additional information about your issue",
			"required": true,
			"useAsAdditionalDetails": true
		}
	]
}
---
