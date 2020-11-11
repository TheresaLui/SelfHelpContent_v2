<properties
pageTitle="Performance issues due to high send latency"
description="Performance issues due to high send latency"
service="microsoft.eventhubs"
resource="highsendlatency"
authors="mksuni"
ms.author="mksuni"
displayOrder=""
selfHelpType="problemScopingQuestions"
supportTopicIds="32636941"
resourceTags=""
productPesIds="16125"
cloudEnvironments="public, Fairfax, usnat, ussec"
articleId="eh-high-send-latency"
schemaVersion="1"
	ownershipId="AzureMessaging_Common"
/>
# Performance issues due to high send latency
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Performance issues due to high send latency",
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
            "id": "problem_issueFrequency",
            "order": 3,
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
            "id": "problem_locationofcode",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Are you running the code from Azure or On-premise or external cloud provider? If Azure, please specify the Azure service name and specific resource name.",
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
            "id": "problem_currentLatency",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "Provide current latency of the request(s)",
            "required": false
        },
        {
            "id": "problem_expectedLatency",
            "order": 7,
            "controlType": "textbox",
            "displayLabel": "Provide the expected latency of the request(s)",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 8,
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