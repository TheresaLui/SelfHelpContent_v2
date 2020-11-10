<properties
pageTitle="Low message egress"
description="Low message egress"
service="microsoft.eventhubs"
resource="lowMessageEgress"
authors="mksuni"
ms.author="mksuni"
displayOrder=""
selfHelpType="problemScopingQuestions"
supportTopicIds="32636943"
resourceTags=""
productPesIds="16125"
cloudEnvironments="public, Fairfax, usnat, ussec"
articleId="eh-low-message-egress"
schemaVersion="1"
	ownershipId="AzureMessaging_Common"
/>
# Low message egress
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Low message egress",
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
            "id": "problem_throttlingerrors",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Do you see throttling errors?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "DontKnow",
                    "text": "I don't know"
                }
            ]
        },
        {
            "id": "problem_locationofcode",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Are you running the code from Azure or On-premise or external cloud provider?",
            "required": true
        },
        {
            "id": "problem_sdkversion",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Enter the SDK stack and SDK version you are using?",
            "required": false
        },
        {
            "id": "problem_messageprocessingtime",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "Has your message processing time increased (Yes/No)?",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 6,
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