<properties
	pageTitle="Performance and query execution/monitoring metrics and alerts"
	description="Scoping questions for performance and query execution/monitoring metrics and alerts"
	ms.author="pedin,xinyl"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630434"
	productPesIds="13491"
	articleId="7CB09AA1-5844-4C6E-A7A2-B830CA09B2E3"
	cloudEnvironments="public,blackForest,fairfax,mooncake,usnat,ussec"
	schemaVersion="1"
	ownershipId="AzureData_AzureSQLDB_Performance"
/>
# Performance and query execution/monitoring metrics and alerts
---
{
	"$schema": "SelfHelpContent",
	"resourceRequired": true,
	"subscriptionRequired": true,
	"title": "Monitoring Metrics and Alerts",
	"fileAttachmentHint": "",
	"diagnosticCard": {
	"title": "SQL DB Performance Troubleshooter",
	"description": "Our SQL DB Performance Troubleshooter can help you troubleshoot and solve your problem.",
	"insightNotAvailableText": "Our troubleshooter did not detect any issues with your resource. See our manual troubleshooting steps below to troubleshoot your problem."
	},
	"formElements": [{
			"id": "problem_start_time",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem start?",
			"required": true,
			"diagnosticInputRequiredClients": "Portal"
		}, {
			"id": "problem_end_time",
			"order": 2,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem stop? (If ongoing, leave this field blank)",
			"required": false,
			"diagnosticInputRequiredClients": "Portal"
		}, {
			"id": "feature_dropdown",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "Which feature are you requesting help for?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Query_Performance_Insights",
					"text": "Query Performance Insights can be used to easily monitor resource usage in your Azure SQL database (single or pooled database) by using build-in monitoring capabilities in the Azure portal"
				}, {
					"value": "Automatic_Tuning",
					"text": "Automatic tuning automatically recommends and fixes query plan issues, and creates and drops indexes, to improve performance"
				}, {
					"value": "Alerts_Usage",
					"text": "Alerts can easily be created and managed in the Azure portal"
				}, {
					"value": "Feature_Other",
					"text": "Other feature not listed"
				}, {
					"value": "dont_know_answer",
					"text": "Don't know answer"
				}
			],
			"required": true
		}, {
			"id": "problem_description",
			"order": 4,
			"controlType": "multilinetextbox",
			"useAsAdditionalDetails": true,
			"displayLabel": "Details of the issue.",
			"watermarkText": "Please provide additional context for your Monitoring, Metrics and Alerts issues.",
			"required": true
		}
	]
}
---