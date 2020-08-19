<properties
	articleId="adla-portal-clienttool-issues"
	pageTitle="Scoping Questions for ADLA Portal and client tool issues"
	description="Scoping Questions for ADLA Portal and client tool issues"
	authors="guyhay, lisaliu, v-anukar"
	ms.author="guyhay, lisaliu, v-anukar"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32680645"
	productPesIds="15940"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_AzureDataLakeAnalytics"
/>
# ADLA Portal and client tooling issues
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
