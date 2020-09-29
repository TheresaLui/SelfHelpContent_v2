<properties
	articleId="92e180e0-645e-4b37-8a7e-354558aeb1fe"
	pageTitle="Scoping Questions for DDoS protection Under attack issue"
	description="Scoping Questions for DDoS protection Under attack Issue"
	authors="genlin"
	ms.author="mariliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32614219"
	productPesIds="16355"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="CloudNet_AzureDDoSProtection"
/>
# DDOS Protection\\Under attack
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Configure DDoS protection standard",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "ip_under_attack",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "What public IP address is under attack?",
            "watermarkText": "",
            "required": false
        },
        {
            "id": "check_if_has_waf",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Do you have an Application Gateway WAF associated with this public IP or subscription?",
            "watermarkText": "",
            "infoBalloonText": "Click <a href='https://docs.microsoft.com/azure/application-gateway/overview#web-application-firewall'>here</a> to see more information about Application Gateway WAF.",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "dont_know_answer",
                    "text": "No"
                }
            ],
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---