<properties
pageTitle="Questions on Configuring Qradar, Splunk or SIEM"
description="Questions on Configuring Qradar, Splunk or SIEM"
service="microsoft.eventhubs"
resource="siemSplunkQradar"
authors="mksuni"
ms.author="mksuni"
displayOrder=""
selfHelpType="problemScopingQuestions"
supportTopicIds="32636947"
resourceTags=""
productPesIds="16125"
cloudEnvironments="public, Fairfax, usnat, ussec"
articleId="eh-siem-qradar-splunk-config"
schemaVersion="1"
	ownershipId="AzureMessaging_Common"
/>
# Questions on Configuring Qradar, Splunk or SIEM
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Questions on Configuring Qradar, Splunk or SIEM",
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
            "id": "problem_siempartner",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Which SIEM product are you using?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "qradar",
                    "text": "IBM QRadar"
                },
                 {
                    "value": "splunk",
                    "text": "Splunk"
                },
                 {
                    "value": "sumologic",
                    "text": "SumoLogic"
                },
                {
                    "value": "arcSight ",
                    "text": "ArcSight "
                },
                 {
                    "value": "syslogserver ",
                    "text": "Syslog server "
                }
            ]
        },
        {
            "id": "problem_metrics",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Do you see incoming/outgoing requests or messages on the Azure Portal under the Event Hubs metrics section ?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide any additional details",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---