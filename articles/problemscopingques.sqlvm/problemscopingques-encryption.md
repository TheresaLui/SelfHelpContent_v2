<properties pageTitle="Encryption"
	 description="Encryption"
	 authors="yareyes"
     ms.author="yareyes"
	 selfHelpType="problemScopingQuestions"
	 supportTopicIds="32633505"
	 productPesIds="14745"
	 cloudEnvironments="public,fairfax, usnat, ussec"
	 schemaVersion="1"
	 articleId="0f9676d3-b4da-4110-b8d6-3841cf378b01"
	ownershipId="AzureData_AzureSQLVM"
/>
# Encryption
---
{
    "resourceRequired": false,
    "title": "Encryption",
    "fileAttachmentHint": null,
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start",
            "required": true
        },
        {
            "id": "type_of_encryption",
            "visibility": null,
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What type of encryption are you using?",
            "watermarkText": "Choose an option",
            "content": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Transparent Data Encryption (TDE)",
                    "value": "TDE"
                },
                {
                    "text": "TDE with Azure Key Vault",
                    "value": "TDE-AKV"
                },
                {
                    "text": "Other",
                    "value": "Other"
                },
                {
                    "text": "I’m not sure/don’t know",
                    "value": "dont_know_answer"
                }
            ],
            "dynamicDropdownOptions": null,
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
