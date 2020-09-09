<properties 
  pageTitle="SQL image provisioning"
  description="SQL image provisioning"
  authors="ujpat,amamun"
  ms.author="ujpat,amamun"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32740092"
  productPesIds="14745,16342"
  cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
  schemaVersion="1"
  articleId="cc834662-8339-4a88-b567-5dfd828ed480"
  ownershipId="AzureData_AzureSQLVM"
/>
# SQL image provisioning
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "SQL image provisioning",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start",
            "required": false
        },
        {
            "id": "how",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "How are you attempting to provision the image?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "text": "Azure Portal",
                    "value": "Azure Portal"
                },
                {
                    "text": "Azure PowerShell",
                    "value": "Azure PowerShell"
                },
                {
                    "text": "Azure CLI",
                    "value": "Azure CLI"
                },
                {
                    "text": "Other, don't know or not applicable",
                    "value": "dont_know_answer"
                }
            ],
            "required": true
        },
        {
            "id": "error",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "What is the image you are trying to provision?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "text": "I am using the image (describe below) and if tails",
                    "value": "Using_Image"
                },
                {
                    "text": "I am not able to find the image on Azure Portal",
                    "value": "Cannot_Find"
                },
                {
                    "text": "Other, don't know or not applicable",
                    "value": "dont_know_answer"
                }
            ],
            "required": true
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
