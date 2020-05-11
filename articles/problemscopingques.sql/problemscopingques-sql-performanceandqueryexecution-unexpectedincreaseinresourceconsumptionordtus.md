<properties
	pageTitle="Performance and query execution/unexpected increase in resource consumption or DTUs"
	description="Scoping questions for performance and query execution/unexpected increase in resource consumption or DTUs."
	ms.author="andikshi,xinyl"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630459"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake,usnat,ussec"
	schemaVersion="1"
	articleId="problemscopingques-sql-performanceandqueryexecution-unexpectedincreaseinresourceconsumptionordtus"
	ownershipId="AzureData_AzureSQLDB_Performance"
/>
# Performance and query execution/unexpected increase in resource consumption or DTUs
---
{
	"$schema": "SelfHelpContent",
	"resourceRequired": true,
	"subscriptionRequired": true,
	"title": "Unexpected increase in resource consumption or DTUs",
	"fileAttachmentHint": "",
	"diagnosticCard": {
	"title": "SQL DB Performance Troubleshooter",
	"description": "Our SQL DB Performance Troubleshooter can help you troubleshoot and solve your problem.",
	"insightNotAvailableText": "Our troubleshooter did not detect any issues with your resource. See our manual troubleshooting steps below to troubleshoot your problem."
	},
	"formElements": [{
			"id": "problem_start_time",
			"order": 1,
			"controltype": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"watermarkText": "Specify when the problem started",
			"infoBalloonText": "Specify when the problem started",
			"required": true,
			"diagnosticInputRequiredClients": "Portal"
		}, {
			"id": "attempt_method",
			"order": 2,
			"controlType": "dropdown",
			"displayLabel": "Was there any significant change in your environment or usage recently?",
			"required": true,
			"dropdownOptions": [
				{
					"value": "workload",
					"text": "My workload increased."
				},
				{
					"value": "Service tier",
					"text": "I changed my database service tier recently."
				},
				{
					"text": "Other, don't know or not applicable",
					"value": "dont_know_answer"
				}
			]
		}, {
			"id": "encountering_an_error",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "Are you encountering an error message?",
			"dropdownOptions": [
				{
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
		}, {
			"id": "error_message",
			"order": 4,
			"controlType": "multilinetextbox",
			"displayLabel": "Please provide the error message",
			"required": false,
			"visibility": "encountering_an_error == Yes"
		}, {
			"id": "problem_description",
			"order": 1000,
			"controlType": "multilinetextbox",
			"displayLabel": "Description",
			"watermarkText": "Provide additional information about your issue",
			"required": true,
			"useAsAdditionalDetails": true
		}
	]
}
---