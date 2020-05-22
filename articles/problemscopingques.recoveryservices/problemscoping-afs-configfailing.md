<properties
         pageTitle="Scoping questions for issue configuring Azure File share backup"
         description="Scoping questions for issue configuring Azure File share backup"
         authors="srinathvasireddy"
	       ms.author="srinathvasireddy"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32612212"
         productPesIds="15207"
         cloudEnvironments="public, fairfax, usnat, ussec"
         schemaVersion="1"
	 articleId="a7f05b99-4465-4c48-819b-b8e64da4d9eb"
	ownershipId="StorageMediaEdge_Backup"
/>
# Questions for issue configuring Azure File share backup
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Issue configuring Azure File share backup",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "For issue configuring Azure File share backup",
        "description": "These diagnostics will check for errors.",
        "insightNotAvailableText": "We didn't find any problems"
    },
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
            "displayLabel": "Provide the name(s) of the File Share whose backup configuration is failing?",
            "watermarkText": "Enter file share name(s) comma separated",
            "required": false
        },
        {
            "id": "jobID_Name",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Enter the failed configuration job Activity ID:",
            "watermarkText": "Ex. cace7461-dd3c-4e38-b4db-38dc57fdee7b",
            "required": false
        },
        {
            "id": "basic_troubleshooting_multiselect",
            "order": 4,
            "controlType": "multiselectdropdown",
            "infoBalloonText": "Check Azure File Share configuring backup <a href='https://aka.ms/BKP-AFS-Tshooting'>Troubleshooting</a> article",
            "displayLabel": "Select the troubleshooting steps that you have performed:",
            "dropdownOptions": [
                {
                    "value": "Ensured the storage account don't have Virtual Networks or Firewall enabled",
                    "text": "Ensured the storage account don't have Virtual Networks or Firewall enabled"
                },
                {
                    "value": "Ensured the storage account is not already associated with another vault",
                    "text": "Ensured the storage account is not already associated with another vault"
                },
                {
                    "value": "Ensured the storage account is supported by File Share backup",
                    "text": "Ensured the storage account is supported by File Share backup"
                },
                {
                    "value": "Ensured the File Share is not already protected in the same vault",
                    "text": "Ensured the File Share is not already protected in the same vault"
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
            "required": true,
            "diagnosticInputRequiredClients": "Portal"
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
