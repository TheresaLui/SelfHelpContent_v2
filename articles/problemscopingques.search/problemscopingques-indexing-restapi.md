<properties
	pageTitle="Issue indexing documents using REST API"
	description="Issue indexing documents using REST API"
	authors="cynotebo"
	ms.author="cynotebo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32681367"
	productPesIds="15568"
	cloudEnvironments="Public,MoonCake,FairFax, usnat, ussec"
	schemaVersion="1"
	articleId="266f3ac6-4c3d-4d73-85a1-a6380e2f549d"
	ownershipId="AzureSearch_AzureSearch"
/>
# Issue indexing documents using REST API
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
            "id": "replica_count",
            "order": 2,
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
			"required": true
		  },
       {
            "id": "ai_skills",
            "order": 3,
            "controlType": "dropdown",
            "infoBalloonText": "string",
            "displayLabel": "Are you using AI skills with this index?",
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
			"required": true
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
