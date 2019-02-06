<properties
pageTitle="DDoS Attack was detected and has been mitigated for Public IP resource"
description="DDoS Attack was detected and has been mitigated for Public IP resource"
infoBubbleText="DDoS Attack was detected and has been mitigated for Public IP resource."
service="microsoft.networkinsights"
resource="DDoS"
authors="alhow"
displayOrder="10"
articleId="DDoSProtectionPlanMitigationDetected"
diagnosticScenario="Customer is onboarded to DDoS Standard and creates a case for an attack already mitigated."
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public"
/>
# Customer is onboarded to DDoS Standard and creates a case for an attack already mitigated
<!--issueDescription-->
DDoS Attack was detected and has been mitigated for Public IP resource. <br>


### **Impacted Resources**
Public IP resource(s) that were mitigated are:​ <!--$List of Public IPs-->[**AffectedIps**]<!--/$List of Public IPs-->
<!--/issueDescription-->

#
### **Recommended Action**
The Public IP resources listed above has been mitigated. Check the status of the resource in the [dashboard](https://InsertDashboardLinkHere) in Resource Explorer for this resource. If this IP is getting mitigated correctly, inform the customer accordingly . Otherwise create a Sev 2 Incident (CRI) with Owning Service = Cloudnet ; Owning Team = DDoS with the details of the attack , Public IP resource, **Subscription ID:** [SubscriptionID], **Region:** [Regions] and **Case ID:** [CaseID].​

#
### **Customer Ready Content** 
The Public IP resources that were/are under mitigation: <!--$List of Public IPs-->[**AffectedIps**] <!--/$List of Public IPs--> 
<br>

Please review metrics in Azure Monitor. ​ 