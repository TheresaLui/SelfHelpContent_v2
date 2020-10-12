<properties
         pageTitle="Scoping questions for creating, updating and importing assessments"
         description="Scoping questions for creating, updating and importing assessments"
         authors="An-mol"
         ms.author="anvar"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32675741"
         productPesIds="16348"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="39abdc64-9b14-424f-8411-0b804b966bab"
	ownershipId="Compute_AzureMigrate"
/>

# Creating, updating and importing assessments

---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Creating, updating and exporting issues",
    "fileAttachmentHint": "",
    "formElements": [
         {
            "id": "API_used",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Are you using REST API to create/update/export assessment?",
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
