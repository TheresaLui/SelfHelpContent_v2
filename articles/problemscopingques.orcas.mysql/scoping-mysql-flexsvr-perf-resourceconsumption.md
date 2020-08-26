<properties
    pageTitle="Database Performance"
    description="Database Performance"
    authors="Hang-Zhang"
    ms.author="haz"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32747643"
    productPesIds="17344"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="scoping-mysql-flexsvr-perf-resource_consumption"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>
# Performance and Query Execution - Unexpected increase in resource consumption (CPU, Memory, I/O)
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Database Performance Resource Consumption",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "issue_ongoing",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Is the issue ongoing?",
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
                    "text": "Don't know or unsure"
                }
            ],
            "required": false
        },
        {
            "id": "issue_time",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Can you provide the start time and end time of the issue?",
            "required": false
        },
        {
            "id": "workload_increase",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Did your workload increase during the issue time range?",
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
                    "text": "Don't know or unsure"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Problem description",
            "watermarkText": "Provide your repro steps and other information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
