<properties pageTitle="Upgrade-downgrade SQL Server Version/Edition"
	 description="Upgrade-downgrade SQL Server Version/Edition"
	 authors="yareyes"
     ms.author="yareyes"
	 selfHelpType="problemScopingQuestions"
	 supportTopicIds="32633525"
	 productPesIds="14745"
	 cloudEnvironments="public,fairfax"
	 schemaVersion="1"
	 articleId="2fac49be-dd38-4cdf-87b3-fb2e0bf1990b"
	ownershipId="AzureData_AzureSQLVM"
/>
# Upgrade-downgrade SQL Server Version/Edition
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Upgrade-downgrade SQL Server Version/Edition",
    "fileAttachmentHint": null,
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start",
            "required": true
        },
        {
            "id": "whichOption",
            "visibility": null,
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Are you trying to change the SQL Server version or edition?",
            "watermarkText": "Choose an option",
            "content": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "SQL Server version (e.g. 2012, 2014, 2016, 2017, …)",
                    "value": "SQLVersion"
                },
                {
                    "text": "SQL Server Edition (e.g. Express, Web, Standard, Enterprise)",
                    "value": "SQLEdition"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "dynamicDropdownOptions": null,
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "upgradeDowngrade",
            "visibility": null,
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Are you interested in upgrade or downgrade?",
            "watermarkText": "Choose an option",
            "content": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Upgrade",
                    "value": "Upgrade"
                },
                {
                    "text": "Downgrade",
                    "value": "Downgrade"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "dynamicDropdownOptions": null,
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
