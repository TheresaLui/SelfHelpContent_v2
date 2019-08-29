<properties
	articleId=""
	pageTitle="Scoping Questions for installing ADLS within Visual Studio"
	description="Scoping Questions for installing ADLS within Visual Studio"
	authors="guyhay, lisaliu, v-anukar"
	ms.author="guyhay, lisaliu, v-anukar"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32680649"
	productPesIds="15940"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# ADLS installation issues within Visual Studio
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "ADLS installation issues within Visual Studio",
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
            "id": "visualstudio_version",
            "order": 150,
            "controlType": "textbox",
            "displayLabel": "Version of Visual Studio",
            "watermarkText": "Please provide the version of visual studio being used",
            "required": true
        },
        {
            "id": "datalakestudio_version",
            "order": 160,
            "controlType": "textbox",
            "displayLabel": "Version of Data Lake Studio",
            "watermarkText": "Please provide the version of data lake studio being used",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 500,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details about the issue",
            "watermarkText": "Please provide the details including the full error message obtained while installing ADL within Visual Studio",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
