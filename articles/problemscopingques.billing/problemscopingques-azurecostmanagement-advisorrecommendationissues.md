<properties
	pageTitle="Azure Cost Management"
	description="Azure Cost Management"
	articleId="advisorrecommendationissues-problemscopingquestion"
	ms.author="prdasneo"
	authors="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32615280,32615298"
	productPesIds="15659"
	cloudEnvironments="public, Mooncake"
	schemaVersion="1"
/>

# Azure Cost Management
---
{
	"resourceRequired": false,
	 "subscriptionRequired": true,
	"title": "Azure Cost Management",
	"fileAttachmentHint": "Please attach the HAR file and the screenshot of the error message",
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
      "order": 2,
      "controlType": "dropdown",
      "displayLabel": "Select the Subscription ID",
      "watermarkText": "Choose an option",
      "dynamicDropdownOptions": {
        "uri": "/subscriptions?api-version=2014-04-01",
        "jTokenPath": "value",
        "textProperty": "displayName,subscriptionId",
        "textTemplate": "{displayName} ({subscriptionId})",
        "valueProperty": "id",
        "textPropertyRegex": "[^\/]+$",
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
      "order": 3,
      "visibility": "SubscriptionId == dont_know_answer",
      "controlType": "textbox",
      "displayLabel": "Subscription ID",
      "watermarkText": "Provide your Subscription id",
      "required": true
    },
     {
      "id": "emailid",
      "order": 4,
      "controlType": "textbox",
      "displayLabel": "Email ID accessing the Subscription",
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
      "id": "additionaldetails",
      "order": 7,
      "controlType": "multilinetextbox",
      "displayLabel": "Additional details or Error Message (if applicable)",
      "watermarkText": "Provide any error message or additional information about your issue",
      "required": false
    },
    {
      "id": "problem_description",
      "order": 8,
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
  ]
}
---
