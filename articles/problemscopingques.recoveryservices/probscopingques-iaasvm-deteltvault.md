<properties
         pageTitle="Scoping questions for Recovery services vault deletion failure"
         description="Scoping questions for Recovery services vault deletion failure"
         authors="ashishgangwar, TobyTu"
	     ms.author="asgang"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32592055"
         productPesIds="16370"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
	    articleId="06d2190a-f0a0-479b-ab9e-48a98b9c9bc3"
	ownershipId="Compute_SiteRecovery"
/>
# Questions on Deleting the vault  
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Delete a vault",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "vault_name",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Provide name of the vault",
            "watermarkText": "Enter name(s) to scope down quickly",
            "required": true
        },
        {
            "id": "error_id",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Provide error ID or job ID of the failed operation",
            "watermarkText": "Enter in the error or job ID",
            "infoBalloonText": "Open a new tab, navigate to Recovery Services Vault, click on Jobs & paste error or job ID of failed re-protect job",
            "required": false
        },
        {
            "id": "tried_steps",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "I have gone through steps provided in the following articles",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Delete a Site Recovery Services vault",
                    "text": "Delete a Site Recovery Services vault"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
       {
            "id": "problem_start_time",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "watermarkText": "Enter in local time",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 5,
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
