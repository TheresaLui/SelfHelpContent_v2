<properties
pageTitle="Other Issues"
description="Other Issues"
service="microsoft.servicebus"
resource="errorMessageTypes"
authors="mksuni"
ms.author="mksuni"
displayOrder=""
selfHelpType="problemScopingQuestions"
supportTopicIds="32633385,32637097"
resourceTags=""
productPesIds="13186"
cloudEnvironments="public, Fairfax, usnat, ussec"
articleId="sb-other-issues"
schemaVersion="1"
	ownershipId="AzureMessaging_Common"
/>
# Other Issues
---
{
    "subscriptionRequired": true,
    "title": "Other Issues",
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