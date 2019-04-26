<properties
	articleId="01d9d342-3648-4876-ab5f-9b7b137993c6"
	pageTitle="Scoping for 7000-8000 Migration"
	description="7000-8000 Migration Scoping"
	authors="Archana-MSFT"
	ms.author="armukk"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630491"
	productPesIds="15438"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Scoping for 700-8000 Migration
---
{
	"resourceRequired": true,
	"subscriptionRequired": true,
	"title": "7000-8000 Migration",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "software version",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "Select the source appliance software version",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Version 2.1.1.518",
					"text": "Version 2.1.1.518"
				},{
					"value": "Version 2.1.1.548",
					"text": "Version 2.1.1.548"
				}, {
					"value": "Other",
					"text": "Other"
				},
			],
			"required": false
		}, {
			"id": "problem_start_time",
			"order": 4,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
		}, {
			"id": "serial number",
			"order": 2,
			"controlType": "textbox",
			"displayLabel": "Serial number of source appliance",
			"watermarkTest": "Serial number of 5000-7000 series appliance",
			"required": false
		}, {
			"id": "problem_description",
			"order": 5,
			"controlType": "multilinetextbox",
			"displayLabel": "Details",
			"watermarkText": "Provide additional information about your issue",
			"required": true,
			"useAsAdditionalDetails": true
		},
			{
			"id": "device name",
			"order": 1,
			"controlType": "dropdown",
			"displayLabel": "Destination device name",
			"watermarkText": "Choose destination device",
			"dynamicDropdownOptions": {
				"uri": "/subscriptions/{subscriptionid}/resourceGroups/{resourcegroup}/providers/Microsoft.StorSimple/managers/{resourcename}/devices?api-version=2018-07-01",
                "jTokenPath": "value",
                "textProperty": "id",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$"
			},
				"required": false
				},
		]
}
---
