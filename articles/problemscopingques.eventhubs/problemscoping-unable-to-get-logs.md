<properties
pageTitle="Unable to retrieve diagnostics or log information"
description="Unable to retrieve diagnostics or log information"
service="microsoft.eventhubs"
resource="unableToGetLogs"
authors="mksuni"
ms.author="mksuni"
displayOrder=""
selfHelpType="problemScopingQuestions"
supportTopicIds="32636953"
resourceTags=""
productPesIds="16125"
cloudEnvironments="public, Fairfax, usnat, ussec"
articleId="eh-unable-to-get-logs"
schemaVersion="1"
	ownershipId="AzureMessaging_Common"
/>
# Unable to retrieve diagnostics or log information
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Unable to retrieve diagnostics or log information",
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
            "id": "problem_saskeys",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Did you reset your SAS keys recently and When?",
            "required": false
        },
       {
            "id": "problem_monitoringdata",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "What Azure monitoring data are your trying to collect ?",
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