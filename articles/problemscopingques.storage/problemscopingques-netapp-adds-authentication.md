<properties
	articleId="adds-authentication-issues"
	pageTitle="Active Directory Domain Services and Authentication Issues"
	description="Active Directory Domain Services and Authentication Issues"
	authors="b-tonya"
	ms.author="b-tonya"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32740752"
	productPesIds="16469"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureNetAppFiles"
/>
# Active Directory Domain Services and Authentication Issues
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": true,
  "resourceRequired": true,
  "title": "Active Directory Domain Services and Authentication Issues",
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
      "id": "AzureADDS",
      "order": 2,
      "controlType": "dropdown",
      "displayLabel": "Are you using Azure ADDS?",
      "dropdownOptions": [
        {
          "value": "Yes",
          "text": "Yes"
        },
        {
          "value": "No",
          "text": "No"
        },
        {
          "value": "dont_know_answer",
          "text": "None of the above"
        }
      ],
      "required": true
    },
    {
      "id": "DNSreachable",
      "order": 3,
      "controlType": "dropdown",
      "displayLabel": "Is your DNS server IP addresses reachable?",
      "watermarkText": "If there’s no issues with the DNS server IP addresses, then verify that no firewalls are blocking the access?",
      "dropdownOptions": [
        {
          "value": "Yes",
          "text": "Yes"
        },
        {
          "value": "No",
          "text": "No"
        },
        {
          "value": "dont_know_answer",
          "text": "None of the above"
        }
      ],
      "required": true
    },
    {
      "id": "error_message",
      "order": 4,
      "controlType": "textbox",
      "displayLabel": "Error message",
      "watermarkText": "What was the error message?",
      "required": false
    },
    {
      "id": "problem_description",
      "order": 5,
      "controlType": "multilinetextbox",
      "displayLabel": "Provide any additional details",
      "required": true,
      "useAsAdditionalDetails": true
    }
  ]
}
---