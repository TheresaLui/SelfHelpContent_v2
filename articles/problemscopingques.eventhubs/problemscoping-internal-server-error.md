<properties
pageTitle="Internal Server Errors"
description="Internal Server Errors"
service="microsoft.eventhubs"
resource="internalServerissues"
authors="mksuni"
ms.author="mksuni"
displayOrder=""
selfHelpType="problemScopingQuestions"
supportTopicIds="32636942"
resourceTags=""
productPesIds="16125"
cloudEnvironments="public, Fairfax, usnat, ussec"
articleId="eh-internal-server-error"
schemaVersion="1"
	ownershipId="AzureMessaging_Common"
/>
# Internal Server Errors
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Internal Server Errors",
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
            "id": "problem_sdkversion",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Have you enabled exponential back off and retry behaviors" ,
            "required": false
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide the call stack with exception messages?",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---