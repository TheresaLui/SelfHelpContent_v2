<properties 
  pageTitle="Issue in Package deployment"
  description="Issue in Package deployment"
  authors="ujpat,amamun"
  ms.author="ujpat,amamun"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32749436"
  productPesIds="14745,16342"
  cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
  schemaVersion="1"
  articleId="7735839e-a6e3-4f13-9dc6-875010f87b80"
  ownershipId="AzureData_AzureSQLVM"
/>
# Issue in Package deployment
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Issue in Package deployment",
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
         "id": "TargetVersion",
            "visibility": null,
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "What is the version of the Target SQL Server where you are deploying the SSIS projects?",
            "content": null,
            "infoBalloonText": null,
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 3
        },
         {
         "id": "Permissions",
            "visibility": null,
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Did you change the SQL Server service account recently or can you confirm with your Domain admins if they revoked any permissions/privileges?",
            "content": null,
            "infoBalloonText": null,
            "required": false,
            "useAsAdditionalDetails": false
        },
        {
            "id": "TargetServer",
            "visibility": null,
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Did you set the TargetServerVersion of the SSIS project accordingly?  If not, set it accordingly.",
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
