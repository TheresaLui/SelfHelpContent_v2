<properties
    pageTitle="SAP HANA on Azure Large Instances"
    description="Problem scoping for SAP HANA on Azure Large Instances"
    authors="phgantik,timbasham"
    ms.author="tibasham"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32549255,32549257,32549256,32549258,32549259,32632347,32632349,32632350,32632360,32632373,32632374,32632342,32632345,32632357,32632361,32632365,32632369,32632371,32632372,32632337,32632338,32632339,32632354,32632366,32632348,32632351,32632352,32632353,32632358,32632362,32632370,32632346,32632364,32632340,32632341,32632343,32632355,32632356,32632363,32632367,32632344,32632359,32632368"
    productPesIds="16208,15571,15797"
    cloudEnvironments="public"
    schemaVersion="1"
    articleId="3561f156-4abd-4450-9a71-792802e50f89"
/>


# SAP HANA on Azure Large Instances
---
{
    "resourceRequired": false,
    "title": "Configure SAP HANA large instances",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "configure_sap_hana",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Is this an Azure VM or a SAP HANA Large Instance",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Azure VM",
                    "text": "Azure VM(G-Series, M-Series,DS-Series etc)"
                },
                {
                    "value": "SAP HANA Large Instance",
                    "text": "SAP HANA Large Instance"
                }
            ],
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "region_sap_hana",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Select the SAP HANA Large Instances Region",
            "dropdownOptions": [
                {
                    "value": "West US",
                    "text": "West US"
                },
                {
                    "value": "East US",
                    "text": "East US"
                },
                {
                    "value": "North Europe",
                    "text": "North Europe"
                },
                {
                    "value": "West Europe",
                    "text": "West Europe"
                },
                {
                    "value": "Australia East",
                    "text": "Australia East"
                },
                {
                    "value": "Australia Southeast",
                    "text": "Australia Southeast"
                },
                {
                    "value": "other",
                    "text": "other"
                }
            ],
            "required": true
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional details",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Names of the SAP HANA Large Instances."
                },
                {
                    "text": "The IP address of the SAP HANA Large Instance"
                },
                {
                    "text": "Note: Make sure you have selected the subscription which contains the SAP HANA Large Instance while creating this case"
                }
            ]
        }
    ]
}
---
