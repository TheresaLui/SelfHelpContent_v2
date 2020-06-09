<properties
pageTitle="Subscriber Issues"
description="Subscriber Issues"
service="microsoft.eventgrid"
resource="subscriberissues"
authors="mksuni"
ms.author="mksuni"
displayOrder=""
selfHelpType="problemScopingQuestions"
supportTopicIds="32583170"
resourceTags=""
productPesIds="16263"
cloudEnvironments="public, Fairfax, usnat, ussec"
articleId="eg-subscriberissues"
schemaVersion="1"
	ownershipId="AzureEventGrid_Topics"
/>
# Subscriber issues
---
{
    "subscriptionRequired": true,
    "title": "Subscriber Issues",
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
            "id": "problem_eventsize",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Please provide size of the event you are passing to the subscriber",
            "required": false
        },
        {
            "id": "problem_throughputevent",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide throughput of events you are passing to the subscriber",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 4,
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
