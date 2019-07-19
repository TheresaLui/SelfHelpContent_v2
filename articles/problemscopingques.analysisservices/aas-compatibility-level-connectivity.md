 <properties
      articleId="B3D687A7-BD38-41AB-A06E-58B9C17E8F59"
      pageTitle="compatibility level"
      description="compatibility level"
      authors="pjfreitas"
      ms.author="pfreitas"
      selfHelpType="problemScopingQuestions"
      supportTopicIds="32675685"
      productPesIds="16157"
      cloudEnvironments="public, MoonCake, fairfax" 
      schemaVersion="1"
/>
# Compatibility level for Analysis Services tabular models
---
{
  "resourceRequired": false,
  "subscriptionRequired": true,
  "title": "Compatibility level for Analysis Services tabular models",
  "fileAttachmentHint":"",
  "formElements": 
  [
    {
      "id": "compatibility_level"
      "order": 100,
      "controltype": "multilinetextbox",
      "displaylabel":"What compatibility level are you attempting to use?",
      "watermarktext": "What compatibility level are you attempting to use?",
      "required": true,
      "useAsAdditionalDetails: true
    }
,
    {
      "id": "compatibility_level"
      "order": 200,
      "controltype": "Dropdown",
      "displaylabel":"Was this recently upgraded?",
      "watermarkText":"Choose an option","dropdownOptions":[{"value": "Yes","text": "Yes"},{"value": "No","text": "No"},{"value": "dont_know_answer","text":"Other, don't know or not applicable"}],
      "required": true,
      "useAsAdditionalDetails: true
    }
,
    {
      "id": "compatibility_level"
      "order": 300,
      "controltype": "multilinetextbox",
      "displaylabel":"What is the full error message with all error IDs?",
      "watermarktext": "What is the full error message with all error IDs?",
      "required": true,
      "useAsAdditionalDetails: true
    }
,
    {
      "id": "compatibility_level"
      "order": 400,
      "controltype": "Dropdown",
      "displaylabel":"Can the issue be reproduced by other users?",
      "watermarkText":"Choose an option","dropdownOptions":[{"value": "Yes","text": "Yes"},{"value": "No","text": "No"},{"value": "dont_know_answer","text":"Other, don't know or not applicable"}],
      "required: true,
      "useAsAdditionalDetails: true
    }
,
    {
      "id": "compatibility_level"
      "order": 500,
      "controltype": "Dropdown",
      "displaylabel":"Is this an intermittent or permanent issue?",
      "watermarkText":"Choose an option","dropdownOptions":[{"value": "Intermittent","text": "Intermittent"},{"value": "Permanent","text": "Permanent"},{"value": "dont_know_answer","text":"Other, don't know or not applicable"}],
      "required": true,
      "useAsAdditionalDetails: true
    }
  ],
    "$schema": "SelfHelpContent"
}
