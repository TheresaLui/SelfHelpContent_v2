<properties
	pageTitle="Azure Cost Management"
	description="Azure Cost Management"
	articleId="azureusagedetailsapiissues-problemscopingquestion"
	ms.author="prdasneo"
	authors="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32615297"
	productPesIds="15659"
	cloudEnvironments="public, Mooncake, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="ASMS_Billing"
/>

# Azure Cost Management
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Azure Cost Management",
    "fileAttachmentHint": "Please upload the HAR file or a file that may help diagnose the issue",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "Problem Start Date",
            "required": true
        },
        {
            "id": "subscriptionid_details",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Subscription ID",
            "watermarkText": "Provide your Subscription id",
            "required": true
        },
        {
            "id": "browser_details1",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Browser Information",
            "watermarkText": "Choose the browser",
            "dropdownOptions": [
                {
                    "value": "Apple Safari",
                    "text": "Apple Safari"
                },
                {
                    "value": "Google Chrome",
                    "text": "Google Chrome"
                },
                {
                    "value": "Internet Explorer",
                    "text": "Internet Explorer"
                },
                {
                    "value": "Microsoft Edge",
                    "text": "Microsoft Edge"
                },
                {
                    "value": "Mozilla Firefox",
                    "text": "Mozilla Firefox"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other"
                }
            ],
            "required": true
        },
        {
            "id": "browser_details2",
            "order": 5,
            "visibility": "browser_details1 == dont_know_answer",
            "controlType": "textbox",
            "displayLabel": "Please provide the Browser Information",
            "required": true
        },
        {
            "id": "additionaldetails",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details or Error Message (if applicable)",
            "watermarkText": "Provide any error message or additional information about your issue",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 7,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": " Browser network trace (HAR file)",
            "required": true,
            "hints": [
                {
                    "text": "Learn more - <a href='https://blogs.msdn.microsoft.com/benjaminperkins/2016/10/18/capture-a-trace-for-troubleshooting-azure-portal-issues/'>how to capture a browser network trace</a>"
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
