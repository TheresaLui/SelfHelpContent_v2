<properties
pageTitle="Unexpected Service behavior or Errors"
description="Unexpected Service behavior or Errors"
service="microsoft.relay"
resource="errorMessageTypes"
authors="mksuni"
ms.author="mksuni"
displayOrder=""
selfHelpType="problemScopingQuestions"
supportTopicIds="32684546,32684545"
resourceTags=""
productPesIds="16123"
cloudEnvironments="public, Fairfax, usnat, ussec"
articleId="relay-issue-not-listed"
schemaVersion="1"
	ownershipId="AzureMessaging_Common"
/>
# Unexpected Service behavior or Errors
---
{
    "subscriptionRequired": true,
    "title": "Unexpected Service behavior or Errors",
    "resourceRequired": true,
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
            "id": "problem_errorMessageText",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide the exact error message including call stack, Tracking Id and timestamp, if any",
            "required": false
        },
        {
            "id": "problem_client",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What Client are your using with this resource",
            "required": false
        },
      {
            "id": "problem_sdk",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Which SDK are you using and please provide the SDK version as well",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Please provide the exact error message , timestamp, tracking ID, and call-stack",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---