<properties 
  pageTitle="Issue in SSIS Service"
  description="Issue in SSIS Service"
  authors="ujpat,amamun"
  ms.author="ujpat,amamun"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32749438"
  productPesIds="14745,16342"
  cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
  schemaVersion="1"
  articleId="496cca67-a726-4750-9e42-a073f207f9b4"
  ownershipId="AzureData_AzureSQLVM"
/>
# Issue in SSIS Service
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Issue in SSIS Service",
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
         "id": "whatError",
            "visibility": null,
            "order": 2,
            "controlType": "textbox",
            "displayLabel": " Do you see any other SSIS errors in the event log? If so, share the error event.",
            "content": null,
            "infoBalloonText": null,
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 2
        },
         {
         "id": "hasWorked",
            "visibility": null,
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Has it worked on this computer? Did you install SSIS component successfully?",
            "content": null,
            "infoBalloonText": null,
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 2
        },
          {
         "id": "KbInfo",
            "visibility": null,
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Any recent changes to the .NET framework recently? If so, what are the new KBs installed now?",
            "content": null,
            "infoBalloonText": null,
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 3
        },
        {
            "id": "issueType",
            "visibility": null,
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Did you change the Integration services (SSIS) service account recently? ",
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
