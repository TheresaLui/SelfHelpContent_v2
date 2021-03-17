<properties
  pageTitle="Virtual machine restarts"
  description="Virtual machine restarts "
  authors="ujpat,amamun"
  ms.author="ujpat,amamun"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32740114"
  productPesIds="14745,16342"
  cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT" 
  schemaVersion="1"
  articleId="bf4cbfe7-47fe-4b3c-9c12-9857d695ed54"
  ownershipId="AzureData_AzureSQLVM"
/>
# Virtual machine restarts
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Help diagnose my VM restart issue",
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
            "id": "restart_error",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the error you received?",
            "required": false,
            "useAsAdditionalDetails": false
        },
        {
            "id": "machinetype",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Which machine version are you running?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Windows 7/Windows server 2008r2",
                    "text": "Windows 7/Windows server 2008r2"
                },
                {
                    "value": "Windows 8/Windows server 2012",
                    "text": "Windows 8/Windows server 2012"
                },
                {
                    "value": "Windows 8.1/Windows server 2012r2",
                    "text": "Windows 8.1/Windows server 2012r2"
                },
                {
                    "value": "Windows 10/Windows server 2016",
                    "text": "Windows 10/Windows server 2016"
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
