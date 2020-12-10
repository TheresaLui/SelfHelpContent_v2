<properties
	pageTitle="Issue querying an index with REST API"
	description="Issue querying an index with REST API"
	authors="cynotebo"
	ms.author="cynotebo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32681371"
	productPesIds="15568"
	cloudEnvironments="Public,MoonCake,FairFax, usnat, ussec"
	schemaVersion="1"
	articleId="b6ca0846-567d-423c-abeb-74f98faaaed7"
	ownershipId="AzureSearch_AzureSearch"
/>
# Issue querying an index with REST API
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Issue querying an index with REST API",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "index_error_message",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the exact error you received?",
            "required": false,
            "useAsAdditionalDetails": true
        },
        {
            "id": "index_failure",
            "order": 2,
            "controlType": "dropdown",
            "infoBalloonText": "string",
            "displayLabel": "Is failure across multiple indexes or just one?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [{
                "value": "Multiple indexes",
                "text": "Multiple indexes"
              }, {
                "value": "Just one",
                "text": "Just one"
              }, {
                "value": "dont know answer",
                "text": "Don't Know"
              }
            ],
            "required": false
        },
          {
		"id": "replica_count",
		"order": 3,
		"controlType": "dropdown",
		"infoBalloonText": "string",
		"displayLabel": "Do you have multiple replicas on this service?",
		"watermarkText": "Choose an option",
		"dropdownOptions": [{
				"value": "Yes",
				"text": "Yes"
			}, {
				"value": "No",
				"text": "No"
			}, {
				"value": "dont_know_answer",
				"text": "Don't Know"
			}
		],
		"required": false
	},
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details",
            "useAsAdditionalDetails": false,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "When did you last attempt to delete the service?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
