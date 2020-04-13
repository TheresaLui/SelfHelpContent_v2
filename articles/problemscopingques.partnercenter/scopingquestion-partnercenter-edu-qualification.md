<properties
       pageTitle="Customer Education qualification"
       description="Customer Education qualification"
       authors="brentserbus"
       ms.author="brserbus"
       selfHelpType="problemScopingQuestions"
       supportTopicIds="32730249"
       productPesIds="17012"
       cloudEnvironments="public, fairfax, usnat, ussec"
       schemaVersion="1"
       articleId="problemscopingques-partnercentereduqualification"
       clientIds="partnercenter"
       ownershipId="PartnerCenter_Transact_and_Manage"
/>
# PC Sample
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Customer Education qualification",
    "fileAttachmentHint": "Upload any supporting files that can help us understand the issue.",
    "formElements": [
             {
            "id": "pc_customer_name",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Please provide the customer name this issue is about",
            "watermarkText": "Provide the customer name",
            "required": false
             },
             {
            "id": "pc_tenant_id",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Please provide the tenant id of your customer",
            "watermarkText": "Provide the tenant id as a GUID",
            "required": true
             },
	    {
            "id": "pc_customer_address",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Please include the address for your customer",
            "required": false
             },
             {
            "id": "pc_website_url",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Please provide url for your customer's website",
            "watermarkText": "Provide the http:// url of your customer's website",
            "required": false
             },
	     {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Please provide additional information about your issue",
            "useAsAdditionalDetails": true,
            "required": true
             },
             {
            "id": "problem_start_time",
            "order": 6,
            "controlType": "datetimepicker",
            "displayLabel": "When did your issue begin",
            "required": true
             }
    ]
}
---
