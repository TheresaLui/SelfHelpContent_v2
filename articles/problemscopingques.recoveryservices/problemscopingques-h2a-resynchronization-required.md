<properties
         pageTitle="Scoping questions for Hyper-V VM resynchronization failure"
         description="Scoping questions for Hyper-V VM  resynchronization failure"
         authors="ashishgangwar"
	     ms.author="asgang"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32536448"
         productPesIds="16370"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
	     articleId="c791b57a-6fd5-40c8-975f-7c7ba6d9e9b7"
	ownershipId="Compute_SiteRecovery"
/>
# Questions Hyper-V VM resynchronization failure 
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Hyper-V VM resynchronization failure",
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
