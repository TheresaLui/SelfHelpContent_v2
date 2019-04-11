<properties
	pageTitle="Scoping questions for Monitoring Metrics and Alerts"
	description="Monitoring Metrics and Alerts"
	service="microsoft.sql"
	authors="pxding"
        ms.author="pedin"
        articleId="56AEDE05-378E-4B89-9FF6-2B3776D9BD09"
        selfHelpType="ProblemScopingQuestions"
        supportTopicIds="32630434"
        productPesIds="13491"
	cloudEnvironments="public"
        schemaVersion="1"
/>

# Monitoring Metrics and Alerts
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Monitoring Metrics and Alerts",
    "fileAttachmentHint": "",
    "formElements": [{
                        "id": "problem_start_time",
                        "order": 1,
                        "controlType": "datetimepicker",
                        "displayLabel": "When did the problem start?",
                        "required": true
                }, {
			"id": "problem_end_time",
			"order": 2,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem stop? (If ongoing, leave this field blank)",
			"required": false
		}, {
			"id": "feature_dropdown",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "Which feature are you requesting help for?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
				value": "Query_Performance_Insights",
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



