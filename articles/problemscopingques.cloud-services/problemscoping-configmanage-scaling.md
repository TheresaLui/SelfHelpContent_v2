<properties
                pageTitle="Configuration and Management"
                description="Configuration and Management"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32569897"
                productPesIds="13185"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0100"
	ownershipId="Compute_CloudServices_Content"
/>
# Config and Management
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Scaling",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "scaling_symptom",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the symptom related to your scaling issue?",
            "required": false,
            "useAsAdditionalDetails": false
        },
        {
            "id": "autoscale",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "How did you enable AutoScale?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "I am using a tool that manages my autoscaling using the Azure rest APIs",
                    "text": "I am using a tool that manages my autoscaling using the Azure rest APIs"
                },
                {
                    "value": "I am using Azure autoscaling through Azure portal",
                    "text": "I am using Azure autoscaling through Azure portal"
                }
            ],
            "required": false
        },
        {
            "id": "autoscale_notification",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "If you have received a notification for AutoScale from Azure, please share.",
            "required": false,
            "useAsAdditionalDetails": false
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
