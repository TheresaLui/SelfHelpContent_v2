<properties
	pageTitle="Add or Edit VAT TAX ID or PO Number"
	description="Add or Edit VAT TAX ID or PO Number"
	articleId="addoreditvattaxidorponumber"
	ms.author="prdasneo"
	authors="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32454917"
	productPesIds="15660"
	cloudEnvironments="public"
	schemaVersion="1"
	ownershipId="ASMS_SubscriptionManagement"
/>

# Add or Edit VAT TAX ID or PO Number
---
{
    "resourceRequired": false,
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
            "id": "taxid_details",
            "order": 2,
            "controlType": "textbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "VAT, TAX ID or PO Number",
            "watermarkText": "Provide your VAT, TAX ID or PO Number",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide details about your issue",
            "required": true,
            "useAsAdditionalDetails": true,
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
