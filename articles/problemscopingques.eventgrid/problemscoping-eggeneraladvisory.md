<properties
pageTitle="General Advisory questions"
description="General Advisory questions"
service="microsoft.eventgrid"
resource="generaladvisory"
authors="mksuni"
ms.author="mksuni"
displayOrder=""
selfHelpType="problemScopingQuestions"
supportTopicIds="32583160,32583163"
resourceTags=""
productPesIds="16263"
cloudEnvironments="public, Fairfax, usnat, ussec"
articleId="eg-issue-not-listed"
schemaVersion="1"
	ownershipId="AzureEventGrid_Topics"
/>
# General Advisory questions
---
{
    "subscriptionRequired": true,
    "title": "General Advisory questions",
    "resourceRequired": false,
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
