<properties 
  pageTitle="Tools -Management Studio, Azure Data Studio"
  description="Tools -Management Studio, Azure Data Studio"
  authors="ujpat,amamun"
  ms.author="ujpat,amamun"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32740105"
  productPesIds="14745,16342"
  cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
  schemaVersion="1"
  articleId="3f83ed8c-92ff-472e-a218-c838457b7e70"
  ownershipId="AzureData_AzureSQLVM"
/>
# Tools -Management Studio, Azure Data Studio
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Tools -Management Studio, Azure Data Studio",
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
            "id": "whichSSMS",
            "visibility": null,
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Does the same functionality work on some other box/latest SSMS version?",
            "watermarkText": "Choose an option",
            "content": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "It works on another machine",
                    "value": "WorksOnSomeMachine"
                },
                {
                    "text": "I have not tried this",
                    "value": "DidNotTry"
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
