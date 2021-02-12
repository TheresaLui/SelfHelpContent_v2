<properties pageTitle="Check Proxy or NAT"
            description="Check Proxy or NAT"
            service="Microsoft.Storage"
            resource="Microsoft.Storage/storageAccounts"
            authors="akshaymatmicrosoft"
            ms.author="akshaym"
            displayOrder=""
            selfHelpType="TSG_Content"
            supportTopicIds=""
            resourceTags=""
            productPesIds=""
            cloudEnvironments="public, fairfax, usnat, ussec"
            articleId="b421498e-4148-4dd2-a40e-54729ac00783"
            ownershipId="Centennial_CloudNet_LoadBalancer" />


# Check Proxy or NAT

1. Customer have a proxy or any other kind of NAT device in his Local Network, that is blocking the connection from On-Prem to Azure for map the Azure File Share
2. Use the storage account user for copying the files:
	1. Customer needs to add the IP Address for the Storage Account or range (x.x.x.0/24) in the proxy or NAT device
    2. On elevated cmdline: ipconfig /flushdns & ipconfig /registerdns
    3. Control Panel -> Administrative Tools -> Local Security Policy
    4. Under Security Settings -> Local Policies -> Security Options Set Microsoft network client: Digitally sign communications: Disable {Enabled by default}

<!---

---
**This is the end of the work flow. Did this TSG resolve your issue?**

1. Yes
2. No

-->