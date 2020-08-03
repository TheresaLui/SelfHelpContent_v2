<properties
	pageTitle="Azure Data Movement performance issue info"
	description="Scoping questions to gather Azure Data Movement performance issue information"
	authors="chez-charlie, hecepeda"
	ms.author="chez"
	selfHelpType="problemScopingQuestions"
    supportTopicIds="32629468"
	productPesIds="15613"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
    articleId="5e8933fe-c7dd-48d9-9dec-e214035697c9"
	ownershipId="AzureData_DataFactory"
/>
# Azure Data Movement Performance Issue
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Azure Data Movement performance issue info",
    "fileAttachmentHint": "Please attach JSON code for dataset, linked service and screen shots to help us triage your problem faster",
    "formElements": [
        {
            "id": "problem_description",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "Please briefly describe the issue",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Is it a new issue or regression?"
                },
                {
                    "text": "Is the issue intermittent or persistent?"
                }
            ]
        },
        {
            "id": "error_message",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "What error message do you see?",
            "required": false
        },
        {
            "id": "source_name",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What's the source of the slow copy activity?",
            "required": false
        },
        {
            "id": "sink_name",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "What's the sink of the slow copy activity?",
            "required": false
        },
        {
            "id": "ir_type",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Which type of integration runtime are you using?",
            "watermarkText": "Choose an IR type",
            "dropdownOptions": [
                {
                    "value": "Azure IR",
                    "text": "Azure IR"
                },
                {
                    "value": "Self-hosted IR",
                    "text": "Self-hosted IR"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "problem_run_id",
            "order": 6,
			"visibility": "ir_type == Azure IR || dont_know_answer",
            "controlType": "textbox",
            "displayLabel": "Sample slow pipeline RunIDs (separate with commas)",
            "required": true
        },
		{
            "id": "problem_report_id",
            "order": 7,
			"visibility": "ir_type == Self-hosted IR",
            "controlType": "textbox",
            "displayLabel": "Sample slow pipeline Report ID from all nodes separated with commas. (see Solutions tab for guidance on how to obtain Report ID)",
            "required": true
        },
        {
            "id": "sample_normal_run_id",
            "order": 8,
			"visibility": "ir_type == Azure IR || dont_know_answer",
            "controlType": "textbox",
            "displayLabel": "Sample normal pipeline RunIDs (separate with commas)",
            "required": false
        },
                {
            "id": "problem_start_time",
            "order": 9,
            "controlType": "datetimepicker",
            "displayLabel": "What time did the problem begin?",
            "required": true
        },
        {
            "id": "problem_end_time",
            "order": 10,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate time when the problem stopped occurring. If the issue is ongoing, leave this field blank",
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
