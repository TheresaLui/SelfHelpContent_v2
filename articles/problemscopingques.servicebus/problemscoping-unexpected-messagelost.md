<properties
pageTitle="Unexpected Service Behavior"
description="Message Lost or duplicate message issues"
service="microsoft.servicebus"
resource="errorMessageTypes"
authors="mksuni"
ms.author="mksuni"
displayOrder=""
selfHelpType="problemScopingQuestions"
supportTopicIds="32633401,32633397"
resourceTags=""
productPesIds="13186"
cloudEnvironments="public, Fairfax, usnat, ussec"
articleId="sb-message-lost-issue"
schemaVersion="1"
	ownershipId="AzureMessaging_Common"
/>
# Message Lost or duplicate message issues
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Message Lost or duplicate message issues",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "servicebus_feature",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Service Bus feature",
            "watermarkText": "Choose an option",
            "required": false,
            "dropdownOptions": [{
                "value": "Queues",
                "text": "Queues"
            }, {
                "value": "Topics",
                "text": "Topics"
            }]
        },
        {
            "id": "servicebus_queues",
            "order": 2,
            "controlType": "multiselectdropdown",
            "displayLabel": "Queue names",
            "watermarkText": "Choose an option",
            "required": false,
            "visibility": "servicebus_feature != null && servicebus_feature == Queues",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/resourcegroups/{resourcegroup}/providers/Microsoft.ServiceBus/namespaces/{resourceName}/queues?&api-version=2015-08-01",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "name",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Not applicable/No queues available"
                }
            }
        },
        {
            "id": "servicebus_topics",
            "order": 3,
            "controlType": "multiselectdropdown",
            "displayLabel": "Topic names",
            "watermarkText": "Choose an option",
            "required": false,
            "visibility": "servicebus_feature != null && servicebus_feature == Topics",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/resourcegroups/{resourcegroup}/providers/Microsoft.ServiceBus/namespaces/{resourceName}/topics?&api-version=2015-08-01",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "name",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Not applicable/No topics available"
                }
            }
        },
        {
            "id": "problem_start_time",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_messageId",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide the Message ID and Enqueue time for the message",
            "watermarkText": "Enter the Message ID",
            "required": true
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