<properties
	pageTitle="Partner Center MPN Order ID"
	description="Partner Center MPN Order ID"
	authors="dimanjar" 
        ms.author="dimanjar"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32725823"
	productPesIds="17003"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="scopingquestion_partnercenter_MPN_order_id"
	clientIds="partnercenter"
	ownershipId="PartnerCenter_Billing_and_Invoicing"
/>
# Partner Center MPN Order ID
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "MPN order ID",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "mpn_order_id",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Please enter Order ID you are having issue with",
            "watermarkText": "Order ID",
            "required": false
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
            "controltype": "datetimepicker",
            "displayLabel": "When did this issue start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
