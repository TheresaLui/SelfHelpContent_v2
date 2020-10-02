<properties
	pageTitle="aci unable to connect"
	description="aci unable to connect"
	ms.author="macolso"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32588399"
	productPesIds="16326"
	cloudEnvironments="public,fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="problemscopingques-aciunabletoconnect"
	ownershipId="compute-containerinstances-cs"
/>
# Unable to connect to ACI
---
{
   "$schema":"SelfHelpContent",
   "resourceRequired":false,
   "subscriptionRequired":true,
   "title":"Unable to connect to ACI",
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
         "id":"connection_mechanism",
         "order":4,
         "controlType":"multiselectdropdown",
         "displayLabel":"Select the applications running on your virtual machine",
         "dropdownOptions":[
            {
               "value":"Public IP",
               "text":"Public IP"
            },
            {
               "value":"Private IP",
               "text":"Private IP"
            },
            {
               "value":"SSH into container",
               "text":"SSH into container"
            },
            {
               "text":"Other, don't know or not applicable",
               "value":"dont_know_answer"
            }
         ],
         "required":true
      }
   ]
}
---
