
<properties
pageTitle="Permissions and access control (IAM)"
description="Permissions and access control (IAM)"
articleId="problemscopingques-Permissions_and_access_control_(IAM)"
authors="yossiy"
ms.author="yossiy"
selfHelpType="problemScopingQuestions"
supportTopicIds="32612439"
productPesIds="15725"
cloudEnvironments="Public, Fairfax, usnat, ussec"
schemaVersion="1"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# Permissions and access control (IAM)
 
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Permissions and access control (IAM)",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "desired_goal",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What is your desired goal by contacting Microsoft Support today?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "I can’t find the information in product documentation",
                    "text": "I can’t find the information in product documentation"
                },
                {
                    "value": "Have an issue but can’t find a suitable support topic for it",
                    "text": "I have an issue but can’t find a suitable support topic for it"
                },
                {
                    "value": "General question",
                    "text": "General question"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Not sure"
                }
            ],
            "required": true
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "hints": []
        }
    ],
    "$schema": "SelfHelpContent"
}
---