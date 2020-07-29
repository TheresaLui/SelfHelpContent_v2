<properties 
  pageTitle="Encryption- TDE, Always Encrypted, AKV"
  description="Encryption- TDE, Always Encrypted, AKV"
  authors="ujpat,amamun"
  ms.author="ujpat,amamun"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32740080"
  productPesIds="14745,16342"
  cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
  schemaVersion="1"
  articleId="c77ad2a8-313d-41c4-b6a6-8cc92170e58a"
  ownershipId="AzureData_AzureSQLVM"
/>
# Encryption- TDE, Always Encrypted, AKV
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Encryption- TDE, Always Encrypted, AKV",
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
                    "text": "TDE",
                    "value": "TDE"
                },
                {
                    "text": "Always Encrypted or Secure enclaves",
                    "value": "AESecureEnclaves"
                },
                {
                    "text": "Azure Key Vault configuration or errors",
                    "value": "AKVErrors"
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
             "id": "How_Ecnrypt",
             "visibility": null,
             "order": 3,
             "controlType": "dropdown",
             "displayLabel": "How are you encrypting data?",
             "watermarkText": "Choose an option",
             "content": null,
             "infoBalloonText": null,
             "dropdownOptions": [
                 {
                     "text": "Using Symmetric Key",
                     "value": "SymmetricKey"
                 },
                 {
                     "text": "Using Asymmetric Key",
                     "value": "AsymmetricKey"
                 },
                 {
                     "text": "Using a Certificate",
                     "value": "UsingCertificate"
                 },
                 {
                     "text": "Encrypting Database files using TDE",
                     "value": "TDEEncryption"
                 },
                 {
                     "text": "Encrypting column",
                     "value": "EncryptingColumn"
                 },
                 {
                     "text": "Other or need guidance",
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
