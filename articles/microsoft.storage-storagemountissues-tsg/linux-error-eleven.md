<properties pageTitle="Mount error(11) 'resource temporarily unavailable' when you try to mount the share from Linux"
            description="Mount error(11) 'resource temporarily unavailable' when you try to mount the share from Linux"
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
            articleId="3fc82f0c-93ba-45bf-9e8a-f673aed756b1"
            ownershipId="Centennial_CloudNet_LoadBalancer" />

# Mount error(11) 'resource temporarily unavailable' when you try to mount the share from Linux

This issue specially been seen on Ubuntu 16.10

**Cause**

1. Known issue in Ubuntu 16.10 kernel (v.4.8) where the client claims to support encryption
2. However, it does not

**Resolution**

Until Ubuntu 16.10 is fixed, try use Ubuntu 16.04 or specify SMB version 2.1 instead of SMB version 3.0 with the vers=2.1 when mounting the share

Example:

```bash
sudo mount -t cifs //.file.core.windows.net/  -o vers=2.1,username=,password=,dir_mode=0777,file_mode=0777,serverino
```

<!---

---

**This is the end of the work flow. Did this TSG resolve your issue?**

1. Yes
2. No

-->