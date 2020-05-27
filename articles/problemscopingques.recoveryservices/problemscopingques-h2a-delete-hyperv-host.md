<properties
         pageTitle="Scoping questions for Hyper-V server deletion failure"
         description="Scoping questions for Hyper-V server deletion failure"
         authors="ashishgangwar"
         ms.author="asgang"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32592052"
         productPesIds="16370"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="c0eb3ade-b5e3-44b5-a952-c587b51f7ca8"
	ownershipId="Compute_SiteRecovery"
/>
# Hyper-V server deletion failure
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Hyper-V server deletion failure",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "vm_facing_issue",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Which Hyper-V server is experiencing the problem?",
            "watermarkText": "Enter the name of the Hyper-V server",
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
    ]
}
---
