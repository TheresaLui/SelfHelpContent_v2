<properties
	pageTitle="Partner Center Invoice and Billing Issue"
	description="Partner Center Invoice and Billing Issue"
	authors="brentserbus"
	ms.author="brserbus"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32635667,32635679,32635684,32635695,32635696"
	productPesIds="15960"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="scopingquestion_partnercenterinvoices"
	clientIds="partnercenter"
/>
# PC Sample
---
{
    "resourceRequired": true,
	"subscriptionRequired": true,
    "title": "Partner Center Invoice and Billing Issue",
    "fileAttachmentHint": "",
    "formElements": [
        {	"id": "pc_invoice_type",
			"order": 1,
			"controlType": "dropdown",
			"displayLabel": "What kind of invoice is your issue about?",
			"watermarkText": "Select invoice type",
			"dropdownOptions": [{
						"value": "Recurring",
						"text": "Recurring"
					}, {
						"value": "One-time",
						"text": "One-time"
					}
				],
				"required": false
		},
		{
            "id": "pc_invoice_id",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Please provide the invoice id you have issues with.",
            "watermarkText": "Provide the invoice id",
            "required": false
        },
        {	"id": "pc_recon_type",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "What kind of recon file is your issue about?",
			"watermarkText": "Select recon file type",
			"dropdownOptions": [{
						"value": "Recurring license-based",
						"text": "Recurring license-based"
					}, {
						"value": "Recurring usage-based",
						"text": "Recurring usage-based"
					}, {
						"value": "One-time purchases",
						"text": "One-time purchases"
					}

				],
				"required": false
		},
		{
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Please describe your issue",
            "required": true
        },
		{
			"id": "problem_start_time",
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "When did your issue begin",
            "required": true
		}
    ]
}