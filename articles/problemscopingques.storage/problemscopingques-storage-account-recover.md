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
	"resourceRequired": false,
	"title": "Recover deleted Storage Account",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "storage_account_name",
			"order": 1,
			"controlType": "textbox",
			"displayLabel": "Name of the deleted Storage Account",
			"required": true
		}, {
			"id": "storage_account_type",
			"order": 2,
			"controlType": "dropdown",
			"displayLabel": "Deployment type of Storage Account?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "ARM",
					"text": "Resource Manager"
				}, {
					"value": "Classic",
					"text": "Classic"
				}
			],
			"required": false
		}, {
			"id": "problem_start_date",
			"order": 3,
			"controlType": "datetimepicker",
			"displayLabel": "Date and time that the issue occured?",
			"required": false
		}, {
			"id": "additional_details",
			"order": 4,
			"controlType": "multilinetextbox",
			"displayLabel": "Provide any additional details",
			"required": false,
			"useAsAdditionalDetails": true,
			"hints": [{
					"text": "Issue description."
				}, {
					"text": "Additional details."
				}
			]
		}, {
			"id": "learn_more_text",
			"order": 5,
			"controlType": "infoblock",
			"content": "You can follow our <a href='https://docs.microsoft.com/azure/storage/common/storage-disaster-recovery-guidance?toc=%2fazure%2fstorage%2fblobs%2ftoc.json#best-practices-for-protecting-your-data'>best practices for protecting your data</a> to ensure that your deleted data will be recoverable in the future."
		}
	]
}
---