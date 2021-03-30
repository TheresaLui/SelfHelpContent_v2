<properties
	pageTitle="Issue with debug sessions"
	description="Issue with debug sessions"
	authors="cynotebo"
	ms.author="cynotebo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32781151"
	productPesIds="15568"
	cloudEnvironments="Public,MoonCake,FairFax, usnat, ussec"
	schemaVersion="1"
	articleId="ec4dcdcf-96e9-446b-b1ae-46de865fbc16"
  ownershipId="AzureSearch_AzureSearch"
/>
# Issue with debug sessions (preview)
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": true,
  "resourceRequired": true,
	"title": "Issue with debug sessions (preview)",
	"fileAttachmentHint": "",
	"formElements": [
	  {
            "id": "error_message",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the exact error message you received?",
            "required": true,
            "useAsAdditionalDetails": false
          },
	  {
		"id": "debug_error_session",
		"order": 2,
		"controlType": "dropdown",
		"infoBalloonText": "string",
		"displayLabel": "Are all debug sessions failing or just a combination of document parameters?",
		"watermarkText": "Choose an option",
		"dropdownOptions": [{
				"value": "Yes",
				"text": "Yes"
			},{
				"value": "No",
				"text": "No"
			},{
				"value": "dont_know_answer",
				"text": "Don't Know"
		        }
	        ],
		"required": false
	    },
		{
     			"id": "data_access",
			"order": 3,
			"controlType": "dropdown",
			"infoBalloonText": "string",
			"displayLabel": "Does the search service have access to the data?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [
				{
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
			"displayLabel": "Details",
			"watermarkText": "Provide additional information about your issue",
			"required": true,
			"useAsAdditionalDetails": true
    }, {
			"id": "problem_start_time",
			"order": 5,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
	}
    ],
    "$schema": "SelfHelpContent"
}
---
