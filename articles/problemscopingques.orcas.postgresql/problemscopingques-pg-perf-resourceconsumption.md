<properties
    pageTitle="Database Performance"
    description="Database Performance"
    authors="Xin-Cheng"
    ms.author="chengxin"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32731228"
    productPesIds="17067,17069,17068"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="problemscopingques-pg-perf-resourceconsumption"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
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
