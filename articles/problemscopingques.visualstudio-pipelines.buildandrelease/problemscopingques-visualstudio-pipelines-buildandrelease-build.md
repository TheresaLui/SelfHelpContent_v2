<properties
	
	articleId="problemscopingques-visualstudio-pipelines-buildandrelease-build"
	pageTitle="Scoping questions for Pipelines Build Issues"
	description="Scoping questions for Pipelines Build Issues"
	authors="chrisjco"
	ms.author="ccoop"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="
32742292, 
32742305, 
32742307, 
32742308, 
32742314, 
32742315, 
32742319, 
32742320, 
32742322, 
32742326, 
32742330, 
32742291, 
32742295, 
32742306, 
32742311, 
32742312, 
32742316, 
32742317, 
32742321, 
32742323,
32742318, 
32742328, 
32742327, 
32742329, 
32742331, 
32742332, 
32742333, 
32742334, 
32742294, 
32742296, 
32742297, 
32742298, 
32742299, 
32742300, 
32742302, 
32742303, 
32742304, 
32742310, 
32742324, 
32742293, 
32742301, 
32742309, 
32742313, 
32742325"
	productPesIds="15543"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Azure_DevOps_Services"
	

/>
# Pipelines Issues Build
---
{
"$schema": "SelfHelpContent",
"resourceRequired": false,
  "subscriptionRequired": false,
  "title": "Pipeline Issues",
    "fileAttachmentHint": "Upload any screenshots or the <a href='https://docs.microsoft.com/azure/devops/pipelines/troubleshooting?view=azure-devops#get-logs-to-diagnose-problems'>Diagnostic log</a>",
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
          "text": "Error message (if any)"
        },
	{
          "text": "Troubleshooting done so far"
        },
        {
          "text": "Additional details"
        },
        {
          "text": "Screenshots and Diagnostic log"
        }
      ]
    },
    {
      "id": "org_name",
      "order": 2,
      "controlType": "textbox",
      "displayLabel": "Please provide your Azure DevOps Organization URL (like XYZ.visualstudio.com or dev.azure.com/XYZ)",
      "watermarkText": "Organization URL",
      "required": false
    },
    {
      "id": "definition_name",
      "order": 3,
      "controlType": "textbox",
      "displayLabel": "Name of pipeline affected",
      "required": false
    },
    {
      "id": "project_name",
      "order": 4,
      "controlType": "textbox",
      "displayLabel": "Name of Team Project with pipeline affected",
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