<properties
         pageTitle="Scoping questions for issue with vault credential"
         description="Scoping questions for issue with vault credential"
         authors="srinathv"
	 ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32632786"
         productPesIds="15207"
         cloudEnvironments="public, fairfax, usnat, ussec"
         schemaVersion="1"
	 articleId="c3a606de-ec65-48ad-840c-c623331d42f0"
	ownershipId="StorageMediaEdge_Backup"
/>
# Questions for issue with vault credential
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "issue with vault credential",
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
            "infoBalloonText": "Check Azure Backup agent <a href='https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot#unable-to-download-vault-credential-file'>Troubleshooting</a> article for vault credential issue",
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
                    "value": "I am using vault credential downloaded within 48hrs",
                    "text": "I am using vault credential downloaded within 48hrs"
                },
                {
                    "value": "The vault credentials are not saved on a network location",
                    "text": "The vault credentials are not saved on a network location"
                },
                {
                    "value": "Machine's date and time is configured correctly",
                    "text": "Machine's date and time is configured correctly"
                },
                {
                    "value": "If proxy is enabled, then browser settings are configured to use proxy",
                    "text": "If proxy is enabled, then browser settings are configured to use proxy"
                },
                {
                    "value": "If performing restore, ensured both original and alternate server are registered to the same vault",
                    "text": "If performing restore, ensured both original and alternate server are registered to the same vault"
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
