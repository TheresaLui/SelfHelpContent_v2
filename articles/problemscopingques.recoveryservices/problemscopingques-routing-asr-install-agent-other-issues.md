<properties
    articleId="ac92ca9c-32p2-017a-a5e4-49812c98d489"
    pageTitle="I am unable to install the mobility service agent due to other errors"
    description="I am unable to install the mobility service agent due to other errors"
    authors="TobyTu"
    ms.author="sideeksh"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32744986"
    productPesIds="16370"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    ownershipId="Compute_SiteRecovery"
/>
# I am unable to install the mobility service agent due to other errors
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "I am unable to install the mobility service agent due to other errors",
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
              "value": "Protection of Azure virtual machines",
              "text": "Protection of Azure virtual machines"
              },
              {
              "value": "Protection of VMware virtual machines to Azure",
              "text": "Protection of VMware virtual machines to Azure"
              },
              {
              "value": "Protection of Hyper-V virtual machines to Azure",
              "text": "Protection of Hyper-V virtual machines to Azure"
              },
              {
              "value": "Protection of physical servers from on-premises to Azure",
              "text": "Protection of physical servers from on-premises to Azure"
              },
              {
              "value": "Protection of Hyper-V virtual machines from one on-premise site to another on-premise site",
              "text": "Protection of Hyper-V virtual machines from one on-premise site to another on-premise site"
              },
              {
              "value": "dont_know_answer",
              "text": "Other"
              }
           ]
        },
        {
            "id": "name",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Please provide the name of the VM with which you are experiencing the problem.",
            "watermarkText": "Enter the name",
            "required": false
        },
        {
            "id": "job_id",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Please provide the ID of the failed Site Recovery job.",
            "watermarkText": "Enter the ID",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 5,
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
