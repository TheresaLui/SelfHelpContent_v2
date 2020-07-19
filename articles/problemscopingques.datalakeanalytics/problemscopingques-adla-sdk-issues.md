<properties
	articleId="adla-sdk-issues"
	pageTitle="Scoping Questions for difficulties while using ADL SDK"
	description="Scoping Questions for difficulties while using ADL SDK"
	authors="guyhay, lisaliu, v-anukar"
	ms.author="guyhay, lisaliu, v-anukar"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32680646"
	productPesIds="15940"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_AzureDataLakeAnalytics"
/>
# Difficulties using ADL SDK
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "ADLA Portal and client tooling issues with using ADL portal",
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
            "id": "request_id",
            "order": 140,
            "controlType": "textbox",
            "displayLabel": "Request ID in CloudException",
            "watermarkText": "Please provide the requestID/operationID in the cloud exception",
            "required": false
        },
        {
            "id": "nugetpackage_version",
            "order": 150,
            "controlType": "textbox",
            "displayLabel": "Version of Nuget Package",
            "watermarkText": "Please provide the version of nuget package",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 500,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details about the issue",
            "watermarkText": "Please provide the details including the full stack trace with exception obtained while using ADLA SDK",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
