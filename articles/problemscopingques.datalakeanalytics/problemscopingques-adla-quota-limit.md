<properties
	articleId="343fcc51-368b-4592-bd99-bf3b6c9d9310"
	pageTitle="Scoping Questions for ADLA Quota and Limits Issue"
	description="Scoping Questions for ADLA Quota and Limits Issue"
	authors="lisaliu"
	ms.author="guyhay, lisaliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32680642"
	productPesIds="15940"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_AzureDataLakeAnalytics"
/>
# ADLA Quota and Limits Issues
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "ADLA Quota and Limits Issue",
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
            "id": "request_type",
            "order": 50,
            "controlType": "dropdown",
            "displayLabel": "What is the request for?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "max_number_accounts",
                    "text": "Increase max number of ADLA accounts"
                },
                {
                    "value": "max_account_limit",
                    "text": "Increase max concurrent job limit or max concurrent AUs per account"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "region",
            "visibility": "request_type == max_number_accounts",
            "order": 110,
            "controlType": "textbox",
            "displayLabel": "Azure Region",
            "watermarkText": "Please provide the Azure Region in which the max number of ADLA accounts is to be increased",
            "required": false
        },
        {
            "id": "new_max_accounts",
            "visibility": "request_type == max_number_accounts",
            "order": 120,
            "controlType": "textbox",
            "displayLabel": "New max number of accounts",
            "watermarkText": "Please provide the new max number of ADLA accounts to be increased to",
            "required": false
        },
        {
            "id": "adla_account_name",
            "visibility": "request_type == max_account_limit",
            "order": 130,
            "controlType": "textbox",
            "displayLabel": "ADLA account name",
            "watermarkText": "Please provide the Azure Data Lake Analytics Account name for which the new account limit is to be adjusted",
            "required": true
        },
        {
            "id": "region2",
            "visibility": "request_type == max_account_limit",
            "order": 140,
            "controlType": "textbox",
            "displayLabel": "Azure Region",
            "watermarkText": "Please provide the Azure Region in which the new ADLA account limit is to be adjusted",
            "required": false
        },
        {
            "id": "new_max_concurrent_jobs",
            "visibility": "request_type == max_account_limit",
            "order": 150,
            "controlType": "textbox",
            "displayLabel": "New max concurrent job limit",
            "watermarkText": "Please provide the new max concurrent job limit for the ADLA account",
            "required": false
        },
        {
            "id": "new_max_concurrent_aus",
            "visibility": "request_type == max_account_limit",
            "order": 160,
            "controlType": "textbox",
            "displayLabel": "New max concurrent AUs",
            "watermarkText": "Please provide the new max concurrent AUs for the ADLA account",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 500,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details about the issue",
            "watermarkText": "Please provide the detail symptom including the full error text if available, the reason behind the request, and any other relevant information",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
