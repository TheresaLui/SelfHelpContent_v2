<properties
    articleId="problemscopingques-custom-fields"
    pageTitle="Custom Fields"
    description="Custom Fields"
    articleId="problemscopingques-Windows_Custom Fields"
    authors="neilghuman"
    ms.author="neghuman"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32745410"
    productPesIds="15725"
    cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
    schemaVersion="1"
    ownershipId="AzureMonitoring_LogAnalytics"
/>

# Custom Fields
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Custom Fields",
    "fileAttachmentHint": "If applicable, please upload logs or screenshots of any relevant which may help the support engineer troubleshoot your issue.",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start happening?",
            "required": true
        },
        {
            "id": "Issue_type",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What type of issue is occurring",
            "watermarkText": "Choose one issu type",
            "dropdownOptions": [
                {
                    "value": "Cannot create a custom field",
                    "text": "Cannot create a custom field"
                },
                {
                    "value": "Cannot remove a custom field",
                    "text": "Cannot remove a custom field"
                },
                {
                    "value": "Custom field is extracting incorrect\incomplete data",
                    "text": "Custom field is extracting incorrect\incomplete data"
                },
                {
                    "value": "Custom field is not extracting any data",
                    "text": "Custom field is not extracting any data"
                },
                {
                    "value": "dont_know_answer",
                    "text": "I don't know"
                }
            ],
            "required": true
        },
        {
            "id": "problem_frequency",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Has this ever worked before?",
            "watermarkText": "Has this ever worked before?",
            "required": false,
            "dropdownOptions": [
                {
                    "value": "True",
                    "text": "True"
                },
                {
                    "value": "False",
                    "text": "False"
                },
                {
                    "value": "dont_know_answer",
                    "text": "I don't know"
                }
            ]
        },
        {
            "id": "users",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Is the issue happening to a single user or multiple users?",
            "watermarkText": "Is the issue happening to a single user or multiple users?",
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
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Is the issue intermittent or constant?",
            "watermarkText": "Is the issue intermittent or constant?",
            "required": false,
            "dropdownOptions": [
                {
                    "value": "Ittermittent",
                    "text": "Ittermittent"
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
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Describe the issue, including as much detail as possible with the exact text of any error messages. Please also include any relevant queries used to query the data on the custom fields, describing what's the expected behavior vs the current behavior",
            "required": true,
            "useAsAdditionalDetails": false,
            "hints": []
        },
        {
            "id": "additional_information",
            "order": 7,
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
