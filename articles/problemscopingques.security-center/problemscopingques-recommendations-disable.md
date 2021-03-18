<properties
    pageTitle="How to disable recommendation"
    description="How to disable recommendation"
    authors="TobyTu"
    ms.author="kawilson"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32693235"
    productPesIds="15947"
    cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="b1b6273d-908e-4f2d-ab00-36a830ea0106"
    ownershipId="Azure_Security_Security_Center"
/>
# How to disable recommendation
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "How to disable recommendation",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "recommendation_name",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Please enter the recommendation name",
            "required": false
        },
        {
            "id": "graph_output",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Please enter the Resource Graph Output",
            "required": false
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
