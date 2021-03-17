<properties
  pagetitle="Security Recommendations (Baseline)"
  ms.author="kawilson,elsagie"
  selfhelptype="Generic"
  supporttopicids="32749420"
  resourcetags=""
  productpesids="15947"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="6bc4e686-7ac5-4850-80dc-ac801cf2bee5"
  ownershipid="Azure_Security_Security_Center" />
# Security Recommendations (Baseline)

### Operating System Security Configurations Common Solutions

Azure Security Center monitors security configurations by applying a set of [over 150 recommended rules](https://github.com/MicrosoftDocs/SecurityBenchmarks/tree/master/Secure%20Compute%20Baselines) for hardening the OS, including rules related to firewalls, auditing, password policies, and more. If a machine is found to have a vulnerable configuration, Security Center generates a security recommendation.

The latency in Security Center scans for vulnerabilities, updates, and issues is:
- Operating system security configurations data is updated within 48 hours

### **Recommended Steps**

Troubleshoot the false positive security configuration (baseline) rule:
1. Open the recommendation "Remediate vulnerabilities in security configuration on your machines"
2. Select the rule that shows you incorrect results
3. Click **View** for affected computer
4. Open the log analytics workspace and search page for the affected VM, then connect it
5. Run this query

   Replace the BaselineRuleId to the failed RuleID. And add your subscription ID to the query:

   ```/
	SecurityBaseline
	| where ( BaselineRuleId =~ "babda20b-1bc0-4204-9745-0cd584dcbb2b" )
	| where tolower(SubscriptionId) in ("2fa14ce2-xxxx-xxxx-baa5-6bb370737216") or isempty(SubscriptionId)
	| project TimeGenerated,BaselineType,Resource,ActualResult,ExpectedResult,AnalyzeResult
   ```

6. Expand one of the results and compare the expected value against the actual result with the rule operation
7. Connect to the affected VM, and examine the actual result on the VM registry file or log location

## **Recommended Documents**

- [Azure Security Center Common Configuration Identifiers and Baseline Rules v4](https://github.com/MicrosoftDocs/SecurityBenchmarks/tree/master/Secure%20Compute%20Baselines)
- [Azure resources are monitored by Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-faq#how-often-does-security-center-scan-for-operating-system-vulnerabilities-system-updates-and-endpoint-protection-issues)

### Troubleshooting
* [ASC Troubleshooting Guide](https://docs.microsoft.com/azure/security-center/security-center-troubleshooting-guide)

### FAQ
* [ASC FAQ](https://docs.microsoft.com/azure/security-center/security-center-faq)
