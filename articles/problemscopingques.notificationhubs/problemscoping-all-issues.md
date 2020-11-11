<properties
pageTitle="All Issues"
description="All Issues"
service="Microsoft.NotificationHubs"
resource="allIssues"
authors="vimunuku"
ms.author="vimunuku"
displayOrder=""
selfHelpType="problemScopingQuestions"
supportTopicIds="32565576,32565577,32565578,32565579,32565580,32565581,32565582,32565583,32565584,32452753,32565571,32565573,32565574,32565575,32565569,32565570,32565572,32447211"
resourceTags=""
productPesIds="15973"
cloudEnvironments="public, Fairfax, usnat, ussec"
articleId="nh-all-issues"
schemaVersion="1"
	ownershipId="AzureMessaging_Common"
/>
# All Issues
---
{

    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "All Issues",
    "fileAttachmentHint": "",
    "formElements": [
        {
        "id": "notificationhubs_namespaces",
        "order": 1,
        "controlType": "multiselectdropdown",
        "displayLabel": "Notification Hub name",
        "watermarkText": "Choose an option",
        "required": false,
        "dynamicDropdownOptions": {
            "uri": "/subscriptions/{subscriptionid}/resourcegroups/{resourcegroup}/providers/microsoft.notificationhubs/namespaces/{resourceName}/notificationhubs?&api-version=2016-03-01",
            "jTokenPath": "value",
            "textProperty": "name",
            "valueProperty": "name",
            "defaultDropdownOptions": {
                "value": "dont_know_answer",
                "text": "Not applicable/No namespaces available"
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
            "id": "problem_description",
            "order": 3,
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
