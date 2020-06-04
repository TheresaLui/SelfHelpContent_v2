<properties
	pageTitle="Issues Signing In or Accessing My Subscriptions"
	description="Issues Signing In or Accessing My Subscriptions"
	articleId="issuessigninginoraccessingsubscriptions-problemscopingquestions"
	ms.author="prdasneo"
	authors="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32632953"
	productPesIds="15660"
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="ASMS_SubscriptionManagement"
/>
# Issues Signing In or Accessing My Subscriptions
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Issues Signing In or Accessing My Subscriptions",
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
            "id": "SubscriptionId",
            "order": 9,
            "controlType": "dropdown",
            "displayLabel": "Select the Subscription ID",
            "watermarkText": "Choose an option",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions?api-version=2014-04-01",
                "jTokenPath": "value",
                "textProperty": "displayName,subscriptionId",
                "textTemplate": "{displayName} ({subscriptionId})",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            },
            "dropdownOptions": [
                {
                    "value": "dont_know_answer",
                    "text": "Not in the list"
                }
            ],
            "useAsAdditionalDetails": false,
            "required": true
        },
        {
            "id": "subscriptionid_details",
            "order": 10,
            "visibility": "SubscriptionId == dont_know_answer",
            "controlType": "textbox",
            "displayLabel": "Subscription ID",
            "watermarkText": "Provide your Subscription id",
            "required": true
        },
        {
            "id": "emailid_details",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Email ID signing in/accessing the subscription",
            "watermarkText": "Provide the Email ID signing in/accessing the subscription",
            "required": false
        },
        {
            "id": "login_date",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "Last login date/time",
            "required": false
        },
        {
            "id": "browser_details1",
            "order": 5,
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
            "order": 6,
            "visibility": "browser_details1 == dont_know_answer",
            "controlType": "textbox",
            "displayLabel": "Please provide the Browser Information",
            "required": false
        },
        {
            "id": "error_details",
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "Error message/Screenshot of the error ",
            "watermarkText": "Provide the error message/Screenshot of the error ",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 8,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Browser network trace or any other details (if applicable)",
            "watermarkText": "Provide the browser network trace or any additional information about your issue",
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
