<properties
	pageTitle="Partner Center MPN cancel or refund"
	description="How to request cancel or refund"
	authors="A-COFLOR"
	ms.author="A-COFLOR"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32739515"
	productPesIds="17003"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="scopingquestion_partnercenter_cancel_refund"
	clientIds="partnercenter"
	ownershipId="PartnerCenter_Billing_and_Invoicing"
/>
# MPN cancel or refund
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "MPN refund issues",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "value_refund",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Specific value of the refund in question",
            "watermarkText": "Value of the refund",
            "required": false
        },
        {
            "id": "currency_type",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Please provide the currency",
            "watermarkText": "Currency",
            "required": false
        },
        {
            "id": "vat_number",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Please provide VAT number",
            "watermarkText": "VAT Number",
            "required": false
        },
        {
            "id": "reason_refund",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Please provide the reason for refund",
            "watermarkText": "Reason for refund",
            "required": false
        },
        {
            "id": "mailing_address",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "Please provide Partner mailing address",
            "watermarkText": "Complete address, City, ZIP code and Country",
            "required": false
        },
        {
            "id": "order_number",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "Please provide Order Number/MPNID",
            "watermarkText": "Order Number/MPNID",
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
            "id": "transaction_date",
            "order": 8,
            "controlType": "datetimepicker",
            "displayLabel": "Please provide the date of the purchase/transaction",
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 9,
            "controltype": "datetimepicker",
            "displayLabel": "When did this issue start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
