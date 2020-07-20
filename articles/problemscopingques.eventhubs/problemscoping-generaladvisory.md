<properties
pageTitle="General Advisory questions"
description="General Advisory questions"
service="microsoft.eventhubs"
resource="generaladvisory"
authors="mksuni"
ms.author="mksuni"
displayOrder=""
selfHelpType="problemScopingQuestions"
supportTopicIds="32636933"
resourceTags=""
productPesIds="16125"
cloudEnvironments="public, Fairfax, usnat, ussec"
articleId="eh-issue-not-listed"
schemaVersion="1"
	ownershipId="AzureMessaging_Common"
/>
# General Advisory questions
---
{
    "subscriptionRequired": true,
    "title": "General Advisory questions",
    "resourceRequired": true,
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
            "id": "problem_errorMessageText",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide the exact error message including call stack, Tracking Id and timestamp, if any",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Issue description."
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---