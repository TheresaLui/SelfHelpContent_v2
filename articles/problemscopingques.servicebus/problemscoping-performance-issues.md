<properties
pageTitle="Performance and Latency issues"
description="Performance and Latency issues"
service="microsoft.servicebus"
resource="errorMessageTypes"
authors="mksuni"
ms.author="mksuni"
displayOrder=""
selfHelpType="problemScopingQuestions"
supportTopicIds="32633389"
resourceTags=""
productPesIds="13186"
cloudEnvironments="public, Fairfax, usnat, ussec"
articleId="sb-performance-issue"
schemaVersion="1"
	ownershipId="AzureMessaging_Common"
/>
# Performance and Latency Issues
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Performance and Latency issues",
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
            "id": "problem_requestInfo",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "What request(s) is(are) having a latency issue?",
            "watermarkText": "Enter the request URL",
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
            "id": "problem_LocationOfClient",
            "order": 8,
            "controlType": "textbox",
            "displayLabel": "What's the location of client experiencing performance issue (for e.g. OnPrem, On Azure, Region etc). If Azure, please specify the Azure service name and specific resource name.",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 9,
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
