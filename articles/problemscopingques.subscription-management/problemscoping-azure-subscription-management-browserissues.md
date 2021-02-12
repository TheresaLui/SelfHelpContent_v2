<properties
	pageTitle="Scoping questions for Issue with Azure purchase - browser issues"
	description="Scoping questions for Subscription Management/Issue with Azure purchase/browser issues"
	authors="prdasneo"
	ms.author="prdasneo"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32680692"
	productPesIds="15660"
	cloudEnvironments="public, MoonCake, fairfax, usnat, ussec"
  schemaVersion="1"
  articleId="problemscopingquestion-azurepurchase-browserissues"
	ownershipId="ASMS_SubscriptionManagement"
/>
# Issue with Azure purchase - browser issues
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Browser Issues - Azure Subscriptions",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "Problem Start Date",
            "required": true
        },
        {
            "id": "subscription_details",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Subscription ID",
            "watermarkText": "",
            "required": true
        },
        {
            "id": "browser_details1",
            "order": 3,
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
            "order": 4,
            "visibility": "browser_details1 == Other",
            "controlType": "textbox",
            "displayLabel": "Please provide the Browser Information",
            "required": false
        },
        {
            "id": "error_details",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Error Message (if any)",
            "watermarkText": "",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Browser network trace or any other error message (if applicable)",
            "watermarkText": "Provide the browser network trace or any error message or additional information about your issue",
            "required": true,"hints": [
                {
                    "text": "Learn more - <a href='https://blogs.msdn.microsoft.com/benjaminperkins/2016/10/18/capture-a-trace-for-troubleshooting-azure-portal-issues/'>how to capture a browser network trace</a>"
                }
            ]
	    }
    ],
    "$schema": "SelfHelpContent"
}
---
