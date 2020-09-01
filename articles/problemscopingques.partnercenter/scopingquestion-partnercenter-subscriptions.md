<properties
	pageTitle="Partner Center Subscriptions"
	description="Partner Center Subscriptions"
	authors="brentserbus"
	ms.author="brserbus"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32725887,32725895,32725900,32730253,32725881,32725898"
	productPesIds="17012"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="scopingquestion_partnercenter_subscriptions"
	clientIds="partnercenter"
	ownershipId="PartnerCenter_Transact_and_Manage"
/>
# Partner Center Subscriptions
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Partner Center Subscriptions",
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
            "id": "pc_customertenant_id",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Please provide the customer tenant id you are purchasing for.",
            "watermarkText": "Provide the customer tenant id as a GUID",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Please provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "problem_start_time",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "Start Time",
            "watermarkText": "When did your issue begin?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
