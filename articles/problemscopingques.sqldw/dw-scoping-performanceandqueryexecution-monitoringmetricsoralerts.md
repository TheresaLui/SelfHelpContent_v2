<properties
	articleId="dw-scoping-performanceandqueryexecution-monitoringmetricsoralerts"
	pageTitle="Monitoring, metrics, or alerts"
	description="Monitoring, metrics, or alerts"
	authors="mlee3gsd"
	ms.author="martinle"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32635204, 32635205"
	productPesIds="15818"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_SQLDataWarehouse"
/>
# Performance and Query Execution - Monitoring, metrics, or alerts
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Performance and Query Execution - Monitoring, metrics, or alerts",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start",
            "required": true
        },
        {
            "id": "dw_scoping_perf_portal",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Are you experiencing this through the Azure portal or programmatically (TSQL)?",
            "required": false
        },
        {
            "id": "dw_scoping_perf_metric",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Which monitoring, metric, or alert is of concern?",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---