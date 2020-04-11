<properties
         pageTitle="Scoping questions for configuration server issues & queries "
         description="Scoping questions for configuration server issues & queries "
         authors="ashishgangwar,TobyTu"
         ms.author="asgang"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32593224"
         productPesIds="16370"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="8ppb4fde-7000-4e97-b711-4b07ac45db50"
	ownershipId="Compute_SiteRecovery"
/>
# Configuration server issues and queries 

---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Configuration server issues and queries",
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
