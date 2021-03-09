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
			"order": 3,
            "visibility":"service_type == rg",
			"controlType": "textbox",
			"displayLabel": "Name of the resource group you are unable to delete",
            "watermarkText":"ResourceGroupName",
			"required": true
		}, {
			"id": "account_name",
			"order": 4,
            "visibility":"service_type == account",
			"controlType": "textbox",
			"displayLabel": "Name of the storage account you are unable to delete",
            "watermarkText":"StorageAccountName1;StorageAccountName2; StorageAccountName3 ",
			"required": true
		}, {
			"id": "blobcontainer_name",
			"order": 5,
            "visibility":"service_type == blob_container",
			"controlType": "textbox",
			"displayLabel": "Name of blob container you are unable to delete",
            "watermarkText":"container1;container2; container3 ",
			"required": true
		}, {
			"id": "fileshare_name",
			"order": 6,
            "visibility":"service_type == file_share",
			"controlType": "textbox",
			"displayLabel": "Name of file share you are unable to delete",
            "watermarkText":"fileshare1;fileshare2; fileshare3 ",
			"required": true
		}, {
			"id": "blob_name",
			"order": 7,
            "visibility":"service_type == blob",
			"controlType": "textbox",
			"displayLabel": "Blob path",
            "watermarkText":"https://myaccount.blob.core.windows.net/myblob",
			"required": true
		}, {
			"id": "file_name",
			"order": 8,
            "visibility":"service_type == file",
			"controlType": "textbox",
			"displayLabel": "File path",
            "watermarkText":"https://myaccount.blob.core.windows.net/myfile",
			"required": true
		}, {
			"id": "disk_name",
			"order": 9,
            "visibility":"service_type == disk",
			"controlType": "textbox",
			"displayLabel": "Disk path",
            "watermarkText":"https://myaccount.blob.core.windows.net/mydisk",
			"required": true
		}, {
			"id": "dont_know",
			"order": 10,
            "visibility":"service_type == dont_know_answer",
			"controlType": "textbox",
			"displayLabel": "Path of object you are unable to delete",
            "watermarkText":"https://myaccount.blob.core.windows.net/myobject",
			"required": true
		},{
			"id": "problem_start_time",
			"order": 11,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
		}, {
			"id": "problem_description",
			"order": 12,
			"controlType": "multilinetextbox",
			"displayLabel": "Details",
			"watermarkText": "Provide additional information about your issue",
			"required": true,
			"useAsAdditionalDetails": true
		}
	]
}
---