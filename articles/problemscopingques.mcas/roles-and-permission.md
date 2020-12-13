<properties
	pageTitle="Cloud App Security - Portal Usage and Configuration - Roles and permission"
	description="Cloud App Security - Portal Usage and Configuration - Roles and permission"
	authors="ms-nagrand"
	ms.author="nagrand"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32729002﻿"
    productPesIds="16031"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="scoping_Roles and permission"
	schemaVersion="1"
	ownershipId="CloudAppSecurity_Portal"
/>
# Portal Usage and Configuration - Roles and permission
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "Portal Usage and Configuration - Roles and permission",
				"subscriptionRequired": false,
                "formElements": [
                {
                    "id": "MCAS_URL",
                    "order": 2,
                    "controlType": "textbox",
                    "displayLabel": "Please provide your MCAS tenant URL (e.g: https://(domain name).portal.cloudappsecurity.com/)",
                    "required": true
                },
				{
                    "id": "User_Permission",
                    "order": 3,
                    "controlType": "textbox",
                    "displayLabel": "For permission issues, please add the role of the user from AAD/O365",
                    "required": false
                },
				{
                    "id": "problem_description",
                    "order": 1,
                    "controlType": "multilinetextbox",
                    "displayLabel": "Description",
                    "useAsAdditionalDetails": true,
                    "required": true
                    },{
                    "id": "problem_start_time",
                    "order": 8,
                    "controlType": "datetimepicker",
                    "displayLabel": "When did the problem start?",
                    "required": true
                  }
                  ]
}
---
