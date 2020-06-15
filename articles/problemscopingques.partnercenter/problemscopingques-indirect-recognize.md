<properties
	pageTitle="Partner Center Indirect Reseller Recognition"
	description="Partner Center Indirect Reseller Recognition"
	authors="brentserbus"
	ms.author="brserbus"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32730251"
	productPesIds="17012"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="sproblemscopingques_indirect_recognize"
	clientIds="partnercenter"
	ownershipId="PartnerCenter_Transact_and_Manage"
/>
# Partner Center Indirect Reseller Recognition
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Partner Center Indirect Reseller Recognition",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "pc_subscription_id",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Please provide the subscription id you want credit for.",
            "watermarkText": "Provide the subscription as a GUID",
            "required": false
        },
        {
            "id": "pc_customertenant_id",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Please provide the customer tenant id you want credit for.",
            "watermarkText": "Provide the customer tenant id as a GUID",
            "required": false
        },
        {
            "id": "mpn_benefit_type",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Did your indirect provider associate your MPN ID to the subscription(s)?",
            "watermarkText": "Did your indirect provider associate your MPN ID to the subscription(s)?",
            "dropdownOptions": [
                {
                    "value": "Yes, my provider associated my MPN ID with the subscription",
                    "text": "Yes, my provider associated my MPN ID with the subscription"
                },
                {
                    "value": "No, my provider did not associate my MPN ID with the subscription",
                    "text": "No, my provider did not associate my MPN ID with the subscription"
                },
                {
                    "value": "I'm not sure if my indirect provider associated my MPN ID with the subscription",
                    "text": "I'm not sure if my indirect provider associated my MPN ID with the subscription"
                }
            ],
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
    ],
    "$schema": "SelfHelpContent"
}
---
