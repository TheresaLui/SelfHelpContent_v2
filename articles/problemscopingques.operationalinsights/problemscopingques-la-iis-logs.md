<properties
    articleId="problemscopingques-la-iis-logs"
    pageTitle="IIS Logs"
    description="IIS Logs"
    authors="neilghuman"
    ms.author="neghuman"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32745412"
    productPesIds="15725"
    cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
    schemaVersion="1"
    ownershipId="AzureMonitoring_LogAnalytics"
/>
# IIS Logs
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "IIS Logs",
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
                    "value": "Cannot enable or disable IIS log collection",
                    "text": "Cannot enable or disable IIS log collection"
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
            "displayLabel": "What is the data source?",
            "watermarkText": "Choose an option",
            "required": false,
            "dropdownOptions": [
                {
                    "value": "Log Analytics Agent installed on the machine(s)",
                    "text": "Log Analytics Agent installed on the machine(s)"
                },
                {
                    "value": "Azure Storage Account",
                    "text": "Azure Storage Account"
                },
                {
                    "value": "dont_know_answer",
                    "text": "I don't know"
                }
            ]
        },
                {
            "id": "la_agent",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "If the data source is the Log Analytics agent, please type the machine name(s).",
            "watermarkText": "If the data source is the Log Analytics agent, please type the machine name(s).",
            "required": false,
            "useAsAdditionalDetails": false
        },
                {
            "id": "azure_storage",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "If the data source is an Azure Storage Account, please type the storage account name:",
            "watermarkText": "If the data source is an Azure Storage Account, please type the storage account name:",
            "required": false,
            "useAsAdditionalDetails": false
        },
        {
            "id": "worked",
            "order": 6,
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
            "order": 7,
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
            "order": 8,
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
            "displayLabel": "Describe the issue, including as much detail as possible with the exact text of any error messages. Please also include any relevant queries used.",
            "watermarkText": "Describe the issue, including as much detail as possible with the exact text of any error messages. Please also include any relevant queries used.",
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
