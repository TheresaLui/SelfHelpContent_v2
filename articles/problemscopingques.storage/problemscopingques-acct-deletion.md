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
			"id": "resource_group_name",
			"order": 3,
            "visibility":"service_type == rg",
			"controlType": "textbox",
			"displayLabel": "Name of the resource group you are unable to delete",
            "watermarkText":"ResourceGroupName",
			"required": true
		}, {
			"id": "storage_account_name",
			"order": 4,
            "visibility":"service_type == account",
			"controlType": "textbox",
			"displayLabel": "Name of the storage account you are unable to delete",
            "watermarkText":"StorageAccountName1;StorageAccountName2; StorageAccountName3 ",
			"required": true
		}, {
			"id": "blob_container",
			"order": 5,
            "visibility":"service_type == blob_container || service_type == blob",
			"controlType": "dropdown",
			"displayLabel": "Blob Container",
            "watermarkText":"Choose an option",
			"dynamicDropdownOptions":{
				"uri":"/subscriptions/{subscriptionid}/resourceGroups/{resourcegroup}/providers/Microsoft.Storage/storageAccounts/{resourcename}/blobServices/default/containers?api-version=2018-07-01",
				"jTokenPath": "value",
				"textProperty": "id",
				"valueProperty": "id",
				"textPropertyRegex": "[^/]+$",
				"defaultDropdownOptions": {
					"value": "dont_know_answer",
					"text": "None of the above"
				},
				"dropdownOptions": [{
					"value": "NoBlobContainer",
					"text": "Not specific to a blob container"
				}],
			}
			"required": true
		}, {
			"id": "blob_path",
			"order": 6,
            "visibility":"service_type == blob",
			"controlType": "textbox",
			"displayLabel": "Blob path",
            "watermarkText":"https://myaccount.blob.core.windows.net/myblob",
			"required": true
		}, {
			"id": "file_share",
			"order": 7,
            "visibility":"service_type == file_share || service_type == file",
			"controlType": "dropdown",
			"displayLabel": "File Share",
            "watermarkText":"Select File Share",
			"dynamicDropdownOptions": {
				"uri" : "/subscriptions/{subscriptionid}/resourceGroups/{resourcegroup}/providers/Microsoft.Storage/storageAccounts/{resourcename}/fileServices/default/shares?api-version=2019-06-01",
				"jTokenPath" : "value",
				"textProperty": "name",
				"valueProperty": "name",
				"textPropertyRegex": "[^/]+$",
				"defaultDropdownOptions": {
					"value" : "dont_know_answer",
					"text" : "None of the above"
				}
			},
			"dropdownOptions":[{
				"value" : "NoFileShare",
				"text" : "NA"
			}],
			"required": true
		},  {
			"id": "file_path",
			"order": 8,
            "visibility":"service_type == file",
			"controlType": "textbox",
			"displayLabel": "File path",
            "watermarkText":"https://myaccount.blob.core.windows.net/myfile",
			"required": true
		}, {
			"id": "object_path",
			"order": 9,
            "visibility":"service_type == dont_know_answer || service_type == disk",
			"controlType": "textbox",
			"displayLabel": "Path of object you are unable to delete",
            "watermarkText":"https://myaccount.blob.core.windows.net/myobject",
			"required": true
		}, {
			"id": "problem_start_time",
			"order": 10,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
		}, {
			"id": "problem_description",
			"order": 11,
			"controlType": "multilinetextbox",
			"displayLabel": "Details",
			"watermarkText": "Provide additional information about your issue",
			"required": true,
			"useAsAdditionalDetails": true
		}
	]
}
---