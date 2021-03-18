<properties 
  pageTitle="Issue in performance of package execution"
  description="Issue in performance of package execution"
  authors="ujpat,amamun"
  ms.author="ujpat,amamun"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32749437"
  productPesIds="14745,16342"
  cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
  schemaVersion="1"
  articleId="8a476a25-7518-4e49-a754-4755baa503f0"
  ownershipId="AzureData_AzureSQLVM"
/>
# Issue in performance of package execution
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Issue in performance of package execution",
    "fileAttachmentHint": null,
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
        {
         "id": "whatMark",
            "visibility": null,
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Do you have a benchmark timing to compare a bad run vs. a bad Run? If so, explain further.",
            "content": null,
            "infoBalloonText": null,
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 3
        },
         {
         "id": "hasWorked",
            "visibility": null,
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Is it a dedicated SSIS server? SQL Server Memory capped?",
            "content": null,
            "infoBalloonText": null,
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 2
        },
          {
         "id": "Info",
            "visibility": null,
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Do you see any other warnings under the SSIS execution logs/report? If so, specify them.",
            "content": null,
            "infoBalloonText": null,
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 3
        },
        {
            "id": "PackageExecute",
            "visibility": null,
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Does this package execute as expected on another environment?",
            "watermarkText": "Choose an option",
            "content": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Yes",
                    "value": "Yes"
                },
                {
                    "text": "No",
                    "value": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "I'm not sure/don't know"
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
