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
            "id": "eventhubs_namespaces",
            "order": 1,
            "controlType": "multiselectdropdown",
            "displayLabel": "Event Hubs",
            "watermarkText": "Choose an option",
            "required": false,
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/resourcegroups/{resourcegroup}/providers/Microsoft.EventHub/namespaces/{resourceName}/eventhubs?&api-version=2015-08-01",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "name",
                "valuePropertyRegex": "^+$",
                    "defaultDropdownOptions": {
                        "value": "dont_know_answer",
                        "text": "Not applicable/No event hubs available"
                    }
                }
        },
        {
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
          {
            "id": "problem_throttlingerrors",
            "order": 3,
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
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Are you running the code from Azure or On-premise or external cloud provider?",
            "required": true
        },
        {
            "id": "problem_sdkversion",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "Enter the SDK stack and SDK version you are using?",
            "required": false
        },
        {
            "id": "problem_messageprocessingtime",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "Has your message processing time increased (Yes/No)?",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 7,
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