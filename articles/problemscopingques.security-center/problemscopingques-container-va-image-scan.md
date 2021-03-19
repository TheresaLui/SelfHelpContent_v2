<properties
    pageTitle="Container Vulnerability Assessment image scanning"
    description="Container Vulnerability Assessment image scanning"
    authors="TobyTu"
    ms.author="kawilson"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32749414"
    productPesIds="15947"
    cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="b1b6273d-908e-4f2d-ab00-36a830ea0102"
    ownershipId="Azure_Security_Security_Center"
/>
# Container Vulnerability Assessment image scanning
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Container Vulnerability Assessment image scanning",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "registry_type",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "What is the container registry type?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Public",
                    "text": "Public"
                },
                {
                    "value": "Private (Firewalled)",
                    "text": "Private (Firewalled)"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other"
                }
            ],
            "required": true
        },
        {
            "id": "issue_type",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What is the issue you are experiencing?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Image scan is missing",
                    "text": "Image scan is missing"
                },
                {
                    "value": "Deleted image findings remain",
                    "text": "Deleted image findings remain"
                },
                {
                    "value": "Scan complete but no findings",
                    "text": "Scan complete but no findings"
                },
                {
                    "value": "Scan error",
                    "text": "Scan error"
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
