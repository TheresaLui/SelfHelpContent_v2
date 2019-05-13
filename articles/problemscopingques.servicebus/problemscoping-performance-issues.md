<properties
    pageTitle="Performance and Latency issues"
    description="Performance and Latency issues"
    service="microsoft.servicebus"
    resource="errorMessageTypes"
    authors="mksuni"
    ms.author="mksuni"
    displayOrder=""
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32633389"
    resourceTags=""
    productPesIds="13186"
    cloudEnvironments="public"
    articleId="sb-performance-issue"
    schemaVersion="1"
/>
#Performance and Latency Issues
---
{  
   "subscriptionRequired":true,
   "title":"Performance and Latency issues",
   "fileAttachmentHint":"",
   "formElements":[  
      {  
         "id":"problem_start_time",
         "order":1,
         "controlType":"datetimepicker",
         "displayLabel":"When did the problem begin?",
         "required":true
      },
      {  
         "id":"problem_requestInfo",
         "order":2,
         "controlType":"multilinetextbox",
         "displayLabel":"What request(s) is(are) having a latency issue?",
         "watermarkText":"Enter the request URL",
         "required":true
      },
      {  
         "id":"problem_currentLatency",
         "order":3,
         "controlType":"textbox",
         "displayLabel":"Provide current latency of the request(s)",
         "required":true
      },
      {  
         "id":"problem_expectedLatency",
         "order":4,
         "controlType":"textbox",
         "displayLabel":"Provide the expected latency of the request(s)",
         "required":true
      },
      {  
         "id":"problem_LocationOfClient",
         "order":5,
         "controlType":"textbox",
         "displayLabel":"What's the location of client experincing performance issue (for e.g. OnPrem, On Azure, Region etc)",
         "required":true
      },
      {  
         "id":"problem_description",
         "order":6,
         "controlType":"multilinetextbox",
         "displayLabel":"Details",
         "watermarkText":"Provide additional information about your issue",
         "required":true,
         "useAsAdditionalDetails":true,
         "hints":[  
            {  
               "text":"Issue description."
            }
         ]
      }
   ]
}
---

