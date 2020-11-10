<properties
	pageTitle="Create or Drop a Database"
	description="Create or Drop a Database"
	authors="Johirsch"
	ms.author="Johirsch"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630418"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="4AE9B6BF-D792-4068-8F4B-EA91F97D1A04"
	ownershipId="AzureData_AzureSQLDB_Provisioning"
/>

# Create or Drop a Database
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": false,
    "title": "Database",
    "fileAttachmentHint": "",
    "subscriptionRequired": false,
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controltype": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "watermarkText": "Specify when the problem started",
            "infoBalloonText": "Specify when the problem started",
            "required": true
        },
	{
	    "id": "attempt_method",
	    "order": 2,
	    "controlType": "dropdown",
	    "displayLabel": "What method are you using to create or drop the database?",
	    "required": true,
	    "dropdownOptions": [{
	            "value": "azure_portal",
		    "text": "Azure Portal"
		},
		{
		    "value": "powershell",
		    "text": "Powershell"
		},
		{
		    "value": "azure_cli",
		    "text": "Azure CLI"
		},
		{
		    "value": "dont_know_answer",
		    "text": "Unsure"
		}
	    ]
	},
        {
	    "id": "encountering_an_error",
	    "order": 3,
	    "controlType": "dropdown",
	    "displayLabel": "Are you encountering an error message?",
	    "dropdownOptions": [{
	            "value": "Yes",
		    "text": "Yes"
		},
		{
		    "value": "No",
		    "text": "No"
		},
		{
		    "value": "dont_know_answer",
		    "text": "Unsure"
		}
	    ],
	    "required": false
	},
	{
	    "id": "error_message",
	    "order": 4,
	    "controlType": "multilinetextbox",
	    "displayLabel": "Please provide this error message",
	    "required": false,
	    "visibility": "encountering_an_error == Yes"
	},
        {
            "id": "problem_description",
            "order": 5,
            "controltype": "multilinetextbox",
            "displayLabel": "Any additional details you would like to include?",
            "watermarkText": "Enter any additional details here",
            "infoBalloonText": "Enter any additional details here",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ]
}
---
