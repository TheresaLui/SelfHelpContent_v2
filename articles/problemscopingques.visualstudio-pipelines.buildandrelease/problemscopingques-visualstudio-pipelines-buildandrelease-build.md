<properties
	
	articleId="problemscopingques-visualstudio-pipelines-buildandrelease-build"
	pageTitle="Scoping questions for Pipelines Build Issues"
	description="Scoping questions for Pipelines Build Issues"
	authors="chrisjco"
	ms.author="ccoop"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32452973, 32452974, 32572374, 32572376"
	productPesIds="15543"
	cloudEnvironments="public"
	schemaVersion="1"
	

/>
# Pipelines Issues Build
---
{
"$schema": "SelfHelpContent",
"resourceRequired": false,
  "subscriptionRequired": false,
  "title": "Pipeline Issues",
  "fileAttachmentHint": "Upload any screenshots or log files of the error or issue",
  "formElements": [
    {
      "id": "problem_description",
      "order": 1,
      "controlType": "multilinetextbox",
      "displayLabel": "Please provide these details",
      "required": true,
      "watermarkText": "Please provide: a detailed scenario of the error condition or issue, troubleshooting done so far, and any other relevant information.",
      "useAsAdditionalDetails": true,
      "hints": [
        {
          "text": "Azure DevOps Organization name (like XYZ.visualstudio.com or dev.azure.com/XYZ)"
        },
       	{
          "text": "Project and Definition name"
        },
    	{
          "text": "Expected behavior, actual behavior"
        },
	{
          "text": "Troubleshooting done so far"
        },
        {
          "text": "Additional details"
        },
        {
          "text": "Screenshots"
        }
      ]
    },
    {
      "id": "org_name",
      "order": 2,
      "controlType": "textbox",
      "displayLabel": "Please provide your Azure DevOps Organization name (like XYZ.visualstudio.com or dev.azure.com/XYZ)",
      "watermarkText": "Choose an option",
      "required": false
    },
    {
      "id": "project_name",
      "order": 3,
      "controlType": "textbox",
      "displayLabel": "Name of project affected",
      "required": false
    },
    {
      "id": "definition_name",
      "order": 4,
      "controlType": "textbox",
      "displayLabel": "Name of definition affected",
      "required": false
    },
    {
      "id": "problem_start_time",
      "order": 5,
      "controlType": "datetimepicker",
      "displayLabel": "When did the problem start?",
      "required": true
    }
  ]
}
---