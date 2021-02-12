 <properties
      articleId="EC42BF9F-D6A0-425E-82A8-3EA6A2BCEF50"
      pageTitle="data sources and connectors"
      description="data sources and connectors"
      authors="pjfreitas"
      ms.author="pfreitas"
      selfHelpType="problemScopingQuestions"
      supportTopicIds="32675686"
      productPesIds="16157"
      cloudEnvironments="public, MoonCake, fairfax, usnat, ussec" 
      schemaVersion="1"
	ownershipId="AzureData_AnalysisServices"
/>
# Connecting to servers
---
{
  "resourceRequired": false,
  "subscriptionRequired": true,
  "title": "Connecting to servers",
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
      "id": "data_sources_and_connectors_400",
      "order": 400,
      "controltype": "multilinetextbox",
      "displaylabel": "What datasource or connector are you using?",
      "watermarktext": "What datasource or connector are you using?",
      "required": false
    }
,
    {
      "id": "data_sources_and_connectors_500",
      "order": 500,
      "controltype": "multilinetextbox",
      "displaylabel": "What is the full error message with all error IDs?",
      "watermarktext": "What is the full error message with all error IDs?",
      "required": false
    }
,
    {
      "id": "data_sources_and_connectors_600",
      "order": 600,
      "controltype": "dropdown",
      "displaylabel": "Can the issue be reproduced by other users?",
      "watermarkText":"Choose an option","dropdownOptions":[{"value": "Yes","text": "Yes"},{"value": "No","text": "No"},{"value": "dont_know_answer","text":"Other, don't know or not applicable"}],
      "required": true
    }
,
    {
      "id": "data_sources_and_connectors_700",
      "order": 700,
      "controltype": "dropdown",
      "displaylabel": "Is this an intermittent or permanent issue?",
      "watermarkText":"Choose an option","dropdownOptions":[{"value": "Intermittent","text": "Intermittent"},{"value": "Permanent","text": "Permanent"},{"value": "dont_know_answer","text":"Other, don't know or not applicable"}],
      "required": true
    }
  ],
  "$schema": "SelfHelpContent"
}
---
