<properties
	pageTitle="Request for Cancellation of a Subscription"
	description="Request for Cancellation of a Subscription"
	articleId="requestforcancellationofasubscriptionthirdpartypurchase"
	ms.author="prdasneo"
	authors="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32549163,32632954"
	productPesIds="15660"
	cloudEnvironments="public"
	schemaVersion="1"
/>

# Third Party Purchase
---
{
  "resourceRequired": false,
  "title": "Azure Marketplace",
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
      "id": "service_description",
      "order": 2,
      "controlType": "textbox",
      "displayLabel": "Name of the service",
      "watermarkText": "Provide the name of the service:",
      "required": true
    },
    {
      "id": "reason_description",
      "order": 3,
      "controlType": "multilinetextbox",
      "displayLabel": "Reason for cancellation/switching/re-enabling",
      "watermarkText": "Provide the reason for cancellation/switching/re-enabling",
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
          "value": "Other",
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
      "required": true
    },
    {
      "id": "error_description",
      "order": 6,
      "controlType": "multilinetextbox",
      "displayLabel": "Error message encountered (if any)",
      "watermarkText": "Provide the error message encountered",
      "required": true
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
  ]
}
---
