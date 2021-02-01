<properties
	pageTitle="Search Results Order"
	description="Search results are not in the order I expected"
	authors="cynotebo"
	ms.author="cynotebo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32681348"
	productPesIds="15568"
	cloudEnvironments="Public,MoonCake,FairFax, usnat, ussec"
	schemaVersion="1"
	articleId="8c973d72-b6fc-419d-bad5-7607564d1713"
  ownershipId="AzureSearch_AzureSearch"
/>
# Search Results Not in Order Expected
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": true,
  "resourceRequired": true,
	"title": "Search Results Not in Order Expected",
	"fileAttachmentHint": "",
	"formElements": [
	  {
		"id": "replica_count",
		"order": 1,
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
     			"id": "scoring_profiles",
			"order": 2,
			"controlType": "dropdown",
			"infoBalloonText": "string",
			"displayLabel": "Are you using scoring profiles?",
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
		}, {
			"id": "query_runtime",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "Where are you running your query from?",
			"dropdownOptions": [{
					"value": "Azure_Portal",
					"text": "Azure Portal"
				}, {
					"value": "REST_API",
					"text": "REST API"
				}, {
					"value": "Custom client using Management API or SDK",
					"text": "Custom client using Management API or SDK"
				},
				 {
                   			 "value": "dont_know_answer",
                   			 "text": "Don't Know"
              			  }
			],
			"required": true
		}, {
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
