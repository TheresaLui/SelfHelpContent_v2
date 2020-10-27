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
	articleId=""
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
	"formElements": [{
			"id": "problem_description",
			"order": 1,
			"controlType": "multilinetextbox",
			"displayLabel": "search_service_replicas",
			"watermarkText": "How many replicas does your search service contain",
			"required": false,
			"useAsAdditionalDetails": true,
		}, {       
      "id": "scoring_profiles",
			"order": 2,
			"controlType": "dropdown",
			"infoBalloonText": "string",
			"displayLabel": "Are you using scoring profiles?",
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
		}, {
			"id": "query_runtime",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "Where are you running your query from?",
			"dropdownOptions": [{
					"value": "Azure Portal",
					"text": "Azure Portal"
				}, {
					"value": "REST API",
					"text": "REST API"
				}, {
					"value": "MY own code",
					"text": "My own code"
				}, {
					"value": "Other (describe below)",
					"text": "Other"
				}
			],
			"required": false
		}, {
			"id": "problem_description",
			"order": 4,
			"controlType": "multilinetextbox",
			"displayLabel": "Details",
			"watermarkText": "Provide additional information about your issue",
			"required": true,
			"useAsAdditionalDetails": true,
    }, {
			"id": "problem_start_time",
			"order": 5,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
		}
	]
}
