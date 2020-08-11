<properties
    articleId="ac92ca9c-27p2-017a-a5e4-49812c98d489"
    pageTitle="I need help with vCenter"
    description="I need help with vCenter"
    authors="TobyTu"
    ms.author="sideeksh"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32745020"
    productPesIds="16370"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    ownershipId="Compute_SiteRecovery"
/>
# I need help with vCenter
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "I need help with vCenter",
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
            "id": "version",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "What is the version of vCenter?",
            "watermarkText": "Enter the version of vCenter",
            "required": false
        },
        {
            "id": "error_id",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Please provide the error ID associated with vCenter as seen on the Azure portal.",
            "watermarkText": "Enter the error ID",
            "required": false
        },
        {
            "id": "action",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Please choose the action you are having trouble with.",
            "watermarkText": "Choose an option",
            "required": true,
            "dropdownOptions": [
              {
              "value": "Upgrade my existing vCenter to the latest version",
              "text": "Upgrade my existing vCenter to the latest version"
              },
              {
              "value": "My existing vCenter is not connected",
              "text": "My existing vCenter is not connected"
              },
              {
              "value": "Add a new vCenter to the same vault",
              "text": "Add a new vCenter to the same vault"
              },
              {
              "value": "Move a few VMs to a new vCenter",
              "text": "Move a few VMs to a new vCenter"
              },
              {
              "value": "Unable to see VMs under the existing vCenter",
              "text": "Unable to see VMs under the existing vCenter"
              },
              {
              "value": "dont_know_answer",
              "text": "Other, don't know or not applicable"
              }
           ]
        },
        {
            "id": "reference",
            "order": 5,
            "controlType": "multiselectdropdown",
            "displayLabel": "I have gone through the steps mentioned in the following articles:",
            "required": false,
            "dropdownOptions": [
              {
              "value": "ASR manage VMware vCenter server",
              "text": "ASR manage VMware vCenter server"
              },
              {
              "value": "Prepare on-premises VMware servers",
              "text": "Prepare on-premises VMware servers"
              },
              {
              "value": "Common questions about VMware to Azure replication",
              "text": "Common questions about VMware to Azure replication"
              },
              {
              "value": "Troubleshoot vCenter discovery failures",
              "text": "Troubleshoot vCenter discovery failures"
              },
              {
              "value": "dont_know_answer",
              "text": "Other, don't know or not applicable"
              }
           ]
        },
        {
            "id": "problem_description",
            "order": 6,
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
