<properties
         pageTitle="Scoping questions for Configuration server issues & queries "
         description="Scoping questions for Configuration server issues & queries "
         authors="ashishgangwar"
         ms.author="asgang"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32680603"
         productPesIds="16370"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="1b342a85-0813-4b4d-b7d0-43639892e013"
	ownershipId="Compute_SiteRecovery"
/>
# Questions for Configuration server issues & queries 

---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Configuration server issues & queries",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "vm_facing_issue",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Provide Configuration server name",
            "watermarkText": "Enter the name of the Configuration server",
            "required": true
        },
        {
            "id": "jobID_Name",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Enter the failed Site Recovery job Activity ID if applicable:",
            "watermarkText": "Ex. cace7461-dd3c-4e38-b4db-38dc57fdee7b",
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
