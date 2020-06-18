<properties 
  pageTitle="SQL Server exceptions, crashes, dumps"
  description="SQL Server exceptions, crashes, dumps"
  authors="ujpat,amamun"
  ms.author="ujpat,amamun"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32740096"
  productPesIds="14745,16342"
  cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
  schemaVersion="1"
  articleId="fd32f54f-3351-4f55-ac07-cff0d1618811"
  ownershipId="AzureData_AzureSQLVM"
/>
# SQL Server exceptions, crashes, dumps
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "SQL Server exceptions, crashes, dumps",
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
            "id": "whichDump",
            "visibility": null,
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Is there a dump file generated?",
            "watermarkText": "Choose an option",
            "content": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Yes (attach file below)",
                    "value": "Yes"
                },
                {
                    "text": "No",
                    "value": "No"
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
             "id": "WhichVersion",
             "visibility": null,
             "order": 3,
             "controlType": "dropdown",
             "displayLabel": "Are you on the latest build for your SQL version?",
             "watermarkText": "Choose an option",
             "content": null,
             "infoBalloonText": null,
             "dropdownOptions": [
                 {
                     "text": "I am on the latest build",
                     "value": "LatestBuild"
                 },
                 {
                     "text": "I am on the build mentioned below (describe below)",
                     "value": "BuildBelow"
                 },
                 {
                     "text": "I'm not sure/don't know",
                     "value": "dont_know_answer"
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
