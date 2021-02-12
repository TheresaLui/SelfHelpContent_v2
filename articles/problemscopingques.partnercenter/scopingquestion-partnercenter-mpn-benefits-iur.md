<properties
	pageTitle="Partner Center MPN benefits IUR Requests"
	description="Partner Center MPN benefits IUR Requests"
	authors="dimanjar" 
        ms.author="dimanjar"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32725801,32725861"
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
                    "value": "advanced_spec",
                    "text": "Advanced Specialization"
                },
                {
                    "value": "azure_exp_msp",
                    "text": "Azure Expert MSP"
                },
                {
                    "value": "Gold",
                    "text": "Gold"
                },
                {
                    "value": "Silver",
                    "text": "Silver"
                },
		{
                    "value": "MAPS",
                    "text": "MAPS"
                },
		{
		   "value": "dont_know_answer",
		   "text": "Not sure / Other"
	       }
            ],
            "required": true
        },
        {
            "id": "mpn_benefit_type",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What type of benefit are you having problems with?",
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
                    "value": "Visual Studio subscriptions",
                    "text": "Visual Studio subscriptions"
                },
		{
		   "value": "dont_know_answer",
		   "text": "Not sure / Other"
	       }
            ],
            "required": true
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Please provide additional information about your issue",
	    "infoBalloonText": "To help us better understand your issue and for a faster resolution please upload the PSR (<a href='https://docs.microsoft.com/office/troubleshoot/settings/how-to-use-problem-steps-recorder'>How to take a PSR</a>)",
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
