<properties
         pageTitle="Scoping questions for issue in vault credential download"
         description="Scoping questions for issue in vault credential download"
         authors="srinathv"
 	 ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32632797"
         productPesIds="15207"
         cloudEnvironments="public, fairfax, usnat, ussec"
         schemaVersion="1"
  	 articleId="2e956193-880f-437c-942e-575465e86ce2"
	ownershipId="StorageMediaEdge_Backup"
/>
# Questions for issue in vault credential download
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Issue in vault credential download",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "error_message",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Provide the error message that are you seeing:",
            "watermarkText": "Copy and paste error message text here",
            "required": false
        },
        {
            "id": "vault_name",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Provide the vault name from which you are trying to download vault credential:",
            "watermarkText": "ex. contoso_vault",
            "required": false
        },
        {
            "id": "basic_troubleshooting_multiselect",
            "order": 3,
            "controlType": "multiselectdropdown",
            "infoBalloonText": "Check Azure Backup agent <a href='https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot#unable-to-download-vault-credential-file'>Troubleshooting</a> article",
            "displayLabel": "Select the troubleshooting steps that you have performed:",
            "dropdownOptions": [
                {
                    "value": "Tried downloading vault credential file using a different browser",
                    "text": "Tried downloading vault credential file using a different browser"
                },
                {
                    "value": "Ensured the subscription is enabled and not expired",
                    "text": "Ensured the subscription is enabled and not expired"
                },
                {
                    "value": "Ensured the firewall rules are not blocking vault credential file download",
                    "text": "Ensured the firewall rules are not blocking vault credential file download"
                },
                {
                    "value": "Ensured user account has permissions to download vault credential file",
                    "text": "Ensured user account has permissions to download vault credential file"
                },
                {
                    "value": "Ensured maximum machines registered per vault limit is not reached",
                    "text": "Ensured maximum machines registered per vault limit is not reached"
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
    ],
    "$schema": "SelfHelpContent"
}
---
