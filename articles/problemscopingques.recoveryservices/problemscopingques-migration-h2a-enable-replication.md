<properties
         pageTitle="Scoping questions for Hyper-V VM protection failure"
         description="Scoping questions for Hyper-V VM  protection failure"
         authors="ashishgangwar"
	     ms.author="asgang"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32680606"
         productPesIds="16370"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
	     articleId="279514ca-0ada-4391-8e9a-d3c287111dd9"
	ownershipId="Compute_SiteRecovery"
/>
# Fail to enable protection for Hyper-V VM 
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Hyper-V VM  protection failure",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "vm_facing_issue",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Which virtual machine is experiencing the problem?",
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
