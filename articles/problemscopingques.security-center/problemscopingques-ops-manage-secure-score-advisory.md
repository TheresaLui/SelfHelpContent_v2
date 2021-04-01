<properties
	pageTitle="Secure Score advisory"
	description="Secure Score advisory"
	authors="genlin"
	ms.author="kawilson"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32788562"
    productPesIds="15947"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="b1b6273d-0021-4f2d-f021-36a830ea0107"
	schemaVersion="1"
	ownershipId="Azure_Security_Security_Center"
/>
# Secure Score advisory in security center
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Secure Score advisory in security center",
    "fileAttachmentHint": "Please run the following query in the <a href='https://docs.microsoft.com/azure/governance/resource-graph/first-query-portal'>Resource Graph Explorer</a> , and upload the csv file  that may help diagnose the issue: **securityresources|where type == "microsoft.security/securescores"**",
    "formElements": [
        {
            "id": "scope_exempt",
            "order": 1,
            "controlType": "multiselectdropdown",
            "displayLabel": "Select the regulatory compliance that is assigned to your subscription ",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "option_1",
                    "text": "Azure Security Baseline (default)"
                },
                {
                    "value": "option_2",
                    "text": "PCI DSS 3.2.1"
                },
                {
                    "value": "option_3",
                    "text": "ISO 27001:2013"
                },
                {
                    "value": "option_4",
                    "text": "SOC TSP"
                },
                {
                    "value": "option_5",
                    "text": "Azure CIS 1.1.0"
                },
                {
                    "value": "option_6",
                    "text": "NIST SP 800 53 R4"
                },
                {
                    "value": "option_7",
                    "text": "Azure CIS 1.1.0 (New)"
                },
                {
                    "value": "option_8",
                    "text": "NIST SP 800 171 R2
                },
                {
                    "value": "option_9",
                    "text": "UK OFFICIAL and UK NHS"
                },
                {
                    "value": "option_10",
                    "text": "Canada Federal PBMM"
                },
                {
                    "value": "option_11",
                    "text": "Azure Security Benchmark"
                },
                {
                    "value": "option_12",
                    "text": "HIPAA HITRUST"
                },
                {
                    "value": "option_13",
                    "text": "SWIFT CSP CSCF v2020"
                },
                {
                    "value": "option_14",
                    "text": "Custom"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other"
                }
            ],
            "required": true
        },
        {
            "id": "problem_description",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
