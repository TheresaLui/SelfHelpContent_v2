<properties
	pageTitle="Partner Center MPN invoice issues"
	description="Partner Center MPN invoice issues"
	authors="dimanjar" 
	ms.author="dimanjar"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32635680"
	productPesIds="15960"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="scopingquestion_partnercenter_mpn_invoice_issues"
	clientIds="partnercenter"
	ownershipId="PartnerCenter_Accounts_Onboarding_Access"
/>
#Partner Center MPN invoice issues
---
{
  "resourceRequired": true,
  "subscriptionRequired": true,
  "title": "MPN invoice issue",
  "fileAttachmentHint": "",
  "formElements": [
    {
      "id": "mpn_invoice_issue_type",
      "order": 1,
      "controlType": "dropdown",
      "displayLabel": "Please select issue type?",
      "watermarkText": "Issue type",
      "dropdownOptions": [
        {
          "value": "Missing invoice",
          "text": "Missing invoice"
        },
        {
          "value": "Unable to download invoice",
          "text": "Unable to download invoice"
        },
         {
          "value": "Invoice format issue",
          "text": "Invoice format issue"
        },
         {
          "value": "Change billing information",
          "text": "Change billing information"
        },
        {
          "value": "VAT ID update",
          "text": "VAT ID update"
        },
        {
          "value": "dont_know_answer",
          "text": "Other"
        }
      ],
      "required": true
    },
    {
      "id": "mpn_order_id",
      "order": 2,
      "controlType": "textbox",
      "displayLabel": "Please enter the order ID you are having issue with",
      "watermarkText": "Order ID",
      "required": false
    },
   {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Please provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "problem_start_time",
            "order": 4,
            "controltype": "datetimepicker",
            "displayLabel": "When did this issue start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
