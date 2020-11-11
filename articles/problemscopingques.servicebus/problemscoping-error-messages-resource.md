<properties
pageTitle="Error Messages"
description="Error Messages for various issues like Timeout , Connectivity , Create and delete operations etc."
service="microsoft.servicebus"
resource="errorMessageTypes"
authors="mksuni"
ms.author="mksuni"
displayOrder=""
selfHelpType="problemScopingQuestions"
supportTopicIds="32633395,32633409,32633400,32633396"
resourceTags=""
productPesIds="13186"
cloudEnvironments="public, Fairfax, usnat, ussec"
articleId="service-bus-error-msg-resource"
schemaVersion="1"
	ownershipId="AzureMessaging_Common"
/>
# Error Messages realted to Timeout , Connectivity , Create and delete
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Error messages",
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
            "id": "problem_issueFrequency",
            "order": 5,
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
            "id": "problem_errorMessageText",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide the exact error message including call stack, Tracking Id and timestamp, if any",
            "required": false,
            "useAsAdditionalDetails": false
        },
        {
            "id": "problem_ClientInformation",
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "Please specific the client library (.Net, .Net Standard, Java, Python, etc) you are using and the version number?",
            "watermarkText": "Clients used by the application and their version number",
            "required": false,
            "useAsAdditionalDetails": true
        },
        {
            "id": "problem_description",
            "order": 8,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": false,
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