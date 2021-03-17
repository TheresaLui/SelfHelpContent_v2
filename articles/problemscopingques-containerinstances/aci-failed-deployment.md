<properties
	pageTitle="aci failed deployment"
	description="aci failed deployment"
	ms.author="macolso"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32588394,32588401,32588400"
	productPesIds="16326"
	cloudEnvironments="public,fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="problemscopingques-acifaileddeployment"
	ownershipId="compute-containerinstances-cs"
/>
# ACI failed deployment
---
{
   "$schema":"SelfHelpContent",
   "resourceRequired":false,
   "subscriptionRequired":true,
   "title":"ACI failed deployment",
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
         "id":"local_repro",
         "order":4,
         "controlType":"radioButtonGroup",
         "displayLabel":"Are you able to run this container successfully on your local machine?",
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
         ]
      },
      {
         "id":"previous_success",
         "order":5,
         "controlType":"radioButtonGroup",
         "displayLabel":"Have you been able to deploy this container group successfully before on ACI?",
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
         ]
      },
      {
         "id":"last_successful_deployment",
         "order":6,
         "visibility":"previous_success == Yes",
         "controlType":"datetimepicker",
         "displayLabel":"When was your last successful deployment on ACI?",
         "required":true
      }
   ]
}
---
