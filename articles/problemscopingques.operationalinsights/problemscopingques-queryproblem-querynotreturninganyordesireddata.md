<properties
pageTitle="My query does not return any results"
description="My query does not return any results"
articleId="problemscopingques-queryproblem-querynotreturninganyordesireddata"
authors="shemers"
ms.author="shemers"
selfHelpType="problemScopingQuestions"
supportTopicIds="32612517"
productPesIds="15725"
cloudEnvironments="Public, Fairfax, usnat, ussec"
schemaVersion="1"
ownershipId="AzureMonitoring_LogAnalytics"
/>

# My query does not return any results
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "My query does not return any results",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem started?",
            "required": false
        },
        {
            "id": "worked_before",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Did this query ever worked before as expected?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "Multiple machines"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Not Sure"
                }
            ],
            "required": false
        },
        {
            "id": "is_multiple_users",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Is the error happening to a single user or multiple users?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Single user",
                    "text": "Single user"
                },
                {
                    "value": "Multiple users",
                    "text": "Multiple users"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Not Sure"
                }
            ],
            "required": false
        },
        {
            "id": "request_id",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "What is the request id for the query?",
            "watermarkText": "Enter the 32 characters request id displayed on the error message",
            "required": false
        },
        {
            "id": "query_desc",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the query being executed?",
            "watermarkText": "Please enter the full query being executed",
            "required": true
        },
        {
            "id": "expected_resualts",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "What were the expected query results?",
            "watermarkText": "Please include as much details as possible",
            "required": false
        },
        {
            "id": "attachment",
            "order": 7,
            "controlType": "infoblock",
            "content": "Please attach or paste in the query and expected results",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 8,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Describe the issue, including as much detail as possible with the exact text of error messages where available. Please also add query time range (if not defined directly on the query itself)",
            "required": true,
            "hints": []
        }
    ],
    "$schema": "SelfHelpContent"
}
---