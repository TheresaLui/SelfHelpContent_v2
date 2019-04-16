<properties
	pageTitle="Partner Center Credit Requests"
	description="Partner Center Credit Requests"
	authors="brentserbus"
	ms.author="brserbus"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32635662,32635698,32635699"
	productPesIds="15960"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="problemscopingques-partnercentercreditrequests"
	clientIds="partnercenter"
/>
# PC Sample
---
{
    "resourceRequired": true,
	"subscriptionRequired": true,
    "title": "Partner Center Credit Requests",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "pc_subscription_id",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Please provide the subscription id you are request credit for.",
            "watermarkText": "Provide the subscription as a GUID",
            "required": false
        },
		{
            "id": "pc_order_id",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Please provide the order id you are request credit for.",
            "watermarkText": "Provide the order id",
            "required": false
        },
        {
            "id": "pc_customertenant_id",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Please provide the customer tenant id you are purchasing for.",
            "watermarkText": "Provide the customer tenant id as a GUID",
            "required": false
        },
		{
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
			"watermarkText": "Please provide additional information about your issue",
			"required": true,
			"useAsAdditionalDetails": true
        },
		{
			"id": "problem_start_time",
            "order": 5,
            "controlType": "datetimepicker",
			"displayLabel": "Start Time",
            "watermarkText": "When did your issue begin?",
            "required": true
		}
    ]
}
---