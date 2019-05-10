<properties
	articleId="d5021901-0901-4fea-a25b-3d65e70531da"
	pageTitle="Scoping for controller offline in portal"
	description="Controller offline in portal scoping"
	authors="Archana-MSFT"
	ms.author="armukk"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630497"
	productPesIds="15438"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Controller offline in protal
---
{
	"resourceRequired": true,
	"subscriptionRequired": true,
	"title": "Slow virtual machine",
	"fileAttachmentHint": "",
	"formElements": [{
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
				"dropdownOptions": [
					{
						"value": "NoDestinationDevice",
						"text": "Not specific to a destination device"
					}
				],
				"required": false
		}, {
			"id": "controller",
			"order": 2,
			"controlType": "dropdown",
			"displayLabel": "Select the controller that is shown offline",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Controller 0",
					"text": "Controller 0"
				}, {
					"value": "Controller 1",
					"text": "Controller 1"
				}
			],
			"required": false
		}, {
			"id": "serial_access",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "Do you have access to the device through the serial console",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Yes",
					"text": "Yes"
				}, {
					"value": "Yes",
					"text": "Yes"
				}
			],
			"required": false
		},{
			"id": "problem_start_time",
			"order": 4,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
		}, {
			"id": "problem_description",
			"order": 5,
			"controlType": "multilinetextbox",
			"displayLabel": "Details",
			"watermarkText": "Provide additional information about your issue",
			"required": true,
			"useAsAdditionalDetails": true
		}
	]
}
---
