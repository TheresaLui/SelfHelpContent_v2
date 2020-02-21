<properties
       pageTitle="Marketplace general information"
       description="Marketplace general information"
       authors="brentserbus"
       ms.author="brserbus"
       selfHelpType="problemScopingQuestions"
       supportTopicIds="32728015,32728016,32728029,32728031,32728033,32728035,32728036,32728037,32728039,32728048,32728055,32728075,32728088,32728102,32728115,32728128,32728161,32728168,32728185,32728205,32728219,32728236,32728248,32728262,32728276,32728076,32728186,32728206,32728249,32728277,32728056,32728077,32728089,32728103,32728116,32728129,32728154,32728169,32728187,32728207,32728220,32728237,32728250,32728263,32728278,32728058,32728079,32728091,32728105,32728118,32728131,32728156,32728171,32728189,32728209,32728222,32728239,32728252,32728265,32728280,32728059,32728080,32728092,32728106,32728119,32728132,32728162,32728172,32728190,32728210,32728223,32728240,32728253,32728266,32728281,32728060,32728081,32728093,32728107,32728120,32728133,32728163,32728173,32728191,32728211,32728224,32728241,32728254,32728267,32728282,32728061,32728082,32728094,32728108,32728121,32728134,32728157,32728174,32728192,32728212,32728225,32728242,32728255,32728268,32728283,32728062,32728083,32728095,32728109,32728122,32728135,32728164,32728175,32728193,32728213,32728226,32728243,32728256,32728269,32728284"
       productPesIds="17006"
       cloudEnvironments="public"
       schemaVersion="1"
       articleId="problemscopingques_partnercenter_marketplace_general" 
       clientIds="partnercenter"
/>
# PC Sample
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Marketplace general information",
    "fileAttachmentHint": "Upload any supporting files that can help us understand your issue.",
    "formElements": [
        {
            "id": "pc_isv_offer_type",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Offer type:",
            "dropdownOptions": [
                {
                    "value": "Azure Application offer",
                    "text": "Azure Application offer"
                },
                {
                    "value": "Consulting Service offer",
                    "text": "Consulting Service offer"
                },
                {
                    "value": "Container offer",
                    "text": "Container offer"
                },
                {
                    "value": "Dynamics 365 Business Central offer",
                    "text": "Dynamics 365 Business Central offer"
                },
                {
                    "value": "Dynamics 365 for Customer Engagement offer",
                    "text": "Dynamics 365 for Customer Engagement offer"
                },
                {
                    "value": "Dynamics 365 for Operations offer",
                    "text": "Dynamics 365 for Operations offer"
                },
                {
                    "value": "IoT Edge Offer",
                    "text": "IoT Edge Offer"
                },
                {
                    "value": "Managed service offer",
                    "text": "Managed service offer"
                },
                {
                    "value": "Office add-in",
                    "text": "Office add-in"
                },
                {
                    "value": "Power BI visual",
                    "text": "Power BI visual"
                },
                {
                    "value": "PowerBI app offer",
                    "text": "PowerBI app offer"
                },
                {
                    "value": "SaaS offer",
                    "text": "SaaS offer"
                },
                {
                    "value": "SharePoint add",
                    "text": "SharePoint add"
                },
                {
                    "value": "Teams app product",
                    "text": "Teams app product"
                },
                {
                    "value": "Virtual machine offer",
                    "text": "Virtual machine offer"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Not sure"
                }
                ],
            "required": true
        },

        {
            "id": "pc_isv_publisher_name",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Please provide the publisher name.",
            "watermarkText": "Please provide the publisher name.",
            "required": false
        },
        {
            "id": "pc_isv_publisher_id",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Please provide the publisher ID.",
            "watermarkText": "Provide the publisher ID as a GUID",
            "required": false
        },
        {
            "id": "pc_isv_seller_id",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Please provide the seller ID.",
            "watermarkText": "Provide the seller ID as a GUID",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Please provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "problem_start_time",
            "order": 6,
            "controlType": "datetimepicker",
            "displayLabel": "Start Time",
            "watermarkText": "When did your issue begin?",
            "required": true
        }
    ]
}
---
