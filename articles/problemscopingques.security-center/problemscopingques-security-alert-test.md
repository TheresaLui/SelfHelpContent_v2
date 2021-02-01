<properties
    pageTitle="Testing Security Alerts"
    description="Testing Security Alerts"
    authors="TobyTu"
    ms.author="kawilson"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32693250"
    productPesIds="15947"
    cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="b1b6273d-908e-4f2d-ab00-36a830ea0110"
    ownershipId="Azure_Security_Security_Center"
/>
# Testing Security Alerts
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Testing Security Alerts",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "alert_resource",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Select the alert resource or entity",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Virtual machin",
                    "text": "Virtual machin"
                },
                {
                    "value": "Kubernetes",
                    "text": "Kubernetes"
                },
                {
                    "value": "Container/Docker/Other image",
                    "text": "Container/Docker/Other image"
                },
                {
                    "value": "Key Vault",
                    "text": "Key Vault"
                },
                {
                    "value": "SQL",
                    "text": "SQL"
                },
                {
                    "value": "Storage Account",
                    "text": "Storage Account"
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
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
