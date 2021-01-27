<properties
	pageTitle="File connectivity firewall errors"
	description="File connectivity firewall errors scoping questions"
	authors="Annayak"
	ms.author="annayak"
	selfHelpType="problemScopingQuestions"
	articleId="StorageScoping_file_connectivity_firewall"
	supportTopicIds="32688881"
	productPesIds="16460"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	ownershipId="StorageMediaEdge_StorageFiles"
/>
# File connectivity firewall errors
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Blob connectivity firewall errors scoping question",
    "fileAttachmentHint": "",
    "diagnosticCard": {
		"title": "Firewall & VNet Issues Troubleshooter",
		"description": "For Firewall & VNet issues, answer the following questions and give us a few minutes to run automated diagnostics. Using the diagnostics, we’ll provide a self-help solution for you.",
		"insightNotAvailableText": "Our automated troubleshooter did not detect any issues with your resource. Confirm that the answers provided are accurate and that they align with the input format suggested by watermark in the respective fields."
	},
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "Local start time of the latest occurrence",
            "required": true,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
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
	},
    {
			"id": "file_firewall_vnet_request_id",
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
		},
        {
            "id": "file_path",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "file path",
            "watermarkText": "File name or path if specific to a file",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional details",
            "required": true,
            "useAsAdditionalDetails": true,
            "diagnosticInputRequiredClients": "Portal,ASC"
        }
    ],
    "$schema": "SelfHelpContent"
}
---
