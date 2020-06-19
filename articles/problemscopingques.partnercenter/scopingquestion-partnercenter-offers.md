<properties
	pageTitle="Partner Center Offer Issue"
	description="Partner Center Offer Issue"
	authors="brentserbus"
	ms.author="brserbus"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32692600,32692594,32692603,32692606,32692607,32725880,32730254,32692602,32725890"
	productPesIds="17011,17012"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="scopingquestion_partnercenter_offers"
	clientIds="partnercenter"
	ownershipId="PartnerCenter_Pricing_and_Offers"
/>
# Partner Center Offer Issue
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Partner Center Offer Issue",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "pc_offer_id",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Please provide the offer id you are having problems finding.",
            "watermarkText": "Provide the offer id as a GUID",
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
            "id": "pc_offer_search",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "What type of product are you trying to find?",
            "watermarkText": "Select product type",
            "dropdownOptions": [
                {
                    "value": "License-based offers",
                    "text": "License-based offers"
                },
                {
                    "value": "Azure reservations",
                    "text": "Azure reservations"
                },
                {
                    "value": "Software subscriptions",
                    "text": "Software subscriptions"
                },
                {
                    "value": "Marketplace offers",
                    "text": "Marketplace offers"
                }
            ],
            "required": false
        },
        {
            "id": "pc_offer_type",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "What kind of offer is your issue about?",
            "watermarkText": "Select offer type",
            "dropdownOptions": [
                {
                    "value": "Commercial",
                    "text": "Commercial"
                },
                {
                    "value": "Academic",
                    "text": "Academic"
                },
                {
                    "value": "GCC (Government Community Cloud)",
                    "text": "GCC (Government Community Cloud)"
                },
                {
                    "value": "Nonprofit",
                    "text": "Nonprofit"
                }
            ],
            "required": false
        },
	{
            "id": "pc_customer_country",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "Please provide the country of the customer you are trying to sell to.",
            "watermarkText": "Please provide the country of the customer you are trying to sell to",
            "required": false
        },
        {
            "id": "pc_partner_country",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "Please provide your country.",
            "watermarkText": "Please provide your country",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Please provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "problem_start_time",
            "order": 8,
            "controlType": "datetimepicker",
            "displayLabel": "Start Time",
            "watermarkText": "When did your issue begin?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
