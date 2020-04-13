<properties
         pageTitle="Scoping questions for V2A failover"
         description="Scoping questions for V2A failover"
         authors="ashishgangwar"
         ms.author="asgang"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32680608"
         productPesIds="16370"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="4b342a85-0813-4b4d-b7d0-43639892e013"
	ownershipId="Compute_SiteRecovery"
/>
# Questions for V2A failover

---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "V2A failover",
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
