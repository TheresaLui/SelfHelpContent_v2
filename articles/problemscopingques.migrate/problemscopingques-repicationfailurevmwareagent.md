<properties
         pageTitle="Scoping questions for replication failures"
         description="Scoping questions for replication failures"
         authors="anvar-ms"
         ms.author="anvar"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32755172"
         productPesIds="16348"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="5saae5a6-4466-77c7-98bf-70918fcee123"
	ownershipId="Compute_AzureMigrate"
/>

# Replication failures in agent-based VMware migration

---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Replication failed",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "VM_name",
            "order": 1,
            "visibility": "null",
            "controlType": "textbox",
            "displayLabel": "Provide the name of the virtual machines in which you are facing the issue.",
            "watermarkText": "E.g. MyContosoVM1, MyContosoVM2",
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
