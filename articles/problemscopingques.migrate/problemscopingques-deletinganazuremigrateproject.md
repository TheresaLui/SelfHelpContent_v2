<properties
         pageTitle="Deleting an Azure Migrate project"
         description="Deleting an Azure Migrate project"
         authors="ms-psharma"
        ms.author="panshar"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32683731"
         productPesIds="16348"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
        articleId="0f9a2d55-c412-4d41-b367-4a85e3932b4d"
	ownershipId="Compute_AzureMigrate"
/>
# Deleting an Azure Migrate project
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Deleting an Azure Migrate project",
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
            "displayLabel": "Do you have required permissions to delete this project?",
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
