<properties
    articleId="ac92ca9c-38p2-017a-a5e4-49812c98d489"
    pageTitle="I need help with Site Recovery licenses"
    description="I need help with Site Recovery licenses"
    authors="TobyTu"
    ms.author="sideeksh"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32745016"
    productPesIds="16370"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    ownershipId="Compute_SiteRecovery"
/>
# I need help with Site Recovery licenses
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "I need help with Site Recovery licenses",
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
              "value": "Pricing for Azure Site Recovery",
              "text": "Pricing for Azure Site Recovery"
              },
              {
              "value": "Know how much it will cost you for enabling DR on your Azure VMs",
              "text": "Know how much it will cost you for enabling DR on your Azure VMs"
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
