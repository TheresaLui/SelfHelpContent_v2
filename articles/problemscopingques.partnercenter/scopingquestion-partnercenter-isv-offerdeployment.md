<properties
	pageTitle="Partner Center Isv Offer Deployment Issue"
	description="Partner Center Isv Offer Deployment Issue"
	authors="harshab"
	ms.author="harshab"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32635659"
	productPesIds="15960"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="scopingquestion_partnercenter_isv_offerdeployment"
	clientIds="partnercenter"
/>
# Partner Center Isv Publishing Issue
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Partner Center Isv Offer Deployment Issue",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "pc_offer_type",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "What is the offer related to this issue?",
            "watermarkText": "Select offer",
            "dropdownOptions": [
                {
                    "value": "Azure Applications",
                    "text": "Azure Applications"
                },
                {
                    "value": "Consulting Services",
                    "text": "Consulting Services"
                },
                {
                    "value": "Container Apps",
                    "text": "Container Apps"
                },
                {
                    "value": "Containers",
                    "text": "Containers"
                },
                {
                    "value": "Core Virtual Machines",
                    "text": "Core Virtual Machines"
                },
                {
                    "value": "D365 Business Central",
                    "text": "D365 Business Central"
                },
                {
                    "value": "D365 for Customer Engagement",
                    "text": "D365 for Customer Engagement"
                },
                {
                    "value": "D365 for Operations",
                    "text": "D365 for Operations"
                },
                {
                    "value": "IoT Edge",
                    "text": "IoT Edge"
                },
                {
                    "value": "Managed Services",
                    "text": "Managed Services"
                },
                {
                    "value": "PowerBI Apps",
                    "text": "PowerBI Apps"
                },
                {
                    "value": "SaaS apps",
                    "text": "SaaS apps"
                },
                {
                    "value": "VM",
                    "text": "VM"
                }
            ],
            "required": false
        },
        {
            "id": "pc_customer_id",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Please provide the customer id you have issues deploying to.",
            "watermarkText": "Provide the customer id",
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
