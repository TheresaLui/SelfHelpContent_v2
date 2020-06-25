<properties
	articleId="adla-general-advisory"
	pageTitle="Scoping Questions for ADLA General Advisory"
	description="Scoping Questions for ADLA General Advisory"
	authors="guyhay, lisaliu"
	ms.author="guyhay, lisaliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32680880"
	productPesIds="15940"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_AzureDataLakeAnalytics"
/>
# ADLA General Advisory
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "ADLA General Advisory",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "What time did the problem begin?",
            "required": true
        },
        {
            "id": "problem_end_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate time when the problem stopped occurring. If the issue is ongoing, leave this field blank",
            "required": false
        },
        {
            "id": "adla_account_name",
            "order": 130,
            "controlType": "textbox",
            "displayLabel": "ADLA account name",
            "watermarkText": "Please provide the Azure Data Lake Analytics Account name",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 500,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details about the issue",
            "watermarkText": "Please provide the details including the full error message obtained while using ADL portal blade",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
