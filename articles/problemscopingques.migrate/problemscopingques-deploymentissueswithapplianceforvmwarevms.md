<properties
         pageTitle="Scoping questions for deployment issues with appliance for physical servers (Configuration Server)"
         description="Scoping questions for deployment issues with appliance for physical servers (Configuration Server)"
         authors="anvar-ms"
        ms.author="anvar"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32755160"
         productPesIds="16348"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="9398f098-8c04-4de6-a4db-599612w805ea"
        ownershipId="Compute_AzureMigrate"/>

# Deployment issues with appliance for VMware servers (Configuration Server)

---
{
    "subscriptionRequired": false,
    "resourceRequired": false,
    "title": "Deployment issues with appliance for VMware servers (Configuration Server)",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "Whitelisting_URLs",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Have you whitelisted the URLs?",
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
            "id": "ports_opened",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Are the required ports open?",
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
            "id": "appliance_name",
            "order": 3,
            "visibility": "null",
            "controlType": "textbox",
            "displayLabel": "Provide the name of appliance (if applicable)",
            "watermarkText": "E.g. MyContosoAppliance",
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 5,
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
