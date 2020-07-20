 <properties
      articleId="F34F1F3B-3285-43A1-A411-9E86143ACD07"
      pageTitle="deploy model"
      description="deploy model"
      authors="pjfreitas"
      ms.author="pfreitas"
      selfHelpType="problemScopingQuestions"
      supportTopicIds="32675687"
      productPesIds="16157"
      cloudEnvironments="public, MoonCake, fairfax, usnat, ussec" 
      schemaVersion="1"
	ownershipId="AzureData_AnalysisServices"
/>
# Deployment Script Files - Input Used to Create Deployment Script
---
{
  "resourceRequired": false,
  "subscriptionRequired": true,
  "title": "Deployment Script Files - Input Used to Create Deployment Script",
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
      "id": "deploy_model_400",
      "order": 400,
      "controltype": "multilinetextbox",
      "displaylabel": "What tool is being used to deploy? (Visual Studio, DevOps, Azure Portal, etc.)",
      "watermarktext": "What tool is being used to deploy? (Visual Studio, DevOps, Azure Portal, etc.)",
      "required": false
    }
,
    {
      "id": "deploy_model_500",
      "order": 500,
      "controltype": "multilinetextbox",
      "displaylabel": "Did the deployment timeout, complete or take longer than expected?",
      "watermarktext": "Did the deployment timeout, complete or take longer than expected?",
      "required": false
    }
,
    {
      "id": "deploy_model_600",
      "order": 600,
      "controltype": "multilinetextbox",
      "displaylabel": "What application being used? ",
      "watermarktext": "What application being used? ",
      "required": false
    }
,
    {
      "id": "deploy_model_700",
      "order": 700,
      "controltype": "multilinetextbox",
      "displaylabel": "What is the full error message with all error IDs?",
      "watermarktext": "What is the full error message with all error IDs?",
      "required": false
    }
,
    {
      "id": "deploy_model_800",
      "order": 800,
      "controltype": "dropdown",
      "displaylabel": "Can the issue be reproduced by other users?",
      "watermarkText":"Choose an option","dropdownOptions":[{"value": "Yes","text": "Yes"},{"value": "No","text": "No"},{"value": "dont_know_answer","text":"Other, don't know or not applicable"}],
      "required": true
    }
  ],
  "$schema": "SelfHelpContent"
}
---
