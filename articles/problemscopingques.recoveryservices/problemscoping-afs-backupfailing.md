<properties
         pageTitle="Scoping questions for Azure File share backup failure"
         description="Scoping questions for Azure File share backup failure"
         authors="srinathvasireddy"
	 ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32599715"
         productPesIds="15207"
         cloudEnvironments="public, fairfax, usnat, ussec"
         schemaVersion="1"
	 articleId="70ae6569-0d21-4910-9fb2-1c1b7fcd7962"
	ownershipId="StorageMediaEdge_Backup"
/>
# Questions for Azure File share backup failure
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Azure File share backup failure",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "storage_account_name",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Which storage account(s) is experiencing the problem?",
            "watermarkText": "Enter the name of the storage account(s)",
	     "dynamicDropdownOptions": {
            "uri": "/subscriptions/{subscriptionid}/resources?api-version=2018-05-01&$filter=resourceType eq 'Microsoft.Storage/storageAccounts' or resourceType eq 'Microsoft.ClassicStorage/storageAccounts'",
            "jTokenPath": "value",
            "textProperty": "name",
            "valueProperty": "id",
            "textPropertyRegex": ".*",
	    "defaultDropdownOptions": {
                "value": "dont_know_answer",
                "text": "Other, don't know or not applicable"
            }
          },
            "required": false
        },
        {
            "id": "fileshare_Name",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Provide the name(s) of the File Share whose backup is failing?",
            "watermarkText": "Enter file share name(s) comma separated",
            "required": false
        },
        {
            "id": "jobID_Name",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Enter the failed backup job Activity ID:",
            "watermarkText": "Ex. cace7461-dd3c-4e38-b4db-38dc57fdee7b",
            "required": false
        },
        {
            "id": "basic_troubleshooting_multiselect",
            "order": 4,
            "controlType": "multiselectdropdown",
            "infoBalloonText": "Check Azure File Share backup <a href='https://aka.ms/BKP-AFS-backuptshooting'>Troubleshooting</a> article",
            "displayLabel": "Select the troubleshooting steps that you have performed:",
            "dropdownOptions": [
                {
                    "value": "Ensured the protected file share is exists",
                    "text": "Ensured the protected file share is exists"
                },
                {
                    "value": "Ensured the storage account exists in the Resource Group",
                    "text": "Ensured the storage account exists in the Resource Group"
                },
                {
                    "value": "Ensured the storage account is supported by File Share backup",
                    "text": "Ensured the storage account is supported by File Share backup"
                },
                {
                    "value": "Ensured the Azure File Share max. snapshot limit is not reached",
                    "text": "Ensured the Azure File Share max. snapshot limit is not reached"
                },
                {
                    "value": "Ensured the storage account is not in locked state",
                    "text": "Ensured the storage account is not in locked state"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "error_message",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "Provide the error message that you are seeing:",
            "watermarkText": "Copy and paste error message text here",
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 6,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 7,
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
