<properties
         pageTitle="Resource move to another subscription"
         description="Resource move to another subscription"
         authors="ms-psharma"
        ms.author="panshar"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32675728"
         productPesIds="16348"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
        articleId=""
	ownershipId="Compute_AzureMigrate"
/>
# ISV tools (non Microsoft tools)
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Resource move to another subscription",
    "fileAttachmentHint": "",
    "formElements": [
          {
            "id": "service_name",
            "order": 1,
            "visibility": "null",
            "controlType": "textbox",
            "displayLabel": "Provide the name of the service",
            "watermarkText": "E.g. Virtual machines for Windows",
            "required": false
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
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "hints": []
        }
    ],
    "$schema": "SelfHelpContent"
}
---
