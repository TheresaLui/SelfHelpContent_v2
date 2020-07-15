<properties
         pageTitle="Scoping questions for unable to delete vault"
         description="Scoping questions for unable to delete vault"
         authors="srinathvasireddy"
	 ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32632791"
         productPesIds="15207"
         cloudEnvironments="public, fairfax, usnat, ussec"
         schemaVersion="1"
		articleId="e5e2dea8-3a55-4066-b3e2-29b96afa4357"
	ownershipId="StorageMediaEdge_Backup"
/>
# Questions for unable to delete vault
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Unable to delete vault",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "error_message",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Provide the error message that are you seeing:",
            "watermarkText": "Copy and paste error message text here",
            "required": true
        },
        {
            "id": "basic_troubleshooting_multiselect",
            "order": 2,
            "controlType": "multiselectdropdown",
            "infoBalloonText": "Check delete a <a href='https://docs.microsoft.com/azure/backup/backup-azure-delete-vault'>Recovery Services vault</a> article",
            "displayLabel": "Select the troubleshooting steps that you have performed:",
            "dropdownOptions": [
                {
                    "value": "Ensured all the protected servers are unregistered from the backup infrastructure blade",
                    "text": "Ensured all the protected servers are unregistered from the backup infrastructure blade"
                },
                {
                    "value": "Ensured all the protected servers are unregistered from the backup items blade",
                    "text": "Ensured all the protected servers are unregistered from the backup items blade"
                },
                {
                    "value": "Ensured all the storage account is unregistered from the backup infrastructure blade",
                    "text": "Ensured all the storage account is unregistered from the backup infrastructure blade"
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
