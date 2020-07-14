<properties
pageTitle="Request for Partition change"
description="Request for Partition change"
service="microsoft.eventhubs"
resource="partitionchange"
authors="mksuni"
ms.author="mksuni"
displayOrder=""
selfHelpType="problemScopingQuestions"
supportTopicIds="32636955"
resourceTags=""
productPesIds="16125"
cloudEnvironments="public, Fairfax, usnat, ussec"
articleId="eh-partition-change-request"
schemaVersion="1"
	ownershipId="AzureMessaging_Common"
/>
# Request for Partition change
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Request for Partition change",
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
            "id": "problem_partitionchangecount",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "What would you like to change your current partition count to?",
            "watermarkText": "Please enter the count to update the your current partition",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional Details",
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