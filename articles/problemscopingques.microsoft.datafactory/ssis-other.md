<properties
	pageTitle="Azure-SSIS Other Info"
	description="Scoping questions to gather Azure Data Factory SSIS IR information"
	authors="lle"
    ms.author="lle"
	selfHelpType="problemScopingQuestions"
    supportTopicIds="32680897, 32680900"
	productPesIds="15613"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
    articleId="15245096-3EB3-472A-8EBB-B1C5E30EF8C2"
	ownershipId="AzureData_DataFactory"
/>

# Azure-SSIS Related Issue

---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Azure-SSIS Other Info",
    "formElements": [
        {
            "id": "problem_description",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional details about the issue",
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
            "id": "data_factory_name",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What's the name of Data Factory?",
            "required": false
        },
        {
            "id": "ssisir_name",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "What's the name of Azure-SSIS Integration Runtime?",
            "required": false
        },
        {
            "id": "operation_trigger",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Did you use ADF Portal or SDK?",
            "dropdownOptions": [
                {
                    "value": "ADF Portal",
                    "text": "ADF Portal"
                },
                {
                    "value": "PowerShell",
                    "text": "PowerShell"
                },
                {
                    "value": ".NET Client",
                    "text": ".NET Client"
                },
                {
                    "value": "Other",
                    "text": "Other"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 6,
            "controlType": "datetimepicker",
            "displayLabel": "What time did the problem begin?",
            "required": true
        },
        {
            "id": "problem_end_time",
            "order": 7,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate time when the problem stopped occurring. If the issue is ongoing, leave this field blank",
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
