<properties
         pageTitle="Scoping questions for agent health and notification"
         description="Scoping questions for agent health and notification"
         authors="An-mol"
        ms.author="anvar"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32675735"
         productPesIds="16348"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
        articleId="3a479135-f725-4996-98b2-fcf529877594"
	ownershipId="Compute_AzureMigrate"
/>
# Agent health and notification
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Agent health and notification",
    "fileAttachmentHint": "",
    "formElements": [
          {
            "id": "appliance_name",
            "order": 1,
            "visibility": "null",
            "controlType": "textbox",
            "displayLabel": "Provide the name of the appliance",
            "watermarkText": "E.g. MyContosoAppliance",
            "required": true
        },
        {
            "id": "agent_name",
            "order": 2,
            "visibility": "null",
            "controlType": "textbox",
            "displayLabel": "Provide the name of the agent that has issues",
            "watermarkText": "E.g. Assessment agent",
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
