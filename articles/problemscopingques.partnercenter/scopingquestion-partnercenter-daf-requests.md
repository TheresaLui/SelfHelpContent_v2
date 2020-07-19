<properties
	pageTitle="Partner Center DAF Requests"
	description="Partner Center DAF Requests"
	authors="felicefan"
	ms.author="v-felice"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32739481"
	productPesIds="17003"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="scopingquestion_partnercenter_daf_requests"
	clientIds="partnercenter"
	ownershipId="PartnerCenter_Billing_and_Invoicing"
/>
# Partner Center DAF Requests
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Partner Center DAF Requests",
    "fileAttachmentHint": "Please attach a screenshot of the issue or error you are having",
    "formElements": [
        {
            "id": "invoice_number",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Please provide the invoice number",
            "watermarkText": "Invoice Number",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Please provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "Start Time",
            "watermarkText": "When did your issue begin?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
