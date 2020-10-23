<properties
    articleId="ac92ca9c-41p2-017a-a5e4-49812c98d489"
    pageTitle="I need help with SLAs for RTO, RPO, failover, etc."
    description="I need help with SLAs for RTO, RPO, failover, etc."
    authors="TobyTu"
    ms.author="sideeksh"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32745018"
    productPesIds="16370"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    ownershipId="Compute_SiteRecovery"
/>
# I need help with SLAs for RTO, RPO, failover, etc.
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "I need help with SLAs for RTO, RPO, failover, etc.",
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
            "controlType": "dropdown",
            "displayLabel": "Please confirm you have gone through the steps mentioned in the following articles:",
            "required": false,
            "dropdownOptions": [
              {
              "value": "SLA for Azure Site Recovery",
              "text": "SLA for Azure Site Recovery"
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
