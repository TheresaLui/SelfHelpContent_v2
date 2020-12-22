<properties
    pageTitle="Built-in Vulnerability Assessment (Powered by Qualys)"
    description="Built-in Vulnerability Assessment (Powered by Qualys)"
    authors="TobyTu"
    ms.author="kawilson"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32749413"
    productPesIds="15947"
    cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="b1b6273d-908e-4f2d-ab00-36a830ea0101"
    ownershipId="Azure_Security_Security_Center"
/>
# Built-in Vulnerability Assessment (Powered by Qualys)
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Built-in Vulnerability Assessment",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "issue_type",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "What is the issue you are experiencing?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Fail to provision VM extension",
                    "text": "Fail to provision VM extension"
                },
                {
                    "value": "Fail to get Vulnerability Assessment recommendation to install",
                    "text": "Fail to get Vulnerability Assessment recommendation to install"
                },
                {
                    "value": "Fail to get Vulnerability Assessment findings after install",
                    "text": "Fail to get Vulnerability Assessment findings after install"
                },
                {
                    "value": "dont_know_answer",
                    "text": "General questions"
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
