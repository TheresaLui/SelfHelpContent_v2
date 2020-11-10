<properties
	pageTitle="Question about index related service limits"
	description="Question about index related service limits"
	authors="cynotebo"
	ms.author="cynotebo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32681381"
	productPesIds="15568"
	cloudEnvironments="Public,MoonCake,FairFax, usnat, ussec"
	schemaVersion="1"
	articleId="513f9912-ad72-4d9c-91ca-b86d6cdfe3e3"
	ownershipId="AzureSearch_AzureSearch"
/>
# Question about index related service limits
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Question about index related service limits",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "index_error_message",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the exact error you received?",
            "required": false,
            "useAsAdditionalDetails": false
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
            "id": "service_tier",
            "order": 3,
            "controlType": "dropdown",
            "infoBalloonText": "string",
            "displayLabel": "What is the service tier/Sku of your service?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [{
                "value": "Free",
                "text": "Free"
              }, {
                "value": "Basic",
                "text": "Basic"
              }, {
                "value": "Standard",
                "text": "Standard 1, 2 or 3"
              }, {
                "value": "storage_optimzed",
                "text": "Storage optimized 1 or 2"
              },
                {
                "value": "dont know answer",
                "text": "Don't Know"
              }
            ],
            "required": false
        },
          {
		"id": "replica_count",
		"order": 4,
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
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 6,
            "controlType": "datetimepicker",
            "displayLabel": "When did you last attempt to delete the service?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
