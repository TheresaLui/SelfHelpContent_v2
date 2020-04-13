<properties
pageTitle="Unexpected Service Behavior"
description="Incorrect Message Count issues"
service="microsoft.servicebus"
resource="errorMessageTypes"
authors="mksuni"
ms.author="mksuni"
displayOrder=""
selfHelpType="problemScopingQuestions"
supportTopicIds="32633398"
resourceTags=""
productPesIds="13186"
cloudEnvironments="public, Fairfax, usnat, ussec"
articleId="sb-message-count-issue"
schemaVersion="1"
	ownershipId="AzureMessaging_Common"
/>
# Message Count Issues
---
{
    "subscriptionRequired": true,
    "title": "Incorrect Message Count issues",
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
            "id": "problem_currentMesssageCount",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Enter the current message count",
            "watermarkText": "Enter the current message count",
            "required": false
        },
        {
            "id": "problem_ExpectedMesssageCount",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Enter the expected message count",
            "watermarkText": "Enter the expected message count",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 4,
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
