<properties
         pageTitle="Scoping questions for agentless dependency analysis"
         description="Scoping questions for agentless dependency analysis"
         authors="musa-57"
         ms.author="hamusa"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32691004"
         productPesIds="16348"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="4060b4a6-6e58-45cc-8ad7-a2965d59becq"
	ownershipId="Compute_AzureMigrate"
/>

# Dependency Visualization

---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Agentless dependency analysis",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "appliance_name",
            "order": 1,
            "visibility": "null",
            "controlType": "textbox",
            "displayLabel": "Provide the name of the appliance on which you have set up agentless dependency analysis.",
            "watermarkText": "E.g. AapplianceDC1",
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
