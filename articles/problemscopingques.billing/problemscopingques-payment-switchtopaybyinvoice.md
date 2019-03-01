<properties
	pageTitle="Switch to Pay by Invoice"
	description="Switch to Pay by Invoice"
	articleId="payment-switchtopaybyinvoice-problemscopingquestions"
	ms.author="prdasneo"
	authors="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32454866,32632941"
	productPesIds="15659"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Switch to Pay by Invoice
---
{
  "resourceRequired": false,
  "title": "Switch to Pay by Invoice",
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
      "id": "company_details",
      "order": 2,
      "controlType": "textbox",
      "useAsAdditionalDetails": true,
      "displayLabel": "Company Name",
      "watermarkText": "Provide the Company Name",
      "required": true
    },
    {
      "id": "billingaddress_details",
      "order": 3,
      "controlType": "textbox",
      "useAsAdditionalDetails": true,
      "displayLabel": "Billing Address",
      "watermarkText": "Provide the Billing address",
      "required": true
    },
    {
      "id": "problem_description",
      "order": 4,
      "controlType": "multilinetextbox",
      "useAsAdditionalDetails": true,
      "displayLabel": "Provide any additional information",
      "watermarkText": "Provide any additional information",
      "required": true,
      "hints": [
       {
            "text": "<a href='https://docs.microsoft.com/azure/billing/billing-add-change-azure-subscription-administrator'>Account Administrator's Email Address</a>."
       },
       {
        "text": "Description of your issue"
       }
       ]
    }
  ]
}
---
