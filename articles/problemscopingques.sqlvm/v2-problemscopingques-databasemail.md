<properties 
  pageTitle="Database Mail"
  description="Database Mail"
  authors="ujpat,amamun"
  ms.author="ujpat,amamun"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32740085"
  productPesIds="14745,16342"
  cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
  schemaVersion="1"
  articleId="3b1c820f-6f9e-427c-a9f3-8db5c6efd27b"
  ownershipId="AzureData_AzureSQLVM"
/>
# Database Mail
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Database Mail",
    "fileAttachmentHint": null,
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start",
            "required": true
        },
        {
            "id": "dbmailwhatissue",
            "visibility": null,
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What are you trying to achieve?",
            "watermarkText": "Choose an option",
            "content": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Need help configuring Database Mail",
                    "value": "configure"
                },
                {
                    "text": "Cannot send mail using Database Mail",
                    "value": "sendemail"
                },
                {
                    "text": "Issue with DB Mail using SendGrid",
                    "value": "sendgrid"
                },
                {
                    "text": "I'm not sure/don't know",
                    "value": "dont_know_answer"
                }
            ],
            "dynamicDropdownOptions": null,
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
