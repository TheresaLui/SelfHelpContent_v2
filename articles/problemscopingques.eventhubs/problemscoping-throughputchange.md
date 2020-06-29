<properties
pageTitle="Request to change Throughput unit"
description="Unable to retrieve diagnostics or log information"
service="microsoft.eventhubs"
resource="unableToGetLogs"
authors="mksuni"
ms.author="mksuni"
displayOrder=""
selfHelpType="problemScopingQuestions"
supportTopicIds="32636956"
resourceTags=""
productPesIds="16125"
cloudEnvironments="public, Fairfax, usnat, ussec"
articleId="eh-throughput"
schemaVersion="1"
	ownershipId="AzureMessaging_Common"
/>
# Request to change Throughput unit
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Request to change Throughput unit",
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
            "id": "problem_TUQuota",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "What would you like to change your TU count to (max 40 TUs for Standard, please explore Event Hubs Dedicated)? ",
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