<properties
   pageTitle="Scoping questions for VPN Gateway Issues"
   description="Scoping questions for VPN Gateway Issues"
   authors="tatec,jwazurecloud"
   ms.author="radwiv"
   selfHelpType="problemScopingQuestions"
   supportTopicIds="32591148,32591150,32591151,32591159,32591155,32591154,32591157,32591153,32592934"
   productPesIds="16094"
   cloudEnvironments="public,fairfax,blackforest,moonCake"
   schemaVersion="1"
   articleId="e7d714bd-eb61-42d8-8270-df52d8514149"
/>
# VPN Gateway Issues
---
{
    "resourceRequired": false,
    "formElements": [
        {   "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "Problem start time",
            "required": true
        },
        {   "id": "problem_description",
            "order": 2,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "hints": [{"text": "Issue description"},
                {"text": "Make, model and OS version of on-premises VPN device(s) (for example, \"Cisco ASA 5505 OS version 8.3\")"},
                {"text": "Upload your configuration file to speed the support process"},
                {"text": "For security purposes, please edit or remove the pre-shared key field from the configuration information"}]
        }
    ]
}
---
