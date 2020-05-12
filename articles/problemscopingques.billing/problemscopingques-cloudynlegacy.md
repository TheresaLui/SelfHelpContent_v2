<properties
	articleId="Cloudyn-problemscopingquestions"
	pageTitle="Cloudyn Legacy"
	description="Cloudyn Legacy"
	authors="prdasneo"
	ms.author="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32615279,32615288,32615289,32615290,32615291,32615292,32615294,32615295,32615296,32615299,32615300,32615301,32615302,32615303,32615304,32615305"
	productPesIds="15659"
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="ASMS_Billing"
/>
# Cloudyn Legacy
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Cloudyn Legacy",
    "fileAttachmentHint": "Please upload the HAR file and the screenshot of the error message",
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
            "required": false
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
            "id": "additionaldetails",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details or Error Message (if applicable)",
            "watermarkText": "Provide any error message or additional information about your issue",
            "required": true
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
