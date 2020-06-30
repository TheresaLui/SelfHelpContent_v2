<properties
pageTitle="Development Issues"
description="Development Issues"
service="microsoft.eventgrid"
resource="developmentissues"
authors="mksuni"
ms.author="mksuni"
displayOrder=""
selfHelpType="problemScopingQuestions"
supportTopicIds="32583161"
resourceTags=""
productPesIds="16263"
cloudEnvironments="public, Fairfax, usnat, ussec"
articleId="eg-developmentissues"
schemaVersion="1"
	ownershipId="AzureEventGrid_Topics"
/>
# Development Issues
---
{
    "subscriptionRequired": true,
    "title": "Development Issues",
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
            "id": "problem_sdk",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide the SDK and the version  being used for development ",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
           "displayLabel": "Please provide the exact error message including call stack, Tracking Id and timestamp, if any",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Issue description details"
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---