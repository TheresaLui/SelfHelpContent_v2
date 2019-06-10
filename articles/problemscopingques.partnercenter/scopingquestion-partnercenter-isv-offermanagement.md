<properties
	pageTitle="Partner Center Isv Offer Management Issue"
	description="Partner Center Isv Offer Management Issue"
	authors="harshab"
	ms.author="harshab"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32635669"
	productPesIds="15960"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="scopingquestion_partnercenter_isv_offermanagement"
	clientIds="partnercenter"
/>
# Partner Center Isv Offer Management Issue
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Partner Center Isv Offer Management Issue",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "pc_offer_type",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "What is the program related to this issue?",
            "watermarkText": "Select program",
            "dropdownOptions": [
                {
                    "value": "Global Campaigns",
                    "text": "Global Campaigns"
                },
                {
                    "value": "Channel Developer",
                    "text": "Channel Developer"
                },
                {
                    "value": "Cloud Solution Provider",
                    "text": "Cloud Solution Provider"
                },
                {
                    "value": "Commercial Distributor",
                    "text": "Commercial Distributor"
                },
                {
                    "value": "CSP 2T Disti",
                    "text": "CSP 2T Disti"
                },
                {
                    "value": "CSP 2T Reseller",
                    "text": "CSP 2T Reseller"
                },
                {
                    "value": "Enterprise Incentives",
                    "text": "Enterprise Incentives"
                },
                {
                    "value": "Hosting",
                    "text": "Hosting"
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
