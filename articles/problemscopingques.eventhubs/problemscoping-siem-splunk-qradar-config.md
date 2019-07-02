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
cloudEnvironments="public"
articleId="eh-siem-qradar-splunk-config"
schemaVersion="1"
/>
# Questions on Configuring Qradar, Splunk or SIEM
---
{
    "subscriptionRequired": true,
    "title": "Questions on Configuring Qradar, Splunk or SIEM",
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
            "id": "problem_capacityUnits"
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "How many capacity units are your requesting for?",
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
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Do you see incoming/outgoing requests or messages on the Azure Portal under the Event Hubs metrics section ?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide any additional details ,
            "required": false,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---