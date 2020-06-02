<properties
	pageTitle="Request for Cancellation of a Subscription - browser problem"
	description="Request for Cancellation of a Subscription - browser problem"
	articleId="requestforcancellationofasubscriptionbrowserproblems"
	ms.author="prdasneo"
	authors="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32680687"
	productPesIds="15660"
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="ASMS_SubscriptionManagement"
/>

#  Request for Cancellation of a Subscription- browser problem
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Request for Cancellation of a Subscription- browser problem",
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
            "required": false
        },
        {
            "id": "error_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Error message encountered (if any)",
            "watermarkText": "Provide the error message encountered",
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
