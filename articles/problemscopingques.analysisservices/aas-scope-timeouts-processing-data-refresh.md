 <properties
      articleId="61B69E2F-C93D-4DB7-B771-80D62027B0B8"
      pageTitle="timeouts"
      description="timeouts"
      authors="pjfreitas"
      ms.author="pfreitas"
      selfHelpType="problemScopingQuestions"
      supportTopicIds="32675705"
      productPesIds="16157"
      cloudEnvironments="public, MoonCake, fairfax, usnat, ussec" 
      schemaVersion="1"
	ownershipId="AzureData_AnalysisServices"
/>
# Automating Azure Analysis Services processing with Azure Functions
---
{
  "resourceRequired": false,
  "subscriptionRequired": true,
  "title": "Automating Azure Analysis Services processing with Azure Functions",
  "fileAttachmentHint":"",
  "formElements":
  [
    {
      "id": "problem_description",
      "order": 100,
      "controlType": "multilinetextbox",
      "displayLabel": "Additional details about the issue",
      "watermarkText": "The attempted scenario with resulting observed vs expected behavior.",
      "required": true,
      "useAsAdditionalDetails": true
    }
,
    {
      "id": "problem_start_time",
      "order": 200,
      "controlType": "datetimepicker",
      "displayLabel": "What time did the problem begin?",
      "required": true
    }
,
    {
      "id": "problem_end_time",
      "order": 300,
      "controlType": "datetimepicker",
      "displayLabel": "Approximate time when the problem stopped occurring. If the issue is ongoing, leave this field blank",
      "required": false
    }
,
    {
      "id": "timeouts_400",
      "order": 400,
      "controltype": "dropdown",
      "displaylabel": "Is the cube processing timing out at the same interval each time?",
      "watermarkText":"Choose an option","dropdownOptions":[{"value": "Yes","text": "Yes"},{"value": "No","text": "No"},{"value": "dont_know_answer","text":"Other, don't know or not applicable"}],
      "required": true
    }
,
    {
      "id": "timeouts_500",
      "order": 500,
      "controltype": "multilinetextbox",
      "displaylabel": "If yes how long?",
      "watermarktext": "If yes how long?",
      "required": false
    }
,
    {
      "id": "timeouts_600",
      "order": 600,
      "controltype": "multilinetextbox",
      "displaylabel": "What is the full error message with all error IDs?",
      "watermarktext": "What is the full error message with all error IDs?",
      "required": false
    }
,
    {
      "id": "timeouts_700",
      "order": 700,
      "controltype": "dropdown",
      "displaylabel": "Can the issue be reproduced by other users?",
      "watermarkText":"Choose an option","dropdownOptions":[{"value": "Yes","text": "Yes"},{"value": "No","text": "No"},{"value": "dont_know_answer","text":"Other, don't know or not applicable"}],
      "required": true
    }
,
    {
      "id": "timeouts_800",
      "order": 800,
      "controltype": "dropdown",
      "displaylabel": "Is this an intermittent or permanent issue?",
      "watermarkText":"Choose an option","dropdownOptions":[{"value": "Intermittent","text": "Intermittent"},{"value": "Permanent","text": "Permanent"},{"value": "dont_know_answer","text":"Other, don't know or not applicable"}],
      "required": true
    }
  ],
  "$schema": "SelfHelpContent"
}
---
