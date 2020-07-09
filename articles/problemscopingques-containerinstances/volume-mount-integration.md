<properties
	pageTitle="aci volume mount integration"
	description="aci volume mount integration"
	ms.author="macolso"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32742284"
	productPesIds="16326"
	cloudEnvironments="public,fairfax"
	schemaVersion="1"
	articleId="problemscopingques-acivolumemount"
	ownershipId="compute-containerinstances-cs"
/>
# ACI volume mount integration
---
{
   "$schema":"SelfHelpContent",
   "resourceRequired":true,
   "subscriptionRequired":true,
   "title":"ACI Managed Identity Integration",
   "formElements":[
      {
         "id":"problem_start_time",
         "order":1,
         "controlType":"datetimepicker",
         "displayLabel":"When did the problem start?",
         "infoBalloonText":"Enter the approximate time you started to see the error.",
         "required":true
      },
      {
         "id":"problem_end_time",
         "order":2,
         "controlType":"datetimepicker",
         "displayLabel":"When did the problem stop? (If ongoing, leave this field blank)",
         "infoBalloonText":"Enter when the error stopped, or leave blank if the issue is ongoing.",
         "required":false
      },
      {
         "id":"problem_description",
         "order":3,
         "controlType":"multilinetextbox",
         "displayLabel":"Please provide additional context about the issue you are encountering.",
         "required":true,
         "useAsAdditionalDetails":true,
         "watermarkText":"Always provide the full error text from Azure Container Instances when possible."
      },
      {
         "id":"volume_mount_type",
         "order":4,
         "required":true,
         "controlType":"multiselectdropdown",
         "displayLabel":"Select the volume type(s) you're having difficulty with:",
         "dropdownOptions":[
            {
               "value":"Azure File Share",
               "text":"Azure File Share"
            },
            {
               "value":"GitHub Repository",
               "text":"GitHub Repository"
            },
            {
               "value":"Empty Directory",
               "text":"Empty Directory"
            },
            {
               "value":"Secret",
               "text":"Secret"
            }
         ],
         "required":true
      },
      {
         "id":"radio_button",
         "order":5,
         "controlType":"radioButtonGroup",
         "displayLabel":"Select the operation you are having difficulty with:",
         "radioButtonOptions":[
            {
               "value":"Read",
               "text":"Read"
            },
            {
               "value":"Write",
               "text":"Write"
            },
            {
               "value":"Both",
               "text":"Both"
            }
         ],
         "required":false
      }
   ]
}
---
