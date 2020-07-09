<properties
	pageTitle="aci does not start stop or restart"
	description="aci does not start stop or restart"
	ms.author="macolso"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32588392"
	productPesIds="16326"
	cloudEnvironments="public,fairfax"
	schemaVersion="1"
	articleId="problemscopingques-acidoesntstartstoprestart"
	ownershipId="compute-containerinstances-cs"
/>
# ACI does not start stop or restart
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
         "id":"problem_description",
         "order":3,
         "controlType":"multilinetextbox",
         "displayLabel":"Please provide additional context about the issue you are encountering.",
         "required":true,
         "useAsAdditionalDetails":true,
         "watermarkText":"Always provide the full error text from Azure Container Instances when possible."
      },
      {
        "id": "problem_operation",
        "order": 4,
        "controlType": "multiselectdropdown",
        "displayLabel": "Select the operation(s) you are experiencing difficulty with",
        "dropdownOptions": [{
                "value": "Start",
                "text": "Start"
            }, {
                "value": "Stop",
                "text": "Stop"
            }, {
                "value": "Restart",
                "text": "Restart"
            }
        ],
        "required": true
    }
   ]
}
---
