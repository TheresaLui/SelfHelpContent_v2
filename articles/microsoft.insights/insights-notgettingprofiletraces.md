<properties
    pageTitle="I am not getting profiler traces"
    description="I am not getting profiler traces"
    service="microsoft.insights"
    resource="components"
    authors="brahmnes"
    displayOrder="40"
    selfHelpType="resource"
    productPesIds="15693"
    supportTopicIds="32602204"
    cloudEnvironments="public"
 />
# I am not getting profiler traces
## **Recommended steps**
To ensure that you are able to successfully get profiler traces:

1. Verify that the profiler is properly configured by following the steps in the article for your app type:
  * [Configure profiler for Azure Web Apps](https://go.microsoft.com/fwlink/?linkid=867935)
  * [Configure profiler for Azure VMs, Service Fabric, and Cloud Services](https://go.microsoft.com/fwlink/?linkid=867933)	
2. Verify the profiler traces can be [viewed](https://go.microsoft.com/fwlink/?linkid=867935#view-profiler-data) from the performance blade.<br>

The profiler doesn't collect traces 100% of the time due to resource and performance considerations.  For Azure Web Apps, the profiler can be [configured to run manually](https://go.microsoft.com/fwlink/?linkid=867935#profileondemand) which will collect traces for one fixed period of time.
<br><br>
If there are still issues with profiler after trying the steps above, run through the steps outlined [here](https://go.microsoft.com/fwlink/?linkid=867935#troubleshooting).<br>
## **Recommended documents**
[Profile live Azure web apps with Application Insights](https://go.microsoft.com/fwlink/?linkid=867935)<br>
[Enable Application Insights Profiler for Azure VMs, Service Fabric, and Cloud Services](https://go.microsoft.com/fwlink/?linkid=867933)
