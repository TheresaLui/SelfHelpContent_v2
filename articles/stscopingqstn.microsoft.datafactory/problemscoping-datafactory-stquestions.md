<properties
   pageTitle="Scoping questions for DataFactory issues"
   description="Scoping questions for DataFactory issues"
   authors="arthurw"
   selfHelpType="problemScopingQuestions"
   supportTopicIds="32452733,32356638,32605741,32605742,32592907,32605743,32356667,32356640,32356646,32356648,32356669,32356642,32356670,32605744,32605745,32356674,32605746,32356643,32605747,32356650,32605748,32356652,32356661,32356671,32605718,32605728,32605729,32605730,32605731,32605732,32605733,32605735,32605737,32356639,32356649,32356653,32356656,32592910,32356668,32605719,32605721,32605722,32605723,32605724,32605725,32605726,32605734,32605736,32605740,32605720,32605727,32605738,32605739"
   productPesIds="15613"
   cloudEnvironments="public"
   schemaVersion="1"
   articleId="f570457f-7a26-46cb-8033-541db1f03529"
/>
# DataFactory Issues
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
                    "text": "Factory region and version (V1 or V2)"
                },
                {
                    "text": "Error message(s)"
                },
                {
                    "text": "Authoring or scheduling issue?  Attach trigger/pipeline/dataset json"
                },
                {
                    "text": "Runtime issue? Specify runId, activity/source/target type, whether debug/sandbox run"
                },
                {
                    "text": "If delete failed or stuck in provisioning, do you authorize deletion from backend (yes/no)?"
                },
                {
                    "text": "UI issue?  Specify browser, whether in git mode, repro steps, attach screen shots/traces/logs"
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
    ]
}
---