<properties
pageTitle="All Issues"
description="All Issues"
service="Microsoft.NotificationHubs"
resource="allIssues"
authors="vimunuku"
ms.author="vimunuku"
displayOrder=""
selfHelpType="problemScopingQuestions"
supportTopicIds="32565576"
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
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 2,
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
        },
        {
        "id": "notificationhubs_namespaces",
        "order": 3,
        "controlType": "multiselectdropdown",
        "displayLabel": "Notification Hub namespace names",
        "watermarkText": "Choose an option",
        "required": false,
        "dynamicDropdownOptions": {
            "uri": "/subscriptions/{subscriptionid}/resourcegroups/{resourcegroup}/providers/microsoft.notificationhubs/namespaces/{resourceName}/notificationhubs?&api-version=2016-03-01",
            "jTokenPath": "value",
            "textProperty": "name",
            "valueProperty": "name",
            "valuePropertyRegex": "^+$",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Not applicable/No namespaces available"
                }
            }
        }
    ],
    "$schema": "SelfHelpContent"
}
---