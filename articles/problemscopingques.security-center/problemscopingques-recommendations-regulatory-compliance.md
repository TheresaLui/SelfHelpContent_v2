<properties
    pageTitle="Regulatory compliance"
    description="Regulatory compliance"
    authors="TobyTu"
    ms.author="kawilson"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32693246"
    productPesIds="15947"
    cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="b1b6273d-908e-4f2d-ab00-36a830ea0109"
    ownershipId="Azure_Security_Security_Center"
/>
# Regulatory compliance
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Regulatory compliance",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "regulatory_type",
            "order": 1,
            "controlType": "multiselectdropdown",
            "displayLabel": "Please indicate the Regulatory compliance assigned to your subscription:",
            "watermarkText": "Choose one or more options",
            "dropdownOptions": [
                {
                    "value": "PCI DSS 3.2.1",
                    "text": "PCI DSS 3.2.1"
                },
                {
                    "value": "ISO 27001",
                    "text": "ISO 27001"
                },
                {
                    "value": "SOC TSP",
                    "text": "SOC TSP"
                },
                {
                    "value": "Azure CIS 1.1.0",
                    "text": "Azure CIS 1.1.0"
                },
                {
                    "value": "NIST SP 800 53 R4",
                    "text": "NIST SP 800 53 R4"
                },
                {
                    "value": "Azure CIS 1.1.0 (New)",
                    "text": "Azure CIS 1.1.0 (New)"
                },
                {
                    "value": "NIST SP 800 171 R2",
                    "text": "NIST SP 800 171 R2"
                },
                {
                    "value": "UK OFFICIAL and UK NHS",
                    "text": "UK OFFICIAL and UK NHS"
                },
                {
                    "value": "Canada Federal PBMM",
                    "text": "Canada Federal PBMM"
                },
                {
                    "value": "Azure Security Benchmark",
                    "text": "Azure Security Benchmark"
                },
                {
                    "value": "HIPAA HITRUST",
                    "text": "HIPAA HITRUST"
                },
                {
                    "value": "SWIFT CSP CSCF v2020",
                    "text": "SWIFT CSP CSCF v2020"
                },
                {
                    "value": "Custom",
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
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
