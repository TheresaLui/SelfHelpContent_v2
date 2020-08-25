<properties
  articleId="160E25A6-BB4A-4492-902D-DA7281178043"
  pageTitle="Scoping questions - Immersive Reader launch failure 'Sorry' error"
  description="Scoping questions to troubleshoot the Immersive Reader launch failure 'Sorry' error"
  authors="ltcrew"
  authoralias="ltcrew"
  ms.author="ltcrew"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32741249"
  productPesIds="17258"
  cloudEnvironments="public, usnat, ussec"
  schemaVersion="1"
  ownershipId="AzureCogSvc_CognitiveServices"
/>
# Immersive Reader launch failure 'Sorry' error
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": true,
  "resourceRequired": true,
  "title": "Immersive Reader launch failure: 'Sorry' error",
  "fileAttachmentHint": "Please upload a network trace from the browser developer tools",
  "formElements": [
    {
      "id": "problem_start_time",
      "order": 1,
      "controlType": "datetimepicker",
      "displayLabel": "When did the problem begin?",
      "required": true
    },
    {
      "id": "launch_failure_sorry_error_q2",
      "order": 2,
      "controlType": "radiobuttongroup",
      "displayLabel": "Did you create the resource with the Immersive Reader team provided script at <a href='https://docs.microsoft.com/azure/cognitive-services/immersive-reader/how-to-create-immersive-reader'>How-To: Create an Immersive Reader resource</a>?",
      "radioButtonOptions": [
        {
          "value": "yes",
          "text": "Yes"
        },
        {
          "value": "no",
          "text": "No"
        }
      ],
      "required": true
    },
    {
      "id": "launch_failure_sorry_error_q3",
      "order": 3,
      "controlType": "radiobuttongroup",
      "displayLabel": "Are there any errors in the browser developer tools Console or Network tabs?",
      "radioButtonOptions": [
        {
          "value": "yes",
          "text": "Yes"
        },
        {
          "value": "no",
          "text": "No"
        }
      ],
      "required": true
    },
    {
      "id": "launch_failure_sorry_error_q4",
      "order": 4,
      "controlType": "radiobuttongroup",
      "displayLabel": "What error are you seeing in the browser developer tools Network tab on the GetContentModelForReader call?",
      "radioButtonOptions": [
        {
          "value": "none",
          "text": "None"
        },
        {
          "value": "401",
          "text": "401"
        },
        {
          "value": "429",
          "text": "429"
        },
        {
          "value": "dont_know_answer",
          "text": "Don't know"
        }
      ],
      "required": true
    },
    {
      "id": "launch_failure_sorry_error_q5",
      "order": 5,
      "controlType": "dropdown",
      "displayLabel": "How/when do you acquire the access token?",
      "dropdownOptions": [
        {
          "value": "Each time the Immersive Reader button is clicked",
          "text": "Each time the Immersive Reader button is clicked"
        },
        {
          "value": "Once, when the main page is loaded",
          "text": "Once, when the main page is loaded"
        },
        {
          "value": "Other",
          "text": "Other"
        }
      ],
      "required": true
    },
    {
      "id": "problem_description",
      "order": 6,
      "controlType": "multilinetextbox",
      "displayLabel": "Problem description",
      "watermarkText": "Provide additional information about your issue",
      "useAsAdditionalDetails": true,
      "required": true
    }
  ]
}
---
