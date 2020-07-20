<properties
	pageTitle="Partner Center Tax Exempt"
	description="Partner Center Tax Exempt"
	authors="brentserbus"
	ms.author="brserbus"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32725811,32692609"
	productPesIds="17000,17003"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="sproblemscopingques_tax_exempt"
	clientIds="partnercenter"
	ownershipId="PartnerCenter_Accounts_Onboarding_Access"
/>
# Partner Center Tax Exempt
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Partner Center Tax Exempt",
    "fileAttachmentHint": "Please include a recent tax certification as an attachment.",
    "formElements": [
        {
            "id": "added_taxID",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Have you added your tax ID to your partner profile?",
            "watermarkText": "Have you added your tax ID to your partner profile?",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
            ],
            "required": false
        },
        {
            "id": "reason_why_update_not_performed_via_partner_center",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Reason why update not performed via Partner center",
            "watermarkText": "Please provide the reason why update not performed via Partner center",
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
            "displayLabel": "Tax ID updated date",
            "watermarkText": "When did you add your tax ID to your partner profile?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
