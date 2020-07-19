<properties
	pageTitle="Unexpected output in Azure Stream Analytics"
	description="Unexpected output in Azure Stream Analytics"
	authors="sidramadoss"
	ms.author="sidram"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32357244"
	productPesIds="15663"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="problemscopingques-unexpectedoutput"
	ownershipId="AzureData_StreamAnalytics"
/>
# Unexpected output in Azure Stream Analytics
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": true,
  "resourceRequired": true,
	"title": "Unexpected output in Azure Stream Analytics",
	"fileAttachmentHint": "",
	"formElements": [
         {
			"id": "problem_start_time",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
		},{
			"id": "problem_description",
			"order": 2,
			"controlType": "multilinetextbox",
			"displayLabel": "Expected output",
			"watermarkText": "Describe what is your expected output and what you are seeing instead.",
			"required": true,
			"useAsAdditionalDetails": true,
			"hints": [{
					"text": "Issue description."
				},{
					"text": "Please provide additional details of what your expected and what was actually observed."
				}
			]
		},{
			"id": "sample_input",
			"order": 3,
			"controlType": "multilinetextbox",
			"displayLabel": "Sample Input",
			"watermarkText": "Provide sample input (in JSON) without PII",
			"required": false
		},{
			"id": "asa_query",
			"order": 4,
			"controlType": "multilinetextbox",
			"displayLabel": "ASA Query",
			"watermarkText": "Provide query that is producing unexpected results",
			"required": false
		}
	]
}
---
