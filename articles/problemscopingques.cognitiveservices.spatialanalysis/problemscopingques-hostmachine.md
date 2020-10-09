<properties
  pageTitle="Scoping questions - Issues related to spatial analysis usage"
  description="Scoping questions to troubleshoot the issues related to the host machine setup for the deployment of the spatial analysis container."
  ms.author="kabrow"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32767683, 32767689"
  productPesIds="16970"
  cloudEnvironments="public, Fairfax, usnat, ussec, mooncake"
  schemaVersion="1"
  articleId="53a92698-a164-8375-253a-070312f502e6, 997fa6d5-433b-9e65-3460-e239a25c237b"
  ownershipId="AzureCogSvc_CognitiveServices"
/>

# Issues related to host machine setup for spatial analysis usage
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": true,
  "resourceRequired": true,
  "title": "Issues related to the host machine setup for the use of the spatial analysis container",
  "fileAttachmentHint": "Please provide a screenshot of any errors",
  "formElements": [{
      "id": "problem_start_time",
      "order": 1,
      "controlType": "datetimepicker",
      "displayLabel": "When did the problem begin?",
      "required": true
    },{
      "id": "ASE_device",
      "order": 2,
      "controlType": "multilinetextbox",
      "displayLabel": "If your host computer is an Azure Stack Edge Device, have you met the prerequisite requirements including: activating your Azure Stack Edge Device, and getting access to a Windows client system running PowerShell 5.0 or later to access the device?",
      "required": true
    },{
      "id": "non_ASE_device",
      "order": 3,
      "controlType": "multilinetextbox",
      "displayLabel": "If your host computer is not an Azure Stack Edge Device, are you having issues with configuring IoT edge and registering your device as an IoT Edge via a connection string? ?",
      "required": false
    },{
      "id": "connection_string",
      "order": 4,
      "controlType": "radiobuttongroup",
      "displayLabel": "Are you having any issues related to the retrieval of or use of your connection string?",
      "radioButtonOptions": [{
          "value": "Yes",
          "text": "Yes"
        },{
          "value": "No",
          "text": "No"
        }
      ],
      "required": true
    },{
      "id": "problem_description",
      "order": 5,
      "controlType": "multilinetextbox",
      "displayLabel": "Can you provide any additional details about the issue you are having regarding your container deployment?",
      "useAsAdditionalDetails": true,
      "required": true
    }
  ]
}
---
