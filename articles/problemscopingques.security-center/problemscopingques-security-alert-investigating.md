<properties
    pageTitle="Investigating Security Alerts for root cause"
    description="Investigating Security Alerts for root cause"
    authors="TobyTu"
    ms.author="kawilson"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32693236"
    productPesIds="15947"
    cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="b1b6273d-908e-4f2d-ab00-36a830ea0111"
    ownershipId="Azure_Security_Security_Center"
/>
# Investigating Security Alerts for root cause
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Investigating Security Alerts for root cause",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "name",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Enter the alert name or type",
            "required": false
        },
        {
            "id": "alert_type",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Select the alert resource or entity",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Suspecting false-positive",
                    "text": "Suspecting false-positive"
                },
                {
                    "value": "Requesting more evidence",
                    "text": "Requesting more evidence"
                },
                {
                    "value": "Requesting alert investigation",
                    "text": "Requesting alert investigation"
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
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
