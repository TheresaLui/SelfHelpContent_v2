<properties
	pageTitle="aci network connectivity"
	description="aci network connectivity"
	ms.author="macolso"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32588398"
	productPesIds="16326"
	cloudEnvironments="public,fairfax"
	schemaVersion="1"
	articleId="problemscopingques-acinetworkconnectivity"
	ownershipId="compute-containerinstances-cs"
/>
# ACI network connectivity
---
{
   "$schema":"SelfHelpContent",
   "resourceRequired":true,
   "subscriptionRequired":true,
   "title":"ACI network connectivity",
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
         "id":"attempted_connection",
         "order":4,
         "controlType":"multilinetextbox",
         "displayLabel":"Where are you trying to connect to?",
         "required":true,
         "useAsAdditionalDetails":true,
         "watermarkText":"Examples: another Azure resource via service endpoint, external IP, etc."
      },
      {
         "id":"radio_button",
         "order":5,
         "controlType":"radioButtonGroup",
         "displayLabel":"Can you connect to the desired endpoint with a mechanism other than ACI container groups?",
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
      }
   ]
}
---
