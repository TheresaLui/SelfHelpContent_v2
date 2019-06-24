<properties
    pageTitle="Azure Stack pricing and licensing or partner center usage (for CSPs) questions"
    description="Azure Stack pricing and licensing or partner center usage (for CSPs) questions"
    authors="TobyTu"
    ms.author="prchint"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32629236,32629239"
    productPesIds="16226"
    cloudEnvironments="Public"
    schemaVersion="1"
    articleId="b4b6273d-558e-4f2d-4872-36a830ea0098"
/>
# Azure Stack pricing and licensing or partner center usage (for CSPs) questions

---
{
  "subscriptionRequired": true,
  "resourceRequired": false,
  "title": "Azure Stack pricing and licensing or partner center (for CSPs) questions",
  "fileAttachmentHint": "",
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