<properties
         pageTitle="Scoping questions for my VM health is critical"
         description="Scoping questions for my VM health is critical"
         authors="ashishgangwar,TobyTu"
         ms.author="asgang"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32642158"
         productPesIds="16370"
         cloudEnvironments="public, Fairfax"
         schemaVersion="1"
         articleId="8ppb5fde-7000-4e97-b711-4b07ac45db50"
	ownershipId="Compute_SiteRecovery"
/>
# My VM health is critical
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "My VM health is critical",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "vm_facing_issue",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Which virtual machine(s) is experiencing the problem?",
            "watermarkText": "Enter the name of the virtual machine(s)",
            "required": true
        },
        {
            "id": "jobID_Name",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Enter the failed Site Recovery job Activity ID:",
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
