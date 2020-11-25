<properties
         pageTitle="Scoping questions for post-migration failures"
         description="Scoping questions for post-migration failures"
         authors="anvar-ms"
         ms.author="anvar"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32755166"
         productPesIds="16348"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="5sd0e5a6-4488-77c7-98bf-70918fcee374"
	ownershipId="Compute_AzureMigrate"
/>

# Not able to connect to the VM after migration

---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Post-migration VM boot or connection failed",
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
