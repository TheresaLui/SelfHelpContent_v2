<properties 
  pageTitle="Change Licensing - pay as you go or bring your own"
  description="Change Licensing - pay as you go or bring your own"
  authors="ujpat,amamun"
  ms.author="ujpat,amamun"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32740073"
  productPesIds="14745"
  cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
  schemaVersion="1"
  articleId="6d2c0e8f-ebed-4f8a-ab53-3071bbdc51a6"
  ownershipId="AzureData_AzureSQLVM"
/>
# Change Licensing - pay as you go or bring your own
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Change Licensing - pay as you go or bring your own",
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
            "displayLabel": "How are you attempting to change the license type?",
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
            "required": false
        },
        {
            "id": "error",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Did you encounter any error while applying the change?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "text": "Yes (describe below)",
                    "value": "Yes"
                },
                {
                    "text": "No",
                    "value": "dont_know_answer"
                }
            ],
            "required": false
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
