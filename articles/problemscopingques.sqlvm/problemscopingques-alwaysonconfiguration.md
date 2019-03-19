<properties pageTitle="AlwaysOn - Configuration"
	 description="AlwaysOn - Configuration"
	 authors="yareyes"
     ms.author="yareyes"
	 selfHelpType="problemScopingQuestions"
	 supportTopicIds="32633487"
	 productPesIds="14745"
	 cloudEnvironments="public"
	 schemaVersion="1"
	 articleId="5976622e-bb83-47cf-b199-a40e42d23e21"
/>
# AlwaysOn - Configuration
---
{
    "resourceRequired": false,
    "title": "AlwaysOn - Configuration",
    "fileAttachmentHint": null,
    "formElements": [
        {
            "id": "whichResource",
            "visibility": null,
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "What resource do you need assistance configuring?",
            "watermarkText": "Choose an option",
            "content": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Availability Group",
                    "value": "AvailabilityGroup"
                },
                {
                    "text": "Availability Group Listener",
                    "value": "AvailabilityGroupListener"
                },
                {
                    "text": "Failover Cluster settings",
                    "value": "FailoverClusterSettings"
                },
                {
                    "text": "Other resource",
                    "value": "OtherResource"
                },
                {
                    "text": "I’m not sure/don’t know",
                    "value": "NotSure"
                }
            ],
            "dynamicDropdownOptions": null,
            "hints": [],
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "howFar",
            "visibility": "whichResource != NotSure",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "How far along are you in making the configuration change?",
            "watermarkText": "Choose an option",
            "content": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "I’m still planning and have questions",
                    "value": "StillPlanning"
                },
                {
                    "text": "I’ve already started and have encountered a problem",
                    "value": "ProblemEncountered"
                }
            ],
            "dynamicDropdownOptions": null,
            "hints": [],
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "whichMethod",
            "visibility": "howFar == ProblemEncountered",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "What method are you using to make the configuration change?",
            "content": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Azure Portal",
                    "value": "Portal"
                },
                {
                    "text": "Quickstart template",
                    "value": "QuickstartTemplate"
                },
                {
                    "text": "Azure CLI",
                    "value": "Cli"
                },
                {
                    "text": "Powershell",
                    "value": "Powershell"
                },
                {
                    "text": "Transact-SQL",
                    "value": "Tsql"
                }
            ],
            "dynamicDropdownOptions": null,
            "hints": [],
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        }
    ]
}
---
