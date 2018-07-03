<properties
	pageTitle="Recover deleted Storage Account"
	description="Recover deleted Storage Account scoping question"
	authors="Passaree"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32602701"
	productPesIds="15629"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Recover deleted Storage Account
---
{
	"resourceRequired": true,
	"title": "Storage Account recovery scoping question",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "warning_same_name",
			"order": 1,
			"controlType": "infoblock",
			"content": "Do not recreate Storage Account with the same name while we attempt to recover it."
		}, {
			"id": "storage_account_name",
			"order": 2,
			"controlType": "textbox",
			"displayLabel": "Name of the deleted Storage Account",
			"required": true
		}, {
			"id": "storage_account_type",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "Deployment model",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "ARM",
					"text": "Resource Manager (ARM)"
				}, {
					"value": "Classic",
					"text": "Classic"
				}
			],
			"required": false
		}, {
			"id": "storage_account_region",
			"order": 4,
			"controlType": "textbox",
			"displayLabel": "Region of Storage Account",
			"required": false
		}, {
			"id": "problem_start_date",
			"order": 5,
			"controlType": "datetimepicker",
			"displayLabel": "Date and time that the account was deleted",
			"required": false
		}, {
			"id": "additional_details",
			"order": 6,
			"controlType": "multilinetextbox",
			"displayLabel": "Provide any additional details",
			"required": false,
			"useAsAdditionalDetails": true
		}, {
			"id": "learn_more_text",
			"order": 7,
			"controlType": "infoblock",
			"content": "You can follow our <a href='https://docs.microsoft.com/azure/storage/common/storage-disaster-recovery-guidance?toc=%2fazure%2fstorage%2fblobs%2ftoc.json#best-practices-for-protecting-your-data'>best practices for protecting your data</a> to ensure that your deleted data will be recoverable in the future."
		}
	]
}
---