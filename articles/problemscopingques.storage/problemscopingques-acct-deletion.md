<properties
	pageTitle="Unable to delete storage object scoping"
	description="Unable to delete storage object scoping questions"
	ms.author="leakkari"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32602694"
	productPesIds="15629"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	articleId="B01011DA-7565-4574-BD0C-35E9C749D8D1"
	ownershipId="StorageMediaEdge_AccountManagement"
/>
# Issue deleting storage object
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": true,
  "resourceRequired": true,
	"title": "Unable to delete storage object",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "service_type",
			"order": 1,
			"controlType": "dropdown",
			"displayLabel": "Type of storage object",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "rg",
					"text": "Resource group"
				}, {
					"value": "account",
					"text": "Storage account"
				}, {
					"value": "blob_container",
					"text": "Blob container"
				}, {
					"value": "file_share",
					"text": "File Share"
				}, {
					"value": "blob",
					"text": "Blob"
				}, {
					"value": "file",
					"text": "File"
				},{
					"value": "disk",
					"text": "Disk"
				},{
					"value": "dont_know_answer",
					"text": "Don't Know"
				}
			],
			"required": true
		}, {
			"id": "rg_name",
			"order": 2,
            "visibility":"service_type == rg",
			"controlType": "textbox",
			"displayLabel": "Name of the resource group you are unable to delete",
            "watermarkText":"ResourceGroupName",
			"required": true
		}, {
			"id": "problem_start_time",
			"order": 2,
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
			"useAsAdditionalDetails": true,
		}
	]
}
---