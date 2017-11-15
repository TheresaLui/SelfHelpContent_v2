<properties
	pageTitle="Cannot Connect to or from Internet"
	description="Cannot Connect to or from Internet"
	authors="ritup"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32584250"
	productPesIds="15526"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Cannot Connect to or from Internet
---
{
	"resourceRequired": true,
	"title": "Cannot Connect to or from Internet",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "cannot_connect_vm",
			"order": 1,
			"controlType": "dropdown",
			"displayLabel": "Please select the VM you are not able to connect to?",
			"watermarkText": "Choose an option",
			"dynamicDropdownOptions": {
					"uri": "/subscriptions/{subscriptionid}/resourceGroups/{resourcegroup}/providers/Microsoft.Network/virtualNetworks/{resourcename}/virtualMachines/$ref?api-version=2017-09-01",
					"jTokenPath": "value",
					"textProperty": "id",
					"valueProperty": "id"
					},
			"dropdownOptions": [{
					"value": "Unable to get the list of VM's",
					"text": "Unable to get the list of VM's"
				}
			],
			"required": false
		}, {
			"id": "problem_start_date",
			"order": 2,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": false
		}, {
			"id": "additional_details",
			"order": 5,
			"controlType": "multilinetextbox",
			"displayLabel": "Please provide these details",
			"required": false,
			"useAsAdditionalDetails": true,
			"hints": [{
					"text": "Connectivity direction impacted."
				}, {
					"text": "Are you able to communicate between Vm's within the VNET."
				}
			]
		}
	]
}
---
