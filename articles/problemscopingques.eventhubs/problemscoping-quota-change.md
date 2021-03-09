<properties
pageTitle="Quota Issues"
description="Quota Issues"
service="microsoft.eventhubs"
resource="quotaChangeRequest"
authors="mksuni"
ms.author="mksuni"
displayOrder=""
selfHelpType="problemScopingQuestions"
supportTopicIds="32636952"
resourceTags=""
productPesIds="16125"
cloudEnvironments="public, Fairfax, usnat, ussec"
articleId="eh-quota-request"
schemaVersion="1"
	ownershipId="AzureMessaging_Common"
/>
# Quota Issues
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Quota Issues",
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
            "id": "problem_QuotaChange",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "What quota increase are you requesting for?",
            "required": false
        },
        {
            "id": "problem_Reason",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Enter your justification for increase the quota",
            "watermarkText": "Provide your reasoning for quota change request",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 5,
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