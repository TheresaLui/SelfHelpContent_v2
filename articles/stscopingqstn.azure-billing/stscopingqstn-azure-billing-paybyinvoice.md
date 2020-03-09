<properties
	pageTitle="Scoping questions for Pay by InvoiceStorage/Development"
	description="Scoping questions for Pay by Invoice"
	authors="prdasneo"
	ms.author="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32454866"
	productPesIds="15659"
	cloudEnvironments="public"
	articleId="410e4d3d-ad20-49ce-8ab3-3d236b520742"
	schemaVersion="1"
	ownershipId="ASMS_Billing"
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
            "required": false
        },
        {
            "id": "billingaddress_details",
            "order": 3,
            "controlType": "textbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Billing Address",
            "watermarkText": "Provide the Billing address",
            "required": false
        },
        {
            "id": "accountadminemail_details",
            "order": 4,
            "controlType": "textbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Account Administrator's Email Address",
            "watermarkText": "Provide the account admin's email address",
            "required": false,
            "infoBalloonText": "Learn more: <a href='https://docs.microsoft.com/azure/billing/billing-add-change-azure-subscription-administrator'> Account Admin's email address</a>."
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Provide any additional information",
            "watermarkText": "Provide any additional information",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
