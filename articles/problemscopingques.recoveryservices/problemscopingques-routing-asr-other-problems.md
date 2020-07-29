<properties
    articleId="ac92ca9c-47p2-017a-a5e4-49812c98d489"
    pageTitle="My problem is not listed above"
    description="My problem is not listed above"
    authors="TobyTu"
    ms.author="sideeksh"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32745024"
    productPesIds="16370"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    ownershipId="Compute_SiteRecovery"
/>
# My problem is not listed above
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "My problem is not listed above",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
        {
            "id": "failover_scenario",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What is the scenario?",
            "watermarkText": "Choose an option",
            "required": true,
            "dropdownOptions": [
              {
              "value": "Azure VMs to Azure",
              "text": "Azure VMs to Azure"
              },
              {
              "value": "VMware VMs to Azure",
              "text": "VMware VMs to Azure"
              },
              {
              "value": "Hyper-V VMs to Azure",
              "text": "Hyper-V VMs to Azure"
              },
              {
              "value": "Physical machines to Azure",
              "text": "Physical machines to Azure"
              },
              {
              "value": "Enterprise to Enterprise",
              "text": "Enterprise to Enterprise"
              },
              {
              "value": "dont_know_answer",
              "text": "Other, don't know or not applicable"
              }
           ]
        },
        {
            "id": "name",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Please provide the name of the VM(s) experiencing the problem.",
            "watermarkText": "Enter the name",
            "required": false
        },
        {
            "id": "job_id",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Please provide the ID of the failed Site Recovery job",
            "watermarkText": "Enter the ID",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Please additional details about the issue.",
            "watermarkText": "Please provide the detailed symptom and any other relevant information.",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
