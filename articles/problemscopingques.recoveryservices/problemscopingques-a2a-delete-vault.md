<properties
         pageTitle="Scoping questions for deleting a vault"
         description="Scoping questions for deleting a vault"
         authors="TobyTu"
         ms.author="aaronmax"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32592055"
         productPesIds="16370"
         cloudEnvironments="public"
         schemaVersion="1"
         articleId="q2ade906-df87-4222-9534-98223c9c0527"
/>

# Delete a vault
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
            "watermarkText": "Open a new tab, navigate to Recovery Services Vault, click on Jobs & paste error or job id of failed re-protect job",
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
                }
            ],
            "required": true
        },
       {
            "id": "problem_start_time",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "watermarkText": "Enter local time",
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
