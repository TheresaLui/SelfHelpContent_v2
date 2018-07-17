<properties
	pageTitle="Storage Firewall and VNet"
	description="Storage Firewall and VNet scoping question"
	authors="Passaree"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32602697"
	productPesIds="15629"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Storage Firewall and VNet
---
{
	"resourceRequired": true,
	"title": "Storage Firewall and VNet scoping question",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "application_type",
			"order": 1,
			"controlType": "multiselectdropdown",
			"displayLabel": "If your service/application is not working after configuring Firewall, choose what was impacted",
			"watermarkText": "Choose what was impacted",
			"dropdownOptions": [{
					"value": "Azure_Storage",
					"text": "Azure Storage operations not working, e.g. copy, Disk import/export"
				}, {
					"value": "Azure_Internal",
					"text": "Other Azure or Microsoft Services not working"
				}, {
					"value": "Azure_ThirdParty",
					"text": "Third party services running in Azure VM not working"
				}, {
					"value": "External_ThirdParty",
					"text": "Third party services running outside Azure not working"
				}
			],
			"required": false
		}, {
			"id": "application_name",
			"order": 2,
			"controlType": "textbox",
			"displayLabel": "Name of impacted service/application",
			"watermarkText": "service/application name",
			"required": false
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
