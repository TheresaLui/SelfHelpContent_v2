<properties
	pageTitle="aci cannot change config"
	description="aci cannot change config"
	ms.author="macolso"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32588395"
	productPesIds="16326"
	cloudEnvironments="public,fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="problemscopingques-acicannotchangeconfig"
	ownershipId="compute-containerinstances-cs"
/>
# ACI cannot change config
---
{
   "$schema":"SelfHelpContent",
   "resourceRequired":false,
   "subscriptionRequired":true,
   "title":"ACI cannot change config",
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
         "id":"radio_button",
         "order":4,
         "controlType":"radioButtonGroup",
         "displayLabel":"Have you been able to update your container group configuration file previously?",
         "radioButtonOptions":[
            {
               "value":"Yes",
               "text":"Yes"
            },
            {
               "value":"No",
               "text":"No"
            },
            {
               "value":"Unsure",
               "text":"Unsure"
            }
         ],
         "required":true
      },
      {
         "id":"last_success_time",
         "order":5,
         "visibility":"radio_button == Yes",
         "controlType":"datetimepicker",
         "displayLabel":"When was the last time you were able to change your container group configuration file successfully?",
         "infoBalloonText":"Enter the approximate time",
         "required":true
      }
   ]
}
---
