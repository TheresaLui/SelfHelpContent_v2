<properties
	pageTitle="Blob connectivity firewall errors"
	description="Blob connectivity firewall errors scoping questions"
	authors="Annayak"
	ms.author="passAnnayakap"
	selfHelpType="problemScopingQuestions"
	articleId="StorageScoping_blob_connectivity_firewall"
	supportTopicIds="32688878"
	productPesIds="16459"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>
# Blob connectivity firewall errors
---
{
	"subscriptionRequired": true,
	"resourceRequired": true,
	"title": "Blob connectivity firewall errors scoping question",
	"fileAttachmentHint": "",
	"diagnosticCard": {
		"title": "Firewall & VNet Issues Troubleshooter",
		"description": "For Firewall & VNet issues, help us by providing your input and by giving us a few minutes to run automated diagnostics. We can help diagnose your problem and recommend the solution without needing to open a support ticket.",
		"insightNotAvailableText": "Our automated troubleshooter did not detect any issues with your resource. You can help us by providing the right inputs below and ensuring that the format is as suggested in the watermark."
	},
	"formElements": [{
		"id": "problem_start_time",
		"order": 1,
		"controlType": "datetimepicker",
		"displayLabel": "Local start time of the latest occurrence",
		"required": true,
		"diagnosticInputRequiredClients": "Portal,ASC"
	}, {
		"id": "error_code_dropdown",
		"order": 2,
		"controlType": "dropdown",
		"displayLabel": "Error code",
		"watermarkText": "HTTP error of failed operation",
		"dropdownOptions": [{
			"value": "HTTP_304",
			"text": "HTTP 304"
		}, {
			"value": "HTTP_400",
			"text": "HTTP 400"
		}, {
			"value": "HTTP_403",
			"text": "HTTP 403"
		}, {
			"value": "HTTP_404",
			"text": "HTTP 404"
		}, {
			"value": "HTTP_405",
			"text": "HTTP 405"
		}, {
			"value": "HTTP_409",
			"text": "HTTP 409"
		}, {
			"value": "HTTP_411",
			"text": "HTTP 411"
		}, {
			"value": "HTTP_412",
			"text": "HTTP 412"
		}, {
			"value": "HTTP_413",
			"text": "HTTP 413"
		}, {
			"value": "HTTP_415",
			"text": "HTTP 415"
		}, {
			"value": "HTTP_416",
			"text": "HTTP 416"
		}, {
			"value": "HTTP_500",
			"text": "HTTP 500"
		}, {
			"value": "HTTP_501",
			"text": "HTTP 501"
		}, {
			"value": "HTTP_502",
			"text": "HTTP 502"
		}, {
			"value": "HTTP_503",
			"text": "HTTP 503"
		}, {
			"value": "dont_know_answer",
			"text": "Not listed above "
		}],
		"defaultDropdownOptions": {
			"value": "HTTP_403",
			"text": "HTTP 403"
		},
		"required": true,
		"diagnosticInputRequiredClients": "Portal,ASC"
	}, {
			"id": "blob_firewall_vnet_request_id",
			"order": 3,
			"controlType": "textbox",
			"displayLabel": "Storage server request ID",
			"watermarkText": "Server Request ID of failed operation ending with 000000",
			"infoBalloonText": "Server Request ID of failed operation ending with 000000(6 zeros). It's part of every response that is sent back by storage.",
			"required": false,
			"diagnosticInputRequiredClients": "Portal,ASC",
			"validations": [{
				"type": "RegExMatch",
				"value": "^([0-9A-Za-z]{8}[-][0-9A-Za-z]{4}[-][0-9A-Za-z]{4}[-][0-9A-Za-z]{4}[-][0-9A-Za-z]{6}[0]{6})$",
				"text": "Server Request ID always ends 000000(6 zeros) e.g 05b2d321-403q-0037-4f62-2ag1aa000000"
			}]
		}, {
		"id": "blob_container",
		"order": 4,
		"controlType": "dropdown",
		"displayLabel": "Blob container",
		"watermarkText": "Choose an option",
		"dynamicDropdownOptions": {
			"uri": "/subscriptions/{subscriptionid}/resourceGroups/{resourcegroup}/providers/Microsoft.Storage/storageAccounts/{resourcename}/blobServices/default/containers?api-version=2018-07-01",
			"jTokenPath": "value",
			"textProperty": "id",
			"valueProperty": "id",
			"textPropertyRegex": "[^/]+$",
			"defaultDropdownOptions": {
				"value": "dont_know_answer",
				"text": "None of the above"
			}
		},
		"dropdownOptions": [{
			"value": "NoBlobContainer",
			"text": "Not specific to a blob container"
		}],
		"required": false,
		"diagnosticInputRequiredClients": "Portal,ASC"
	}, {
		"id": "blob_path",
		"order": 5,
		"controlType": "textbox",
		"displayLabel": "Blob path",
		"watermarkText": "Blob name or path if specific to a blob",
		"required": false,
		"diagnosticInputRequiredClients": "Portal,ASC"
	}, {
		"id": "problem_description",
		"order": 6,
		"controlType": "multilinetextbox",
		"displayLabel": "Provide any additional details",
		"required": true,
		"useAsAdditionalDetails": true,
		"diagnosticInputRequiredClients": "Portal,ASC"
	}],
	"$schema": "SelfHelpContent"
}
---
