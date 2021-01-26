
<properties
pageTitle="Query produces error"
description="Query produces error"
articleId="problemscopingques-Query_produces_error_times_out_or_too_slow"
authors="shemers"
ms.author="shemers"
selfHelpType="problemScopingQuestions"
supportTopicIds="32612514"
productPesIds="15725"
cloudEnvironments="Public, Fairfax, usnat, ussec"
schemaVersion="1"
ownershipId="AzureMonitoring_LogAnalytics"
/>

# Query produces error
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Query produces error",
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
            "displayLabel": "Was this query ever successful?",
            "watermarkText": "Choose an option",
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
            "id": "is_intermittent",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Is the error intermittent or constant?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Intermittent",
                    "text": "Intermittent"
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
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "What is the request id for the query?",
            "watermarkText": "Enter the 32 characters request id displayed on the error message",
            "required": false
        },
        {
            "id": "query_desc",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the query being executed?",
            "watermarkText": "Please enter the full query being executed",
            "required": true
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