<properties
pageTitle="Unexpected Service Behavior"
description="Message Lost or duplicate message issues"
service="microsoft.servicebus"
resource="errorMessageTypes"
authors="mksuni"
ms.author="mksuni"
displayOrder=""
selfHelpType="problemScopingQuestions"
supportTopicIds="32633401,32633397"
resourceTags=""
productPesIds="13186"
cloudEnvironments="public, Fairfax, usnat, ussec"
articleId="sb-message-lost-issue"
schemaVersion="1"
	ownershipId="AzureMessaging_Common"
/>
# Message Lost or duplicate message issues
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Message Lost or duplicate message issues",
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
            "id": "problem_messageId",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide the Message ID and Enqueue time for the message",
            "watermarkText": "Enter the Message ID",
            "required": true
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