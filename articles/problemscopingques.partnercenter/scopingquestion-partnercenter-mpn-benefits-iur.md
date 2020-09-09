<properties
	pageTitle="Partner Center MPN benefits IUR Requests"
	description="Partner Center MPN benefits IUR Requests"
	authors="dimanjar" 
        ms.author="dimanjar"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32725801,32725871,32725861,32725862"
	productPesIds="17000,17007"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="scopingquestion_partnercenter_MPN_benefits_IUR_requests"
	clientIds="partnercenter"
	ownershipId="PartnerCenter_Accounts_Onboarding_Access"
/>
# Partner Center MPN benefits IUR requests
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "MPN benefits IUR issue",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "mpn_benefit_program",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "What offer or program are you having issue with?",
            "watermarkText": "Select offer/program type",
            "dropdownOptions": [
                {
                    "value": "MAPS",
                    "text": "MAPS"
                },
                {
                    "value": "Silver",
                    "text": "Silver"
                },
                {
                    "value": "Gold",
                    "text": "Gold"
                },
                {
                    "value": "Azure expert MSP",
                    "text": "Azure expert MSP"
                },
                {
                    "value": "Other",
                    "text": "Other"
                }
            ],
            "required": false
        },
        {
            "id": "mpn_benefit_type",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What type of benefit are you having problem with?",
            "watermarkText": "Select benefit type",
            "dropdownOptions": [
                {
                    "value": "Azure and Cloud products",
                    "text": "Azure and Cloud products"
                },
                {
                    "value": "Software products",
                    "text": "Software products"
                },
                {
                    "value": "Visual studio subscriptions",
                    "text": "Visual studio subscriptions"
                },
                {
                    "value": "Technical benefits",
                    "text": "Technical benefits"
                },
                {
                    "value": "Go to Market",
                    "text": "Go to Market"
                }
            ],
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
            "controltype": "datetimepicker",
            "displayLabel": "When did this issue start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
