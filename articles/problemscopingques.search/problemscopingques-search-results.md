<properties
	pageTitle="I'm not getting the search results I expect"
	description="I'm not getting the search results I expected"
	authors="cynotebo"
	ms.author="cynotebo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32681380"
	productPesIds="15568"
	cloudEnvironments="Public,MoonCake,FairFax, usnat, ussec"
	schemaVersion="1"
	articleId="25e33773-8fa7-4cdb-883e-bbf33da337a9"
  ownershipId="AzureSearch_AzureSearch"
/>
# I"m not getting the search results I expected
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": true,
  "resourceRequired": true,
	"title": "Search results are not as expected",
	"fileAttachmentHint": "",
	"formElements": [
	  {
			"id": "scoring_profiles",
			"order": 1,
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
			"order": 2,
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
			"order": 3,
			"controlType": "multilinetextbox",
			"displayLabel": "Details",
			"watermarkText": "Provide additional information about your issue",
			"required": true,
			"useAsAdditionalDetails": true
    		}, {
			"id": "problem_start_time",
			"order": 4,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
	}
    ],
    "$schema": "SelfHelpContent"
}
---
