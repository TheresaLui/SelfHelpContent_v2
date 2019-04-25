<properties
         pageTitle="Scoping questions for Recovery services vault deletion failure"
         description="Scoping questions for Recovery services vault deletion failure"
         authors="ashishgangwar"
	     ms.author="asgang"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32592055"
         productPesIds="16370"
         cloudEnvironments="public"
         schemaVersion="1"
	    articleId="06d2190a-f0a0-479b-ab9e-48a98b9c9bc3"
/>
# Questions on Deleting the vault  
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Recovery Services vault deletion failure",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "vm_facing_issue",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Which Recovery Services vault was you unable to delete?",
            "watermarkText": "Enter the name of the recovery services vault",
            "required": true
        },
        {
            "id": "Basic_troubleshooting_multiselect",
            "order": 4,
            "controlType": "multiselectdropdown",
            "displayLabel": "Select the troubleshooting steps you have completed:",
            "dropdownOptions": [
                {
                    "value": "Confirmed all Site Recovery replications were deleted",
                    "text": "Check all Site Recovery replications are deleted"
                },
                {
                    "value": "Confirmed all backups were deleted",
                    "text": "Check all backups are deleted"
                },
                {
                    "value": "Tried force deleting the vault by using PowerShell",
                    "text": "Tried force deleting the vault by using PowerShell"
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
    ]
}
---
