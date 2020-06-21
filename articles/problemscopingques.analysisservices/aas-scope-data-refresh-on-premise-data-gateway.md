 <properties
      articleId="6139E6EA-9E4F-4923-9E3B-F3357C5A1F20"
      pageTitle="data refresh"
      description="data refresh"
      authors="pjfreitas"
      ms.author="pfreitas"
      selfHelpType="problemScopingQuestions"
      supportTopicIds="32675683"
      productPesIds="16157"
      cloudEnvironments="public, MoonCake, fairfax, usnat, ussec" 
      schemaVersion="1"
	ownershipId="AzureData_AnalysisServices"
/>
# On-premises data gateway support for Azure Analysis Services
---
{
  "resourceRequired": false,
  "subscriptionRequired": true,
  "title": "On-premises data gateway support for Azure Analysis Services",
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
      "id": "data_refresh_400",
      "order": 400,
      "controltype": "multilinetextbox",
      "displaylabel": "What is the full error message with all error IDs?",
      "watermarktext": "What is the full error message with all error IDs?",
      "required": false
    }
,
    {
      "id": "data_refresh_500",
      "order": 500,
      "controltype": "dropdown",
      "displaylabel": "Can the issue be reproduced by other users?",
      "watermarkText":"Choose an option","dropdownOptions":[{"value": "Yes","text": "Yes"},{"value": "No","text": "No"},{"value": "dont_know_answer","text":"Other, don't know or not applicable"}],
      "required": true
    }
,
    {
      "id": "data_refresh_600",
      "order": 600,
      "controltype": "dropdown",
      "displaylabel": "Is this an intermittent or permanent issue?",
      "watermarkText":"Choose an option","dropdownOptions":[{"value": "Intermittent","text": "Intermittent"},{"value": "Permanent","text": "Permanent"},{"value": "dont_know_answer","text":"Other, don't know or not applicable"}],
      "required": true
    }
  ],
  "$schema": "SelfHelpContent"
}
---
