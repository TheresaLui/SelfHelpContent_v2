<properties
	pageTitle="aci cannot access metrics logs or events"
	description="aci cannot access metrics logs or events"
	ms.author="macolso"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32641172"
	productPesIds="16326"
	cloudEnvironments="public,fairfax"
	schemaVersion="1"
	articleId="problemscopingques-acimetricslogsevents"
	ownershipId="compute-containerinstances-cs"
/>
# ACI cannot access metrics, logs, or events
---
{
   "$schema":"SelfHelpContent",
   "resourceRequired":true,
   "subscriptionRequired":true,
   "title":"ACI cannot access metrics logs or events",
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
         "id":"applications_on_vm",
         "order":4,
         "required":true,
         "controlType":"multiselectdropdown",
         "displayLabel":"Select the diagnostic(s) you're having difficulty with:",
         "dropdownOptions":[
            {
               "value":"Metrics",
               "text":"Metrics"
            },
            {
               "value":"Container logs (std out/std err)",
               "text":"Container logs (std out/std err)"
            },
            {
               "value":"Platform events",
               "text":"Platform events"
            }
         ],
         "required":false
      }
   ]
}
---
