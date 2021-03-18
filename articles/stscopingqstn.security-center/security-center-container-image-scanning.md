<properties
  pagetitle="Vulnerability Assessment - Container image scanning (ACR) self help guide"
  ms.author="elsagie"
  selfhelptype="Generic"
  supporttopicids="32749414"
  resourcetags=""
  productpesids="15947"
  cloudEnvironments="public, fairfax, usnat, ussec"
  articleid="6bc4e686-7ac5-4850-80dc-ac806cf2bee5"
  ownershipid="Azure_Security_Security_Center" />
# Vulnerability Assessment - Container image scanning (ACR) self help guide
### ASC Container image scan results are missing / image was not scanned

If you pushed a container image into an ACR registry and do not find scan results in Security Center under the "Vulnerabilities in Azure Container Registry images should be remediated (powered by Qualys)" ASC recommendation:
1. Verify the registry is under a subscription which is onboarded to Azure Defender for container registries  
To verify: 
   - From Security Center's menu, select Pricing & Settings
   - Select the relevant subscription
   - Look for Container registries in Azure Defender Plans and make sure it is on   
2. Make sure the image and registry types are included in the [Availability section](https://docs.microsoft.com/azure/security-center/defender-for-container-registries-usage)

### Extracting container image scan results 
You can image scan results via REST API. The results are under [Sub-Assessments Rest API](https://docs.microsoft.com/rest/api/securitycenter/subassessments/list). Also, you can use [Azure Resource Graph (ARG)](https://docs.microsoft.com/azure/governance/resource-graph), the Kusto-like API for all of your resources: a query can fetch a specific scan and aggregate them.  

Example query for extracting scanned images summary using [ARG resources REST API](https://docs.microsoft.com/en-us/rest/api/azureresourcegraph/resourcegraph(2019-04-01)/resources/resources), [ARG PowerShell module](https://docs.microsoft.com/azure/governance/resource-graph/first-query-powershell) or [Resource Graph Explorer](https://docs.microsoft.com/azure/governance/resource-graph/first-query-portal), you can use this query:
  
```
securityresources
 | where type == "microsoft.security/assessments/subassessments"
 | where id matches regex  "(.+?)/providers/Microsoft.Security/assessments/dbd0cb49-b563-45e7-9724-889e799fa648/"
 | extend registryResourceId = tostring(split(id, "/providers/Microsoft.Security/")[0])
 | extend imageDigest = tostring(properties.additionalData.imageDigest), repository = tostring(properties.additionalData.repositoryName)
 | extend scanFindingSeverity = tostring(properties.status.severity), scanStatus = tostring(properties.status.code)
 | summarize scanFindingSeverityCount = count() by scanFindingSeverity, scanStatus, registryResourceId, repository, imageDigest
 | summarize  severitySummary = make_bag(pack(scanFindingSeverity, scanFindingSeverityCount)) by registryResourceId, repository, imageDigest, scanStatus
```  

## **Recommended Documents**
- [Use Azure Defender for container registries to scan your images for vulnerabilities](https://docs.microsoft.com/azure/security-center/defender-for-container-registries-usage)
- [Container security in Security Center](https://docs.microsoft.com/azure/security-center/container-security)
- [Introduction to Azure Defender for container registries](https://docs.microsoft.com/azure/security-center/defender-for-container-registries-introduction)
- [Enable Azure Defender](https://docs.microsoft.com/azure/security-center/security-center-pricing#enable-azure-defender)
- [Exporting Azure Container Registry Vulnerability Assessment in Azure Security Center](https://techcommunity.microsoft.com/t5/azure-security-center/exporting-azure-container-registry-vulnerability-assessment-in/ba-p/1255244)
- [Continuously export security findings from vulnerability assessment solution recommendations](https://techcommunity.microsoft.com/t5/azure-security-center/continuously-export-security-findings-from-vulnerability/ba-p/1640691)

### Troubleshooting
* [ASC Troubleshooting Guide](https://docs.microsoft.com/azure/security-center/security-center-troubleshooting-guide)

### FAQ
* [ASC FAQ](https://docs.microsoft.com/azure/security-center/security-center-faq)
