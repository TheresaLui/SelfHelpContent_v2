<properties
	pageTitle="Microsoft Azure has information regarding your issue"
	description="Microsoft Azure has information regarding your issue"
	infoBubbleText="Microsoft Azure has information regarding your issue. Please see details to the right."
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="asgang"
	authoralias="asgang"
	displayOrder=""
	articleId="vmnotconnectingduetodnsissue"
	diagnosticScenario="vmnotconnectingduetodnsissue"
	selfHelpType="Diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="16370"
	cloudEnvironments="Public"
/>

# Your virtual machine is not able to access "login.microsoftonline.com" due to dns resolution failure
<!--issueDescription-->
Installation of mobility agent has failed, as a connection cannot be established to site recovery endpoints due to DNS resolution failure. This is more frequently seen during re-protection when you have failed over the virtual machine but the DNS server is not reachable from the DR region.
<!--/issueDescription-->

## **Recommended Steps**

- If you're using custom DNS, ensure the DNS server is accessible from the Disaster Recovery region
- To check if you have a custom DNS, go to the VM> Disaster Recovery network> DNS servers. Try accessing the DNS server from the virtual machine. If it is not accessible, then make it accessible by either failing over the DNS server or creating the line of site between DR network and DNS.
- [Troubleshoot Azure-to-Azure VM replication issues](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-troubleshoot-errors#outbound-connectivity-for-site-recovery-urls-or-ip-ranges-error-code-151037-or-151072) 

## **Recommended Documents**

* Learn more about [Azure VM disaster Recovery connectivity requirements](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-about-networking#outbound-connectivity-for-ip-address-ranges)
* Learn more about troubleshooting [connectivity failures](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-troubleshoot-errors#outbound-connectivity-for-site-recovery-urls-or-ip-ranges-error-code-151037-or-151072)
