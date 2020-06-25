<properties
         pageTitle="Cannot find existing project"
         description="Cannot find existing project"
         authors="ms-psharma"
        ms.author="panshar"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32678719"
         productPesIds="16348"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
        articleId="47ac72e8-0d7c-4659-ba46-b0271358365e"
	ownershipId="Compute_AzureMigrate"
/>
# Cannot find existing project
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Cannot find existing project",
    "fileAttachmentHint": "",
    "formElements": [
          {
            "id": "project_name",
            "order": 1,
            "visibility": "null",
            "controlType": "textbox",
            "displayLabel": "Provide the name of the project",
            "watermarkText": "E.g. MyContosoProject",
            "required": false
        },
        {
            "id": "access_check",
            "order": 2,
            "visibility": "null",
            "controlType": "dropdown",
            "displayLabel": "Do you have required permissions to view this project?",
            "watermarkText": "Select",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
            ],
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
