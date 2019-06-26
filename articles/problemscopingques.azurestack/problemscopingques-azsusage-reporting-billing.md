<properties
    pageTitle="Azure Stack usage reporting and billing"
    description="Azure Stack usage reporting and billing"
    authors="TobyTu"
    ms.author="prchint"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32629274"
    productPesIds="16226"
    cloudEnvironments="Public"
    schemaVersion="1"
    articleId="b4b6273d-558e-4f2d-5238-36a830ea0098"
/>
# Azure Stack usage reporting and billing questions

---
{
  "subscriptionRequired": true,
  "resourceRequired": false,
  "title": "Azure Stack usage reporting and billing questions",
  "fileAttachmentHint": "Upload the usage detail files from Azure and the local usage report. Use the following script <a href='https://aka.ms/azurestackusagesummary'>Azure Stack Usage Summary</a>.",
  "formElements": [{
            "id": "subscription_registration",
            "order": 1,
            "visibility": "null",
            "controlType": "textbox",
            "displayLabel": "What is the Azure Subscription used for registration?",
            "watermarkText": "Navigate to Azure Stack Region management, then click Properties",
            "infoBalloonText": "Navigate to Azure Stack Region management, then click Properties",
            "required": false
		}, {
            "id": "alert_name",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What is your billing model?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Capacity",
                    "text": "Capacity"
                },
                {
                    "value": "Pay-as-you-use",
                    "text": "Pay-as-you-use"
                }
        ],
            "required": false
        }, {
			"id": "problem_start_time",
			"order": 3,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
		}, {
			"id": "problem_description",
			"order": 4,
			"controlType": "multilinetextbox",
			"displayLabel": "Details",
			"watermarkText": "Provide additional information about your issue",
			"required": true,
			"useAsAdditionalDetails": true,
			"hints": []
		}
	],
  "$schema": "SelfHelpContent"
}
---