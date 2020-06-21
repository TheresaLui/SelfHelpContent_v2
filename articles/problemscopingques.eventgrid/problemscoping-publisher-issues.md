<properties
pageTitle="Publisher Issues"
description="Publisher Issues"
service="microsoft.eventgrid"
resource="publisherissues"
authors="mksuni"
ms.author="mksuni"
displayOrder=""
selfHelpType="problemScopingQuestions"
supportTopicIds="32583169"
resourceTags=""
productPesIds="16263"
cloudEnvironments="public, Fairfax, usnat, ussec"
articleId="eg-publisherissues"
schemaVersion="1"
	ownershipId="AzureEventGrid_Topics"
/>
# Publisher issues
---
{
    "subscriptionRequired": true,
    "title": "Publisher Issues",
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
            "id": "problem_description",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide the exact error message including call stack, Tracking Id and timestamp, if any",
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