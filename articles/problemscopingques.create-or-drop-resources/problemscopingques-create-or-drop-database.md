<properties
	pageTitle="Create or Drop a Database"
	description="Create or Drop a Database"
	authors="Johirsch"
	ms.author="Johirsch"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630418"
	productPesIds="13491"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="problemscopingques-createordropdatabase"
/>

# Create or Drop a Database
---
{
    "resourceRequired": true,
    "title": "Database",
    "fileAttachmentHint": "",
    "subscriptionRequired": true,
    "formElements": [
        {
	    "id": "encountering_an_error",
	    "order": 1,
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
	    "order": 2,
	    "controlType": "multilinetextbox",
	    "displayLabel": "Please provide this error message",
	    "required": false,
	    "visibility": "encountering_an_error == Yes"
	},
	{
	    "id": "attempt_method",
	    "order": 3,
	    "controlType": "multilinetextbox",
	    "displayLabel": "How are you attempting the operation that throws this error?",
	    "required": false,
	    "visibility": "encountering_an_error == Yes"
	},
        {
            "id": "problem_description",
            "order": 4,
            "controltype": "multilinetextbox",
            "displayLabel": "Any additional details you would like to include?",
            "watermarkText": "Enter any additional details here",
            "infoBalloonText": "Enter any additional details here",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "problem_start_time",
            "order": 5,
            "controltype": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "watermarkText": "Specify when the problem started",
            "infoBalloonText": "Specify when the problem started",
            "required": true,
            "useAsAdditionalDetails": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
