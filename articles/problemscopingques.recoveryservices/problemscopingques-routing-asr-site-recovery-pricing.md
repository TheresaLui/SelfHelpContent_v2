<properties
    articleId="ac92ca9c-39p2-017a-a5e4-49812c98d489"
    pageTitle="I need help with Site Recovery pricing"
    description="I need help with Site Recovery pricing"
    authors="TobyTu"
    ms.author="sideeksh"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32745017"
    productPesIds="16370"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    ownershipId="Compute_SiteRecovery"
/>
# I need help with Site Recovery pricing
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "I need help with Site Recovery pricing",
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
            "id": "user_type",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Are you a current user of Site Recovery or a prospective user?",
            "watermarkText": "Choose an option",
            "required": true,
            "dropdownOptions": [
              {
              "value": "Current user",
              "text": "Current user"
              },
              {
              "value": "Prospective user",
              "text": "Prospective user"
              },
              {
              "value": "dont_know_answer",
              "text": "Other, don't know or not applicable"
              }
           ]
        },
        {
            "id": "reference",
            "order": 3,
            "controlType": "multiselectdropdown",
            "displayLabel": "Please confirm you have gone through the steps mentioned in the following articles:",
            "required": false,
            "dropdownOptions": [
              {
              "value": "Software Assurance FAQ",
              "text": "Software Assurance FAQ"
              },
              {
              "value": "Azure Hybrid Benefit FAQ",
              "text": "Azure Hybrid Benefit FAQ"
              },
              {
              "value": "Azure Site Recovery pricing",
              "text": "Azure Site Recovery pricing"
              },
              {
              "value": "Know exactly how much it will cost for enabling DR to your Azure VMs",
              "text": "Know exactly how much it will cost for enabling DR to your Azure VMs"
              },
              {
              "value": "dont_know_answer",
              "text": "Other, don't know or not applicable"
              }
           ]
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
