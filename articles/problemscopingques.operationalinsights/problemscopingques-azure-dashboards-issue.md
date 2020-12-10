<properties
    articleId="problemscopingques-azure-dashboards-issue"
    pageTitle="Azure dashboards issue"
    description="Azure dashboards issue"
    authors="neilghuman"
    ms.author="neghuman"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32745416"
    productPesIds="15725"
    cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
    schemaVersion="1"
    ownershipId="AzureMonitoring_LogAnalytics"
/>
# Azure dashboards issue
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Azure dashboards issue",
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
                    "value": "Cannot pin query to dashboard",
                    "text": "Cannot pin query to dashboard"
                },
                {
                    "value": "Data is not refreshing",
                    "text": "Data is not refreshing"
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
            "displayLabel": "What type of dashboard is being used?",
            "watermarkText": "Choose an option",
            "required": false,
            "dropdownOptions": [
                {
                    "value": "Private",
                    "text": "Private"
                },
                {
                    "value": "Shared",
                    "text": "Shared"
                },
                {
                    "value": "dont_know_answer",
                    "text": "I don't know"
                }
            ]
        },
                {
            "id": "dashboard",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Are you using an existing dashboard?",
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
            "id": "worked",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Has this ever worked?",
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
            "order": 8,
            "controlType": "multilinetextbox",
            "displayLabel": "Describe the issue, including as much detail as possible with the exact text of any error messages. Please also include any relevant queries used to query the data on the Azure dashboards issue, describing what's the expected behavior vs the current behavior.",
            "watermarkText": "Describe the issue, including as much detail as possible with the exact text of any error messages. Please also include any relevant queries used to query the data on the Azure dashboards issue, describing what's the expected behavior vs the current behavior.",
            "required": true,
            "useAsAdditionalDetails": false,
            "hints": []
        },
        {
            "id": "additional_information",
            "order": 9,
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
