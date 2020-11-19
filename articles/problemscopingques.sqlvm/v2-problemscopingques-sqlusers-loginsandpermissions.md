<properties 
  pageTitle="SQL Users, Logins and Permissions"
  description="SQL Users, Logins and Permissions"
  authors="ujpat,amamun"
  ms.author="ujpat,amamun"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32740101"
  productPesIds="14745,16342"
  cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
  schemaVersion="1"
  articleId="1ac973b5-a3b8-46f6-8079-090c33972d18"
  ownershipId="AzureData_AzureSQLVM"
/>
# SQL Users, Logins and Permissions 
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "SQL Users, Logins and Permissions",
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
            "id": "WhatArea",
            "visibility": null,
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What area do you need help with?",
            "watermarkText": "Choose an option",
            "content": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Migrating and Creating logins, users, schema or roles",
                    "value": "MigrateCreate"
                },
                {
                    "text": "Permissions and Security",
                    "value": "PermissionsSecurity"
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
             "id": "WhyFails",
             "visibility": "WhatArea == PermissionsSecurity",
             "order": 3,
             "controlType": "dropdown",
             "displayLabel": "What issue do you face with permissions or security?",
             "watermarkText": "Choose an option",
             "content": null,
             "infoBalloonText": null,
             "dropdownOptions": [
                 {
                     "text": "Authentication",
                     "value": "Authentication"
                 },
                 {
                     "text": "Authorization",
                     "value": "Authorization"
                 },
                 {
                     "text": "Other or Need guidance on same",
                     "value": "dont_know_answer_other"
                 }
             ],
             "dynamicDropdownOptions": null,
             "required": false,
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
