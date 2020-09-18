<properties
pageTitle="DDoS Attack wasn't detected and mitigated for Public IP resource"
description="DDoS Attack wasn't detected and mitigated for Public IP resource"
infoBubbleText="DDoS Attack wasn't detected and mitigated for Public IP resource."
service="microsoft.networkinsights"
resource="DDoS"
authors="alhow"
ms.author="alhoward"
displayOrder="10"
articleId="DDoSStdNoMitigationDetected"
diagnosticScenario="Customer is onboarded to DDoS Standard and creates a case for an ongoing attack for public IP."
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="CloudNet_AzureDDoSProtection"
/>
# Customer is Onboarded to DDoS Standard and Creates a Case for an Ongoing Attack for Public IP
<!--issueDescription-->
DDoS Attack wasn't detected and mitigated for Public IP resource

Public IP resources that were mitigated are : <!--$List of Public IPs-->[AffectedIps]<!--/$List of Public IPs-->
<!--/issueDescription-->

## **Recommended Steps**

Check the status of the resource in the [dashboard](DashboardLink) in Resource Explorer for this resource. If this IP is getting mitigated correctly, inform the customer. Otherwise create a Sev 2 Incident (CRI) with Owning Service = Cloudnet ; Owning Team = DDoS with the details of the attack , Public IP resource, **Subscription ID:** [SubscriptionID], **Region:** [Regions] and **Case ID**: [CaseID].


### **Customer Ready Content**

Investigation ongoing for the below Public IP resources under mitigation: <!--$List of Public IPs-->[AffectedIps]<!--/$List of Public IPs-->

Please review metrics in Azure Portal / Azure Monitor.
