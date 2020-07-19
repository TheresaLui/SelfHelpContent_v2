<properties
	pageTitle="Partner Center Overdue invoice or missing payment"
	description="Partner Center Overdue invoice or missing payment"
	authors="a-crmire" 
	ms.author="a-crmire"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32739482"
	productPesIds="17003"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="scopingquestion_partnercenter_overdue_invoice_or_missing_payment"
	clientIds="partnercenter"
	ownershipId="PartnerCenter_Billing_and_Invoicing"
/>
# Partner Center Overdue invoice or missing payment
---
{
  "resourceRequired": true,
  "subscriptionRequired": true,
  "title": "Partner Center Overdue invoice or missing payment",
  "fileAttachmentHint": "",
  "formElements": [
      {
      "id": "payment_amount",
      "order": 1,
      "controlType": "textbox",
      "displayLabel": "Specific value of the payment amount",
      "watermarkText": "Payment amount",
      "required": false
       },
       {
            "id": "payment_currency",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Please provide the Payment Currency",
            "watermarkText": "Payment Currency",
            "required": false
        },
       {
            "id": "bank_account",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Please provide the Microsoft Bank Account number",
            "watermarkText": "Microsoft Bank Account number",
            "required": false
        },
       {
            "id": "date_of_remittance",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "Please provide the Date of Remittance",
            "required": false
        },
       {
            "id": "order_id",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "Please provide the Order ID/MPN ID",
            "watermarkText": "Order ID/MPN ID",
            "required": false
        },
       {
            "id": "payment_reference",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "Please provide the Payment Reference",
            "watermarkText": "Payment Reference",
            "required": false
        },
       {
            "id": "problem_description",
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Please provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        },
       {
            "id": "problem_start_time",
            "order": 8,
            "controltype": "datetimepicker",
            "displayLabel": "When did this issue start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
