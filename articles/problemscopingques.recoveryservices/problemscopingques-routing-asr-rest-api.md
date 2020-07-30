<properties
    articleId="ac92ca9c-45p2-017a-a5e4-49812c98d489"
    pageTitle="I need help with REST API support"
    description="I need help with REST API support"
    authors="TobyTu"
    ms.author="sideeksh"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32745014"
    productPesIds="16370"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    ownershipId="Compute_SiteRecovery"
/>
# I need help with REST API support
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "I need help with REST API support",
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
              "value": "Site to site",
              "text": "Site to site"
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
            "displayLabel": "Please provide the name of the resource(s) with which you are experiencing the problem.",
            "watermarkText": "Enter the name",
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
