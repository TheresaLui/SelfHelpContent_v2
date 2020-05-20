<properties
         pageTitle="Scoping questions for Recovery services vault deletion failure"
         description="Scoping questions for Recovery services vault deletion failure"
         authors="genlin"
         ms.author="asgang"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32592050"
         productPesIds="16370"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="2b342a85-2011-8811-b7d0-43639892e013"
	ownershipId="Compute_SiteRecovery"
/>
# Questions on Deleting the vault  
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Recovery services vault deletion failure",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "vm_facing_issue",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Which recovery services vault can you not delete?",
            "watermarkText": "Enter the name of the affected  recovery services vault",
            "required": true
        },
        {
            "id": "Basic_troubleshooting_multiselect",
            "order": 4,
            "controlType": "multiselectdropdown",
            "displayLabel": "Select the troubleshooting steps that you have completed:",
            "dropdownOptions": [
                {
                    "value": "Confirmed all Site Recovery replications were deleted",
                    "text": "Verified that all Site Recovery replications are deleted"
                },
                {
                    "value": "Confirmed all backups were deleted",
                    "text": "Verified that all backups are deleted"
                },
                {
                    "value": "Tried force deleting the vault using powershell",
                    "text": "Tried to force delete the vault by using PowerShell"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 6,
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
