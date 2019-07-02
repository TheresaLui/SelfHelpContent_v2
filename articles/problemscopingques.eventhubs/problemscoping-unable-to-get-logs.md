<properties
pageTitle="Unable to retrieve diagnostics or log information"
description="Unable to retrieve diagnostics or log information"
service="microsoft.eventhubs"
resource="unableToGetLogs"
authors="mksuni"
ms.author="mksuni"
displayOrder=""
selfHelpType="problemScopingQuestions"
supportTopicIds="32636941"
resourceTags=""
productPesIds="16125"
cloudEnvironments="public"
articleId="eh-unable-to-get-logs"
schemaVersion="1"
/>
# Unable to retrieve diagnostics or log information
---
{
    "subscriptionRequired": true,
    "title": "Unable to retrieve diagnostics or log information",
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
            "id": "problem_issueFrequency",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "How frequently does the issue occur?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Always",
                    "text": "Always"
                },
                {
                    "value": "Intermittent",
                    "text": "Intermittent"
                },
                {
                    "value": "DontKnow",
                    "text": "Didn't notice any trend"
                }
            ]
        },
        {
            "id": "problem_expectedLatency",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Did you reset your SAS keys recently and When?",
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