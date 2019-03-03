<properties
	pageTitle="Switch to Another Offer"
	description="Switch to Another Offer"
	authors="prdasneo"
	ms.author="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32454938"
	productPesIds="15660"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="switchtoanotheroffer"
/>


# Switch to Another Offer
---
{
  "resourceRequired": false,
  "title": " Activation Extension Request",
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
      "id": "subscriptionid_details",
      "order": 2,
      "controlType": "textbox",
      "displayLabel": "Subscription ID",
      "watermarkText": "Provide the Subscription ID",
      "required": true
    },
    {
      "id": "requesttype_details",
      "order": 3,
      "controlType": "dropdown",
      "displayLabel": "Select the Request type",
      "watermarkText": "Select the type of request",
      "dropdownOptions": [
        {
          "value": "Activation Request",
          "text": "Activation Request"
        },
        {
          "value": "Extension Request",
          "text": "Extension Request"
        }
      ],
      "required": true
    },
    {
      "id": "requesttype_details1",
      "order": 4,
      "visibility": "requesttype_details == Activation Request",
      "controlType": "multilinetextbox",
      "displayLabel": "Error message encountered during activation (if applicable) ",
      "watermarkText": "Provide the error message encountered during activation (if applicable)",
      "required": true
    },
    {
      "id": "requesttype_details2",
      "order": 5,
      "visibility": "requesttype_details == Extension Request",
      "controlType": "textbox",
      "displayLabel": "Please provide the extension period",
      "watermarkText": " Provide the extension period",
      "required": true
    },
    {
      "id": "offertype_details",
      "order": 6,
      "controlType": "dropdown",
      "displayLabel": "Select the Offer type",
      "watermarkText": "Select the type of offer",
      "dropdownOptions": [
        {
          "value": "Action Pack",
          "text": "Action Pack"
        },
        {
          "value": "Enterprise Agreement",
          "text": "Enterprise Agreement"
        },
        {
          "value": "Enterprise Dev/Test",
          "text": "Enterprise Dev/Test"
        },
        {
          "value": "Microsoft Azure Sponsored Offer",
          "text": "Microsoft Azure Sponsored Offer"
        },
        {
          "value": "MSDN Platforms subscribers",
          "text": "MSDN Platforms subscribers"
        },
        {
          "value": "Pay-As-You-Go",
          "text": "Pay-As-You-Go"
        },
        {
          "value": "Pay-As-You-Go Dev/Test",
          "text": "Pay-As-You-Go Dev/Test"
        },
        {
          "value": "Visual Studio Enterprise",
          "text": "Visual Studio Enterprise"
        },
        {
          "value": "Visual Studio Enterprise (BizSpark)",
          "text": "Visual Studio Enterprise (BizSpark)"
        },
        {
          "value": "Visual Studio Enterprise (MPN)",
          "text": "Visual Studio Enterprise (MPN)"
        },
        {
          "value": "Visual Studio Professional",
          "text": "Visual Studio Professional"
        },
        {
          "value": "Visual Studio Test Professional",
          "text": "Visual Studio Test Professional"
        },
        {
          "value": "Other",
          "text": "Other"
        }
      ],
      "required": true
    },
    {
      "id": "offertype_details2",
      "order": 7,
      "visibility": "offertype_details == Other",
      "controlType": "textbox",
      "displayLabel": " Provide the Offer Type",
      "watermarkText": "Provide the Offer Type",
      "required": true
    },
    {
      "id": "problem_description",
      "order": 8,
      "controlType": "multilinetextbox",
      "displayLabel": "Provide a brief description of the issue",
      "watermarkText": "Provide a brief description of the issue",
      "required": true
    }
  ]
}
---
