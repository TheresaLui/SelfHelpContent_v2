<properties
         pageTitle="Scoping questions for dependency visualization"
         description="Scoping questions for dependency visualization"
         authors="An-mol"
         ms.author="anvar"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32675744"
         productPesIds="16348"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="4060b4a6-6e58-45cc-8ad7-a2965d59becd"
	ownershipId="Compute_AzureMigrate"
/>

# Dependency Visualization

---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Creating, updating and exporting issues",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "machine_name",
            "order": 1,
            "visibility": "null",
            "controlType": "textbox",
            "displayLabel": "Provide the name of the machine on which you are facing issue.",
            "watermarkText": "E.g. MyMachine01",
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
