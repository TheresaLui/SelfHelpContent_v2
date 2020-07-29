<properties 
  pageTitle="SQL Server Setup or patching"
  description="SQL Server Setup or patching"
  authors="ujpat,amamun"
  ms.author="ujpat,amamun"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32740100"
  productPesIds="14745,16342"
  cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
  schemaVersion="1"
  articleId="a67c96c2-f732-4d01-a7c8-5780ce368a90"
  ownershipId="AzureData_AzureSQLVM"
/>
# SQL Server Setup or patching
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "SQL Server Setup or patching",
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
            "id": "whatKind",
            "visibility": null,
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What kind of patching assistance do you need?",
            "watermarkText": "Choose an option",
            "content": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "SQL Patching",
                    "value": "SQLPatching"
                },
                {
                    "text": "Windows Patching",
                    "value": "WindowsPatching"
                },
                {
                    "text": "Automated Patching on Azure Portal",
                    "value": "AutomatedPatchingonAzurePortal"
                },
                {
                    "value": "dont_know_answer",
                    "text": "I'm not sure/don't know"
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
