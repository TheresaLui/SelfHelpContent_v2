<properties 
  pageTitle="SQL Server Analysis Services (SSAS)"
  description="SQL Server Analysis Services (SSAS)"
  authors="ujpat,amamun,amigan"
  ms.author="ujpat,amamun,amigan"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32779856,32779857,32779858,32779859,32779860,32779861,32779862,32779863,32779864"
  productPesIds="14745"
  cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
  schemaVersion="1"
  articleId="d8ae3f53-8bb6-45ca-806c-08e83190428d"
  ownershipId="AzureData_AzureSQLVM"
/>
# SQL Server Analysis Services (SSAS) 
---
{
  "resourceRequired":false,
  "subscriptionRequired":false,
  "title":"SQL Server Analysis Services (SSAS)",
  "fileAttachmentHint":null,
  "formElements":[
    {
      "id":"problem_start_time",
      "order":1,
      "controlType":"datetimepicker",
      "displayLabel":"When did the problem start",
      "required":true
    },
    {
      "id":"whatAssistance",
      "visibility":null,
      "order":2,
      "controlType":"dropdown",
      "displayLabel":"What assistance do you need with SSAS?",
      "watermarkText":"Choose an option",
      "content":null,
      "infoBalloonText":null,
      "dropdownOptions":[
        {
          "text":"Initial Configuration or setup SSAS",
          "value":"configSetup"
        },
        {
          "text":"Troubleshoot or manage SSAS",
          "value":"ManageSSAS"
        },
        {
          "value":"dont_know_answer",
          "text":"I'm not sure/don't know"
        }
      ],
      "dynamicDropdownOptions":null,
      "required":true,
      "maxLength":0,
      "useAsAdditionalDetails":false,
      "numberOfLines":0
    },
    {
      "id":"error_details",
      "order":3,
      "controlType":"multilinetextbox",
      "displayLabel":"Please provide these details",
      "watermarkText":"Include error details if any",
      "required":true
    },
    {
      "id":"environmentinfo_description",
      "order":4,
      "controlType":"multilinetextbox",
      "displayLabel":"What have you tried to troubleshoot this?",
      "watermarkText":"Include what you already tried, environment information and recent changes you have done",
      "required":false
    },
    {
      "id":"problem_description",
      "order":1000,
      "controlType":"multilinetextbox",
      "displayLabel":"Description",
      "watermarkText":"Provide additional information about your issue",
      "required":true,
      "useAsAdditionalDetails":true
    }
  ],
  "$schema":"SelfHelpContent"
}
---
