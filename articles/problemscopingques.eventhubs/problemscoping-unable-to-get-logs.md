<properties
pageTitle="Unable to retrieve diagnostics or log information"
description="Unable to retrieve diagnostics or log information"
service="microsoft.eventhubs"
resource="unableToGetLogs"
authors="mksuni"
ms.author="mksuni"
displayOrder=""
selfHelpType="problemScopingQuestions"
supportTopicIds="32636953"
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
    "resourceRequired": true,
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
            "id": "problem_saskeys",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Did you reset your SAS keys recently and When?",
            "required": false
        },
       {
            "id": "problem_monitoringdata",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "What Azure monitoring data are your trying to collect ?",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 5,
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