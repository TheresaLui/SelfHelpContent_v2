<properties
	pageTitle="aci unable to delete"
	description="aci unable to delete"
	ms.author="macolso"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32588396"
	productPesIds="16326"
	cloudEnvironments="public,fairfax"
	schemaVersion="1"
	articleId="problemscopingques-aciunabletodelete"
	ownershipId="compute-containerinstances-cs"
/>
# Unable to delete ACI
---
{
   "$schema":"SelfHelpContent",
   "resourceRequired":true,
   "subscriptionRequired":true,
   "title":"Unable to delete ACI",
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
         "displayLabel":"Are you deploying your container group into an Azure Virtual Network",
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
         "id":"stuck_resources",
         "order":5,
         "visibility":"radio_button == Yes",
         "controlType":"multiselectdropdown",
         "displayLabel":"What resources are you having difficulty deleting?",
         "dropdownOptions":[
            {
               "value":"Container group",
               "text":"Container group"
            },
            {
               "value":"Network profile",
               "text":"Network profile"
            },
            {
               "value":"Subnet",
               "text":"Subnet"
            },
            {
               "text":"Virtual network",
               "value":"Virtual network"
            },
            {
               "text":"I don't know",
               "value":"dont_know_answer"
            }
         ],
         "required":true
      }
   ]
}
---
