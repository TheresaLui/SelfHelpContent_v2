<properties
         pageTitle="ISV tools (non Microsoft tools)"
         description="ISV tools (non Microsoft tools)"
         authors="ms-psharma"
        ms.author="panshar"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32755185"
         productPesIds="16348"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
        articleId="129cefc-b199-11ea-b3de-0242ac130004"
	ownershipId="Compute_AzureMigrate"
/>
# ISV tools (non Microsoft tools)
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "ISV tools (non Microsoft tools)",
    "fileAttachmentHint": "",
    "formElements": [
          {
            "id": "tool_name",
            "order": 1,
            "visibility": "null",
            "controlType": "textbox",
            "displayLabel": "Provide the name of the tool",
            "watermarkText": "E.g. Rackware",
            "required": false
        },
            {
            "id": "project_name",
            "order": 2,
            "visibility": "null",
            "controlType": "textbox",
            "displayLabel": "Provide the name of the project",
            "watermarkText": "E.g. MyContosoProject",
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 4,
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
