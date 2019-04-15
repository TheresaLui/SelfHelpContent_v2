<properties
	pageTitle="Partner Center WHT"
	description="Partner Center Withholding tax SR"
	authors="srinivabms"
	ms.author="srinivab"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="326357011"
	productPesIds="15960"
	cloudEnvironments="public"
	clientIds="partnercenter"
	schemaVersion="1"
	articleId="scopingquestion_partnercenter_wht"
/>
# PC WHT Problem Template
---
{
    "title": "Partner Center WHT Issues",
	"subscriptionRequired": false,
    "fileAttachmentHint": "Upload your tax certificate here",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "pc_invoices",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Please enter your invoices",
			"useAsAdditionalDetails": true,
            "watermarkText": "Provide all your invoice ids (comma separated)",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Details of the issue.",
            "watermarkText": "Provide additional information about your issue including error messages.",
            "required": true
        },
        {
            "id": "pc_learn_more_text",
            "order": 4,
            "controlType": "infoblock",
            "content": "<a href='https://support.microsoft.com/en-us/help/4089764/how-to-get-your-invoice-in-partner-center'> Learn more </a>"
        }
    ]
}
---
