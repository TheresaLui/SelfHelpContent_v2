<properties
   pageTitle="Scoping questions for HDInsight Spark Issues"
   description="Scoping questions for HDInsight Spark Issues"
   authors="bharathb"
   selfHelpType="problemScopingQuestions"
   supportTopicIds="32511173"
  productPesIds="15078"
  cloudEnvironments="public, Fairfax, usnat, ussec"
   schemaVersion="1"
   articleId="c6ed4f84-9229-42a6-9adb-220a0d6acd12"
	ownershipId="AzureData_HDInsight"
/>
# HDInsight Spark Issues
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
                    "text": "How was the Spark job submitted? (Jupyter/Livy/Command Line)"
                },
                {
                    "text": "What is the programming language used? (PySpark/Scala)"
                },
                {
                    "text": "What Spark Components were in use? (Streaming, MLLib, SQL, GraphX)"
                },
                {
                    "text": "Details about executor and driver configuration (Number of cores, memory)"
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