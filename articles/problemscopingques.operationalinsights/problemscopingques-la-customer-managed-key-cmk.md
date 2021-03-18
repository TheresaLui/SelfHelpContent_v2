<properties
    articleId="problemscopingques-la-customer-managed-key-cmk"
    pageTitle="Customer managed key"
    description="Customer managed key"
    authors="neilghuman"
    ms.author="neghuman"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32745440"
    productPesIds="15725"
    cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
    schemaVersion="1"
    ownershipId="AzureMonitoring_LogAnalytics"
/>
# Customer managed key
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Customer managed key",
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
                    "value": "Cannot create / remove the dedicated cluster resource",
                    "text": "Cannot create / remove the dedicated cluster resource"
                },
                {
                    "value": "Cannot update the cluster resource with the key identifier",
                    "text": "Cannot update the cluster resource with the key identifier"
                },
                {
                    "value": "Cannot associate / disassociate a workspace with the cluster resource",
                    "text": "Cannot associate / disassociate a workspace with the cluster resource"
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
            "displayLabel": "Describe the issue, including as much detail as possible with the exact text of any error messages where available. Please also include the dedicate cluster resource(s) and / or workspace name(s) being used.",
            "watermarkText": "Describe the issue, including as much detail as possible with the exact text of any error messages where available. Please also include the dedicate cluster resource(s) and / or workspace name(s) being used.",
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
