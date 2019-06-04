<properties
	pageTitle="CosmosDB Database and Collection Info"
	description="CosmosDB Database and Collection Info"
	authors="rnagpal"
	selfHelpType="problemScopingQuestions" supportTopicIds="32636797,32636824,32636804,32636822,32636823,32636827,32636805,32636825,32636826,32636769,32636776,32636782,32636787,32636807,32636817,32636830,32636770,32636774,32636777,32636783,32636788,32636795,32636808,32636818,32636821,32636829,32636766,32636771,32636778,32636784,32636789,32636810,32636819,32636831,32636767,32636780,32636790,32636799,32636811,32636763,32636775,32636796,32636801,32636812,32636786,32636798,32636800,32636814"
	productPesIds="15585"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="7507fce5-61f0-40d1-8eef-8e6a0c80f941"
/>
# CosmosDB Database and Collection Info
---
{
    "resourceRequired": true,
    "title": "CosmosDB Database and Collection Info",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": false
        },
        {
            "id": "database_name",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Database name",
            "required": true,
            "hints": [
                {
                    "text": "Name of the database that is affected"
                }
            ]
        },
        {
            "id": "collection_name",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Collection name",
            "required": true,
            "hints": [
                {
                    "text": "Name of the collection that is affected"
                }
            ]
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional details about the issue that you were facing",
            "required": false,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "More information on the exact issue."
                },
                {
                    "text": "Read/Write regions where the issue is experienced"
                },
                {
                    "text": "Activity Id of the request (if available)."
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
