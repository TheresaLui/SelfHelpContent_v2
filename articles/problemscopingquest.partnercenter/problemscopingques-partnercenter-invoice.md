<properties
	pageTitle="Partner Center Invoice Issues"
	description="Partner Center Invoice"
	authors="srinivabms"
	ms.author="srinivab"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32569834,32633857"
	productPesIds="15960"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="scopingquestion_partnercenter_invoice"
/>
# PC Invoice Problem Template
---
{
	"title": "Partner Center Invoice Issue",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "problem_start_time",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
		},
		{
			"id": "pc_invoice_id",
			"order": 2,
			"controlType": "textbox",
			"displayLabel": "Please enter your invoice id.",
			"watermarkText": "Provide your invoice id",
			"required": true
		},
		{
			"id": "pc_invoice_type",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "Select the Type of invoice",
			"dropdownOptions": [{
				"value": "license",
				"text": "License Based"
			}, {
				"value": "payg",
				"text": "Pay As You Go"
			}, {
				"value": "modern",
				"text": "Modern"
			}],
			"required": false
		},
		{
			"id": "pc_recon_type",
			"order": 4,
			"controlType": "multiselectdropdown",
			"displayLabel": "Select the Type of Recon file",
			"dropdownOptions": [{
				"value": "usagebased",
				"text": "Usage Based"
			}, {
				"value": "licensebased",
				"text": "License Based"
			}, {
				"value": "onetime",
				"text": "One Time"
			}],
			"required": false
		},
		{
			"id": "problem_description",
			"order": 5,
			"controlType": "multilinetextbox",
			"useAsAdditionalDetails": true,
			"displayLabel": "Details of the issue.",
			"watermarkText": "Provide additional information about your issue including error messages.",
			"required": true
		},
		{
			"id": "pc_learn_more_text",
			"order": 6,
			"controlType": "infoblock",
			"content": "<a href='https://support.microsoft.com/en-us/help/4089764/how-to-get-your-invoice-in-partner-center'> Learn more </a>"
		},
		{
			"id": "pc_dynamicdropdown",
			"order" : 7,
			"controlType": "dropdown",
			"displayLabel": "Please select the Customer Name",
			"watermarkText": "Choose an option",
			"dropDownOption": {
				"uri": "https://api.partnercenter.microsoft-ppe.com/v1/customers?size=200",
				"jTokenPath": "items",
				"textProperty": "companyProfile/companyName",
				"valueProperty": "companyProfile/tenantId",
				"textPropertyRegex": "[^/]+$"
			},		
            "dropdownOptions": [
                {
                    "value": "CustomerListNotFound",
                    "text": "No Customers Available"
                }
		}
	]
}
---
