<properties
	articleId="problemscopingques-sqlmi-messaging-dbmail"
	pageTitle="Scoping questions for email server integration and dbmail in SQL Managed Instance"
	description="Scoping questions to email server integration and dbmail in SQL Managed Instance"
	authors="zhizhwan"
	authoralias="zhizhwan"
	ms.author="zhizhwan"
	selfHelpType="problemScopingQuestions"
	productPesIds="16259"
	supportTopicIds="32637260"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_AzureSQLMI"
/>
# SQL Database Managed Instance
---
{
  "$schema": "SelfHelpContent",
  "resourceRequired": true,
  "subscriptionRequired": true,
  "title": "Email server integration and dbmail errors or questions",
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
      "id": "smtp_configuration",
      "order": 2,
      "controlType": "dropdown",
      "displayLabel": "Where is your SMTP server located?",
      "watermarkText": "Choose an option",
      "dropdownOptions": [
        {
          "value": "On-premise network",
          "text": "SMTP server is located in your own on-premise network "
        },
        {
          "value": "public network",
          "text": "SMTP server is located in public network"
        },
        {
          "value": "Azure cloud",
          "text": "SMTP server is located in Microsoft Azure"
        },
        {
          "value": "Other public cloud",
          "text": "SMTP server is located in other public cloud"
        },
        {
          "value": "dont_know_answer",
          "text": "Don't know answer"
        }
      ],
      "required": true
    },
    {
      "id": "dns_configuration",
      "order": 4,
      "controlType": "dropdown",
      "displayLabel": "What is your DNS server configuration?",
      "watermarkText": "Choose an option",
      "dropdownOptions": [
        {
          "value": "Azure DNS",
          "text": "You are using Azure DNS for DNS resolution"
        },
        {
          "value": "Custom DNS",
          "text": "You are using custom DNS for DNS resolution"
        },
        {
          "value": "dont_know_answer",
          "text": "Don't know answer"
        }
      ],
      "required": true
    },
    {
      "id": "error_message",
      "order": 5,
      "controlType": "multilinetextbox",
      "displayLabel": "What error message (if any) are you getting?",
      "required": false
    },
    {
      "id": "problem_description",
      "order": 6,
      "controlType": "multilinetextbox",
      "useAsAdditionalDetails": true,
      "displayLabel": "Details of the issue.",
      "watermarkText": "Please provide additional context for the error message you are encountering.",
      "required": true
    }
  ]
}
---