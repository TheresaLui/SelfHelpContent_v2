<properties
    articleId="problemscopingques-la-collect-azure-activity-logs"
    pageTitle="Collect Azure Activity logs"
    description="Collect Azure Activity logs"
    authors="neilghuman"
    ms.author="neghuman"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32745408"
    productPesIds="15725"
    cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
    schemaVersion="1"
    ownershipId="AzureMonitoring_LogAnalytics"
/>
# Collect Azure Activity logs
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Collect Azure Activity logs",
    "fileAttachmentHint": "If applicable, please upload logs or screenshots of any relevant information which may help the support engineer troubleshoot your issue.",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start happening?",
            "required": true
        },
        {
            "id": "issue_type",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What type of issue is occurring?",
            "required": true,
            "watermarkText": "Choose one issue type",
            "dropdownOptions": [
                {
                    "value": "Cannot enable or disable Azure Activity logs collection",
                    "text": "Cannot enable or disable Azure Activity logs collection"
                },
                {
                    "value": "No data is being collected",
                    "text": "No data is being collected"
                },
                {
                    "value": "Data is incorrect / incomplete",
                    "text": "Data is incorrect / incomplete"
                },
                {
                    "value": "dont_know_answer",
                    "text": "I don't know"
                }
            ]
        },
        {
            "id": "problem_frequency",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "What collection method is being used?",
            "watermarkText": "Choose an option",
            "required": false,
            "dropdownOptions": [
                {
                    "value": "Collecting Activity Logs through Diagnostic settings",
                    "text": "Collecting Activity Logs through Diagnostic settings"
                },
                {
                    "value": "Collecting Activity Logs through legacy settings",
                    "text": "Collecting Activity Logs through legacy settings"
                },
                {
                    "value": "dont_know_answer",
                    "text": "I don't know"
                }
            ]
        },
        {
            "id": "worked",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Is the target subscription the same where the Log Analytics workspace is?",
            "watermarkText": "Choose an option",
            "required": false,
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
                    "text": "I don't know"
                }
            ]
        },
                {
            "id": "worked-in-the-past",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Has this ever worked?",
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
                    "text": "Not sure"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "users",
            "order": 6,
            "controlType": "dropdown",
            "displayLabel": "Is the issue happening to a single user or multiple users?",
            "watermarkText": "Choose an option",
            "required": false,
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
                    "text": "I don't know"
                }
            ]
        },
                        {
            "id": "intermittent_consistant",
            "order": 7,
            "controlType": "dropdown",
            "displayLabel": "Is the issue intermittent or constant?",
            "watermarkText": "Is the issue intermittent or constant?",
            "required": false,
            "dropdownOptions": [
                {
                    "value": "Itermittent",
                    "text": "Itermittent"
                },
                {
                    "value": "Constant",
                    "text": "Constant"
                },
                {
                    "value": "dont_know_answer",
                    "text": "I don't know"
                }
            ]
        },
        {
            "id": "problem_description",
            "order": 9,
            "controlType": "multilinetextbox",
            "displayLabel": "Describe the issue, including as much detail as possible with the exact text of any error messages where available. Please also include any relevant queries used.",
            "watermarkText": "Describe the issue, including as much detail as possible with the exact text of any error messages where available. Please also include any relevant queries used.",
            "required": true,
            "useAsAdditionalDetails": false,
            "hints": []
        },
        {
            "id": "additional_information",
            "order": 10,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional information about the issue.",
            "watermarkText": "Provide any additional information about the issue.",
            "required": false,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
