<properties
	pageTitle="Scoping questions for Issue with Azure purchase"
	description="Scoping questions for Subscription Management/Issue with Azure purchase"
	authors="prdasneo"
	ms.author="prdasneo"
   selfHelpType="problemScopingQuestions"
   supportTopicIds="32632950,32632948,32632955"
	productPesIds="15660"
	cloudEnvironments="public, MoonCake"
   schemaVersion="1"
   articleId="8297852a-5e4f-41d8-ae24-9e37aaa5714a"
/>
# Issue with Azure purchase
---
{
  "resourceRequired": false,
  "title": "Purchase Issues - Azure Subscriptions",
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
      "id": "phonenumber_details",
      "order": 2,
      "controlType": "textbox",
      "useAsAdditionalDetails": true,
      "displayLabel": "Phone number used during sign-up",
      "watermarkText": "Provide the Phone number used during sign-up",
      "required": true
    },
    {
      "id": "emailid_details",
      "order": 3,
      "controlType": "textbox",
      "useAsAdditionalDetails": true,
      "displayLabel": "Email address used during sign-up",
      "watermarkText": "Provide the Email address used during sign-up",
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
      "visibility": "browser_details1 == Other",
      "controlType": "textbox",
      "displayLabel": "Please provide the Browser Information",
      "required": false
    },
    {
      "id": "problem_description",
      "order": 6,
      "controlType": "multilinetextbox",
      "useAsAdditionalDetails": true,
      "displayLabel": "Browser network trace or any other error message (if applicable)",
      "watermarkText": "Provide the browser network trace or any error message or additional information about your issue",
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
