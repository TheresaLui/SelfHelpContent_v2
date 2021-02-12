<properties
         pageTitle="Scoping questions for issue moving vault"
         description="Scoping questions for issue moving vault"
         authors="srinathvasireddy"
	 ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32632781"
         productPesIds="15207"
         cloudEnvironments="public, fairfax, usnat, ussec"
         schemaVersion="1"
	 articleId="fe9e184c-afe1-4a0f-a39d-a892c55c9849"
	ownershipId="StorageMediaEdge_Backup"
/>
# Questions for issue moving vault
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Issue moving vault",
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
            "infoBalloonText": "Check move <a href='https://docs.microsoft.com/azure/backup/backup-azure-move-recovery-services-vault'>Recovery Services vault</a> article",
            "displayLabel": "Select the troubleshooting steps that you have performed:",
            "dropdownOptions": [
                {
                    "value": "Ensured moving Recovery Services vault within supported region",
                    "text": "Ensured moving Recovery Services vault within supported region"
                },
                {
                    "value": "Ensured user account has subscription admin permission",
                    "text": "Ensured user account has subscription admin permission"
                },
                {
                    "value": "Moving between resource group, ensured both resource group are in the same subscription",
                    "text": "Moving between resource group, ensured both resource group are in the same subscription"
                },
                {
                    "value": "Moving between subscriptions, ensured both source and target subscription are in the same tenant ",
                    "text": "Moving between subscriptions, ensured both source and target subscription are in the same tenant "
                },
                {
                    "value": "Ensured that Azure Site Recovery is not configured in the vault",
                    "text": "Ensured that Azure Site Recovery is not configured in the vault"
                },
                {
                    "value": "Ensured vault does not have protected item types that prevent vault move",
                    "text": "Ensured vault does not have protected item types that prevent vault move"
                },
                {
                    "value": "Tried moving vault using PowerShell",
                    "text": "Tried moving vault using PowerShell"
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
