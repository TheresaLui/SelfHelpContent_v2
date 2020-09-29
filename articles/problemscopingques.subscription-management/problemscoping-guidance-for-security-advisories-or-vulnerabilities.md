<properties
	pageTitle="Guidance for Security Advisories or Vulnerabilities"
	description="Guidance for Security Advisories or Vulnerabilities"
	articleId="guidanceforsecurityadvisoriesorvulnerabilities-problemscopingquestions"
	ms.author="prdasneo"
	authors="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32611254"
	productPesIds="15660"
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="ASMS_SubscriptionManagement"
/>
# Guidance for Security Advisories or Vulnerabilities
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Guidance for Security Advisories or Vulnerabilities",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "Problem Start Date",
            "required": true
        },
        {
            "id": "subscriptionid_details",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Subscription ID",
            "watermarkText": "Provide the Subscription ID",
            "required": false
        },
        {
            "id": "azureservice_details",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Azure Service impacted",
            "watermarkText": "Provide the Azure Service impacted",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Problem description",
            "watermarkText": "Provide a brief description of your request",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
