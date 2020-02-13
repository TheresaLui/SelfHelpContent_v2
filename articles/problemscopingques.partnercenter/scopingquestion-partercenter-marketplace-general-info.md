<properties
       pageTitle="Marketplace general information"
       description="Marketplace general information"
       authors="brentserbus"
       ms.author="brserbus"
       selfHelpType="problemScopingQuestions"
       supportTopicIds="32728223,32728079"
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
            "required": true
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
