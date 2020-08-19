<properties
	pageTitle="Azure-SSIS Data Source Authentication and Connectivity Info"
	description="Scoping questions to gather Azure Data Factory SSIS IR information"
	authors="chez-charlie"
	ms.author="chez"
	selfHelpType="problemScopingQuestions"
    supportTopicIds="32680898,32680899"
	productPesIds="15613"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
    articleId="470E2DC7-1914-49B2-93CA-367CD686A8BC"
	ownershipId="AzureData_DataFactory"
/>

# Azure-SSIS Data Source Authentication and Connectivity Info

---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Azure-SSIS Data Source Authentication and Connectivity Info",
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
            "displayLabel": "What's the name of your Data Factory?",
            "required": false
        },
        {
            "id": "ssisir_name",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "What's the name of your Azure-SSIS Integration Runtime?",
            "required": false
        },
        {
            "id": "data_source_location",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Where is your data source?",
            "dropdownOptions": [
                {
                    "value": "On-prem",
                    "text": "On-prem"
                },
                {
                    "value": "Azure",
                    "text": "Azure"
                },
                {
                    "value": "3rd party",
                    "text": "3rd party"
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
