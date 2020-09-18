<properties
	pageTitle="aci managed identity integration"
	description="aci managed identity integration"
	ms.author="macolso"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32641172"
	productPesIds="16326"
	cloudEnvironments="public,fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="problemscopingques-acimanagedidentityintegration"
	ownershipId="compute-containerinstances-cs"
/>
# ACI Managed Identity integration
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
         "id":"local_repro",
         "order":4,
         "controlType":"radioButtonGroup",
         "required":true,
         "displayLabel":"Which type(s) of managed identity integration are you having difficulty with??",
         "radioButtonOptions":[
            {
               "value":"User assigned",
               "text":"User assigned"
            },
            {
               "value":"System assigned",
               "text":"System assigned"
            },
            {
               "value":"Both",
               "text":"Both"
            }
         ]
      }
   ]
}
---
