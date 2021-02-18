<properties 
  pageTitle="Issue or errors in package execution"
  description="Issue or errors in package execution"
  authors="ujpat,amamun"
  ms.author="ujpat,amamun"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32749439"
  productPesIds="14745,16342"
  cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
  schemaVersion="1"
  articleId="a5df18eb-7790-410f-96ea-6cc4879213dd"
  ownershipId="AzureData_AzureSQLVM"
/>
# Issue or errors in package execution
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Issue or errors in package execution",
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
         "id": "whatVersion",
            "visibility": null,
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "What version of SSIS runtime is being used? ",
            "watermarkText": "Please fill in the version details",
            "content": null,
            "infoBalloonText": null,
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 2
        },
         {
         "id": "howExecute",
            "visibility": null,
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "How is the package being executed and did any errors occur? ",
            "content": null,
            "infoBalloonText": null,
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 3
        },
        {
            "id": "issueType",
            "visibility": null,
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Is the issue intermittent or consistent? ",
            "watermarkText": "Choose an option",
            "content": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Intermittent",
                    "value": "Intermittent"
                },
                {
                    "text": "Consistent",
                    "value": "Consistent"
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
