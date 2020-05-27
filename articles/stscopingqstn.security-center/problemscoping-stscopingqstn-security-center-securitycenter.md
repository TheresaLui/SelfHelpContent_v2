<properties
	pageTitle="Scoping questions for Azure Security Center"
	description="Scoping questions for Azure Security Center"
	authors="KSarens"
   selfHelpType="problemScopingQuestions"
	supportTopicIds="32450560,32450562,32591163,32591165,32450565,32550673,32570938,32508110,32518306,32553101,32553102,32592842,32450564,32510203,32550658,32550672,32553098,32589905,32591166,32451792,32584147,32589963,32589965,32591167,32550659,32550660,32550827,32553099,32553100,32593794,32448383,32450559,32553103,32589964,32589996,32591161,32592929,32450561,32450563,32550686,32589943,32589962,32591162,32591164"
	productPesIds="15947"
	cloudEnvironments="public, fairfax, usnat, ussec"
   schemaVersion="1"
   articleId="8fe29cdc-4d5b-4b33-9dd4-1b3a3c0f1c7d"
	ownershipId="Azure_Security_Security_Center"
/>
#Azure Security Center
---
{
    "resourceRequired": false,
    "formElements": [
        {
            "id": "problem_description",
            "order": 1,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "hints": [
                {
                    "text": "Please note that Azure Security Center is a product for any other security issue in Azure please select the appropriate service. Example: Suspicious activity on your VM -> COMPUTE -> Virtual Machine running...Delays to resolve non Azure Security Center issues will occur if you use this service to open a support case."
                }
            ]
        },
        {
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "Problem start time",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---