<properties
    pageTitle="Adaptive Application Control (AAC)"
    description="Adaptive Application Control (AAC)"
    authors="genlin"
    ms.author="kawilson"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32693228"
    productPesIds="15947"
    cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="b1b6273d-908e-4f2d-0001-36a830ea0107"
    ownershipId="Azure_Security_Security_Center"
/>
# Adaptive Application Control (AAC)
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "32693228",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "acc_issuetype",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "select the option that best matches the issue you're experiencing",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Virtual machine configuration",
                    "text": "Virtual machine configuration"
                },
                {
                    "value": "Group configuration",
                    "text": "Group configuration"
                },
                {
                    "value": "Other issues with AAC",
                    "text": "Other issues with AAC"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other"
                }
            ],
            "required": true
        },
        {
            "id": "problem_description",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
