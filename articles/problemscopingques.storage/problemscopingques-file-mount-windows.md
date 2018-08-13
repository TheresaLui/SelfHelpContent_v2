<properties
	pageTitle="Storage File Share mounting issues - Windows"
	description="Storage File Share mounting issues - Windows"
	authors="Passaree"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32602765"
	productPesIds="16460"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Storage File Share mounting issues - Windows
---
{
	"resourceRequired": false,
	"title": "Storage File Share mounting issues - Windows",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "mount_location",
			"order": 1,
			"controlType": "dropdown",
			"displayLabel": "Location where File Share is being mounted",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "same_region",
					"text": "Azure VM is in same region as the Azure File Share"
				}, {
					"value": "different_region",
					"text": "Azure VM is in different region than the Azure File Share"
				}, {
					"value": "on_premises",
					"text": "Client is outside Azure"
				}
			],
			"required": true
		}, {
			"id": "os_version",
			"order": 2,
			"controlType": "dropdown",
			"displayLabel": "Windows version where File Share is being mounted",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "windows7",
					"text": "Windows 7"
				}, {
					"value": "windows8",
					"text": "Windows 8 or above"
				}, {
					"value": "server2008R2",
					"text": "Windows Server 2008 R2"
				}, {
					"value": "server2012",
					"text": "Windows Server 2012 or above"
				}, {
					"value": "old_windows",
					"text": "Below Windows 7 or Windows Server 2008 R2"
				}
			],
			"required": true
		}, {
			"id": "additional_details",
			"order": 3,
			"controlType": "multilinetextbox",
			"displayLabel": "Provide any additional details",
			"required": false,
			"useAsAdditionalDetails": true
		}
	]
}
---