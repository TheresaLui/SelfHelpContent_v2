<properties
	articleId=""
	pageTitle="Scoping Questions for ADLA Portal and client tool issues"
	description="Scoping Questions for ADLA Portal and client tool issues"
	authors="guyhay, lisaliu, v-anukar"
	ms.author="guyhay, lisaliu, v-anukar"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32680653"
	productPesIds="15940"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# ADLA Portal and client tooling issues
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "ADLA Portal and client tooling issues with using ADL powershell",
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
            "required": true
        },
        {
            "id": "problem_description",
            "order": 500,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details about the issue",
            "watermarkText": "Please provide the details including the full error message obtained while executing the PS command along with PS commands",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
