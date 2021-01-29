<properties
         pageTitle="Scoping questions for Test Migrate failures"
         description="Scoping questions for Test Migrate failures"
         authors="anvar-ms"
         ms.author="anvar"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32755177"
         productPesIds="16348"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="5sd0e5a6-2266-46c7-83bf-71018fcee374"
	ownershipId="Compute_AzureMigrate"
/>

# Test Migrate Operation Failed

---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Test Migrate operation failed",
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
