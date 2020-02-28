<properties
	pageTitle="Reenable a Subscription"
	description="Reenable a Subscription"
	articleId="reenableasubscription"
	ms.author="prdasneo"
	authors="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32454933"
	productPesIds="15660"
	cloudEnvironments="public"
	schemaVersion="1"
	ownershipId="ASMS_SubscriptionManagement"
/>

# Reenable a Subscription
---
{
    "resourceRequired": false,
    "title": "Azure Subscriptions",
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
            "id": "reason_description",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Reason for cancellation/switching/re-enabling",
            "watermarkText": "Provide the reason for cancellation/switching/re-enabling",
            "required": false
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
                    "value": "Other",
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
            "required": true
        },
        {
            "id": "error_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Error message (if any) encountered ",
            "watermarkText": "Provide the error message encountered",
            "required": false
        },
        {
            "id": "email_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Email notification received (if applicable) about subscription suspension",
            "watermarkText": "Provide the email notification received about subscription suspension",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 7,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Browser network trace/Additional details (if any)",
            "watermarkText": "Provide the browser network trace or any other additional relevant details",
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
