<properties
	pageTitle="Add Edit VAT TAX ID or PO Number"
	description="Add Edit VAT TAX ID or PO Number"
	articleId="addeditvattaxidorponumber-problemscopingquestions"
	ms.author="prdasneo"
	authors="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32632927"
	productPesIds="15659"
	cloudEnvironments="public, Mooncake, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="ASMS_Billing"
/>
#  Add Edit VAT TAX ID or PO Number
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Add Edit VAT TAX ID or PO Number",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "visibility": null,
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "Problem Start Date",
	    "required": true
        },
	{
	 "id": "taxexempt_details",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Requesting tax exempt?",
            "watermarkText": "Requesting tax exempt?",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
		{
                    "value": "dont_know_answer",
                    "text": "Other"
		 }
		],
		"required": true
		},
	{
            "id": "taxid_details1",
            "order": 2,
	    "visibility": "taxexempt_details == No",
            "controlType": "textbox",
            "displayLabel": "VAT, TAX ID or PO Number",
            "watermarkText": "Provide your VAT, TAX ID or PO Number",
            "required": false
        },
	{
            "id": "taxexempt_details2",
            "order": 5,
            "visibility": "taxexempt_details == Yes",
            "controlType": "textbox",
            "displayLabel": " Provide the Country",
            "required": true
        },
	{
            "id": "taxexempt_details3",
            "order": 6,
            "visibility": "taxexempt_details == Yes",
            "controlType": "multilinetextbox",
            "displayLabel": "Seller (MS) Name/Address",
            "required": true
        },
	{
            "id": "taxexempt_details4",
            "order": 7,
            "visibility": "taxexempt_details == Yes",
            "controlType": "textbox",
            "displayLabel": "Customer (Tax Payer) Full Legal Name",
            "required": true
        },
	{
            "id": "taxexempt_details5",
            "order": 8,
            "visibility": "taxexempt_details == Yes",
            "controlType": "textbox",
            "displayLabel": "Signature and/or effective date of exemption",
            "required": false
        },
	{
            "id": "taxexempt_details6",
            "order": 9,
            "visibility": "taxexempt_details == Yes",
            "controlType": "multilinetextbox",
            "displayLabel": "State(s) the certificate is applicable to",
            "required": false
        },
	{
            "id": "taxexempt_details7",
            "order": 10,
            "visibility": "taxexempt_details == Yes",
            "controlType": "textbox",
            "displayLabel": "Customer (Tax Payer) Number",
            "required": false
        },
	{
            "id": "taxexempt_details8",
            "order": 11,
            "visibility": "taxexempt_details == Yes",
            "controlType": "textbox",
            "displayLabel": "Reason for exemption",
            "required": false
        },
	{
            "id": "taxexempt_details9",
            "order": 12,
            "visibility": "taxexempt_details == Yes",
            "controlType": "textbox",
            "displayLabel": "Type of Property/Service being purchased",
            "required": false
        },
	{
            "id": "taxexempt_details10",
            "order": 13,
            "visibility": "taxexempt_details == Yes",
            "controlType": "multilinetextbox",
            "displayLabel": "If certificate is applicable for all current and future transactions or just the current transaction",
            "required": false
	   },
	   {
            "id": "taxexempt_details11",
            "order": 14,
            "visibility": "taxexempt_details == Yes",
            "controlType": "textbox",
            "displayLabel": "Signature",
            "required": false
        },
	{
            "id": "taxexempt_details12",
            "order": 15,
            "visibility": "taxexempt_details == Yes",
            "controlType": "textbox",
            "displayLabel": "Title",
            "required": false
        },
	{
            "id": "taxexempt_details13",
            "order": 16,
            "visibility": "taxexempt_details == Yes",
            "controlType": "textbox",
            "displayLabel": "Printed name of the signature",
            "required": false
        },
	{
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Please provide details about your issue",
            "required": true,
            "hints": [
                {
                    "text": "Describe your problem, providing as much detail as possible."
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
