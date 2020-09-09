<properties
  pageTitle="Cannot stop, start, or restart a VM"
  description="Cannot stop, start, or restart a VM"
  authors="ujpat,amamun"
  ms.author="ujpat,amamun"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32740069"
  productPesIds="14745,16342"
  cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
  schemaVersion="1"
  articleId="13c1c6de-10a9-4df6-8f79-2fe0009581af"
  ownershipId="AzureData_AzureSQLVM"
/>
# Cannot stop, start, or restart a VM
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "My VM is unresponsive to start or stop operations",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "startstop_error",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the error you received?",
            "required": false,
            "useAsAdditionalDetails": false
        },
        {
            "id": "startstop_previous",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Has this operation worked previously for this VM?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "I do not know",
                    "text": "I do not know"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
