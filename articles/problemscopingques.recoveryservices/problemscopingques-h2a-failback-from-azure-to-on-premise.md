<properties
         pageTitle="Scoping questions for Hyper-V VM failback failure"
         description="Scoping questions for Hyper-V VM  failback failure"
         authors="ashishgangwar"
	     ms.author="asgang"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32536406"
         productPesIds="16370"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
	     articleId="304ee2b6-672f-4c27-949a-b47abafe5a61"
	ownershipId="Compute_SiteRecovery"
/>
# Failback from Azure to on-premises Hyper-V VM
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Hyper-V VM failback failure",
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
