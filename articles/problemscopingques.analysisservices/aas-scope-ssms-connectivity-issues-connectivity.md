 <properties
      articleId="CC88FE0E-5A0C-4BA4-B748-C01703CDD0FE"
      pageTitle="ssms connectivity issues"
      description="ssms connectivity issues"
      authors="pjfreitas"
      ms.author="pfreitas"
      selfHelpType="problemScopingQuestions"
      supportTopicIds="32675692"
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
      "id": "ssms_connectivity_issues_400",
      "order": 400,
      "controltype": "dropdown",
      "displaylabel": "Can you connect from other tools such as Excel or Power BI Desktop?",
      "watermarkText":"Choose an option","dropdownOptions":[{"value": "Yes","text": "Yes"},{"value": "No","text": "No"},{"value": "dont_know_answer","text":"Other, don't know or not applicable"}],
      "required": true
    }
,
    {
      "id": "ssms_connectivity_issues_500",
      "order": 500,
      "controltype": "multilinetextbox",
      "displaylabel": "What version of SSMS is being used?",
      "watermarktext": "What version of SSMS is being used?",
      "required": false
    }
,
    {
      "id": "ssms_connectivity_issues_600",
      "order": 600,
      "controltype": "multilinetextbox",
      "displaylabel": "What is the full error message with all error IDs?",
      "watermarktext": "What is the full error message with all error IDs?",
      "required": false
    }
,
    {
      "id": "ssms_connectivity_issues_700",
      "order": 700,
      "controltype": "dropdown",
      "displaylabel": "Can the issue be reproduced by other users?",
      "watermarkText":"Choose an option","dropdownOptions":[{"value": "Yes","text": "Yes"},{"value": "No","text": "No"},{"value": "dont_know_answer","text":"Other, don't know or not applicable"}],
      "required": true
    }
,
    {
      "id": "ssms_connectivity_issues_800",
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
