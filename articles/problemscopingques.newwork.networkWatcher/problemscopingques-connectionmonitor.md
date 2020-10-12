<properties
pageTitle="Connection Monitor"
description="Connection Monitor"
authors="vinynigam"
ms.author="vinynigam"
selfHelpType="problemScopingQuestions"
supportTopicIds="32606420"
productPesIds="16160"
cloudEnvironments="public, Fairfax, usnat, ussec"
schemaVersion="1"
articleId="ad021338-109f-4290-a45e-asgard"
	ownershipId="CloudNet_NetAnalytics"
/>
# Connection Monitor Scoping Questions
---
{
"$schema":"SelfHelpContent",
"subscriptionRequired":true,
"resourceRequired":false,
"title":"Error while using Connection Monitor",
"fileAttachmentHint":"",
"formElements":[
{
"id":"region_id",
"order":1,
"controlType":"dropdown",
"required":true,
"displayLabel":"REQUIRED: Please choose the region in which you were trying to create/have created Connection Monitor",
"watermarkText":"Choose a region",
"dynamicDropdownOptions":{
"uri":"/subscriptions/{subscriptionId}/locations?api-version=2019-06-01",
"jTokenPath":"value",
"textProperty":"displayName",
"ValueProperty":"displayName",
"defaultDropdownOptions":{
"value":"dont_know_answer",
"text":"Other, don't know or not applicable"
}
}
},
{
"id":"operation",
"order":2,
"controlType":"dropdown",
"displayLabel":"REQUIRED: Please choose the operation you wanted to perform",
"required":true,
"dropdownOptions":[
{
"value":"Create Connection Monitor",
"text":"Create Connection Monitor"
},
{
"value":"Query results of Connection Monitor",
"text":"Query results of Connection Monitor"
},
{
"value":"Delete a Connection Monitor",
"text":"Delete a Connection Monitor"
},
{
"value":"List all Connection Monitors",
"text":"List all Connection Monitors"
},
{
"value":"Start a Connection Monitor",
"text":"Start a Connection Monitor"
},
{
"value":"Stop a Connection Monitor",
"text":"Stop a Connection Monitor"
},
{
"value":"See a Connection Monitor by name",
"text":"See a Connection Monitor by name"
},
{
"value":"dont_know_answer",
"text":"Other, don't know or not applicable"
}
]
},
{
"id":"resource_id",
"order":3,
"controlType":"dropdown",
"required":true,
"displayLabel":"REQUIRED: Please choose the CM resource with the error. If you were unable to create a CM, choose Not Created",
"watermarkText":"If you were unable to create a CM, choose Not Created.",
"dynamicDropdownOptions":{
"uri":"/subscriptions/{subscriptionId}/locations?api-version=2019-06-01",
"jTokenPath":"value",
"textProperty":"name",
"ValueProperty":"resourceID",
"defaultDropdownOptions":{
"value":"cm_not_created",
"text":"Unable to create Connection Monitor"
}
}
},
{
"id":"cm_name",
"order":4,
"controlType":"textbox",
"required":true,
"visibility":"resource_id == cm_not_created",
"displayLabel":"REQUIRED: Please enter the name with which you tried to create the Connection Monitor"
},
{
"id":"sourcevm_resourceid",
"order":5,
"controlType":"textbox",
"required":false,
"visibility":"resource_id == cm_not_created",
"displayLabel":"REQUIRED: Please enter the resource id of the source VM of the Connection Monitor you tried to create"
},
{
"id":"is_destination_accssible",
"order":6,
"controlType":"dropdown",
"required":false,
"visibility":"resource_id == cm_not_created",
"displayLabel":"REQUIRED:Is the destination accessible on the port specified  ",
"watermarkText":"If you were unable to create a CM, choose Not Created.If the issue is with all your connection monitors, choose All Connection Monitors",
"dropdownOptions":[
{
"value":"Yes",
"text":"Yes"
},
{
"value":"No",
"text":"No"
}
]
},
{
"id":"problem_start_time",
"order":7,
"controlType":"datetimepicker",
"displayLabel":"When did the problem begin or when you saw the error?",
"required":true
},
{
"id":"problem_description",
"order":8,
"controlType":"multilinetextbox",
"useAsAdditionalDetails":true,
"displayLabel":"Details of the issue.",
"watermarkText":"Provide additional information about your issue including error messages.",
"required":true
}
]
}
---