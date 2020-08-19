<properties
    pageTitle="Security Configuration Common Solutions"
    description="Security Configuration Common Solutions"
    service=""
    resource=""
    authors="TobyTu"
    ms.author="jaserano"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32680782"
    resourceTags=""
    productPesIds="15947"
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="a15f058d-8uj6-4b77-a98a-dfaf3843dc2f"
	ownershipId="Azure_Security_Security_Center"
/>

# Operating System Security Configurations Common Solutions

Azure Security Center monitors security configurations by applying a set of [over 150 recommended rules](https://gallery.technet.microsoft.com/Azure-Security-Center-a789e335) for hardening the OS, including rules related to firewalls, auditing, password policies, and more. If a machine is found to have a vulnerable configuration, Security Center generates a security recommendation.

The latency in Security Center scans for vulnerabilities, updates, and issues is:

- Operating system security configurations data is updated within 48 hours

## **Recommended Steps**

Troubleshoot false positive security configuration ( baseline) rule:

1. Open the recommendation "Remediate vulnerabilities in security configuration on your machines"
2. Select the rule that shows you incorrect results
3. Click View for affected computer
4. Open the log analytics workspace and search page for the affected VM, then connect it
5. Run this query

   Replace the CceId to the failed RuleID. And add your subscription ID to the query:

   ```/
   SecurityBaseline
   | where AnalyzeResult == "Failed"
   | where CceId == "AZ-WIN-00119"
   | where tolower(SubscriptionId) in ("2fa14ce2-xxxx-xxxx-baa5-6bb370737216") or isemp (SubscriptionId)
   ```

6. Expand one of the results and compare the expected value against the actual result with the rule operation.
7. Connect to the affected VM, and examine the actual result on the VM registry file or log location.

## **Recommended Documents**

- [Azure Security Center Common Configuration Identifiers and Baseline Rules v4](https://gallery.technet.microsoft.com/Azure-Security-Center-a789e335)
- [Azure resources are monitored by Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-faq#how-often-does-security-center-scan-for-operating-system-vulnerabilities-system-updates-and-endpoint-protection-issues)

**Troubleshooting**

- [ASC Troubleshooting Guide](https://docs.microsoft.com/azure/security-center/security-center-troubleshooting-guide)

**FAQ**

- [ASC FAQ](https://docs.microsoft.com/azure/security-center/security-center-faq)
