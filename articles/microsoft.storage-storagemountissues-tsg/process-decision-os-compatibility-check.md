<properties pageTitle="Check for OS compatibility"
            description="Check for OS compatibility"
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
            articleId="949b4bdc-82e7-479b-b370-f34e860a3354"
            ownershipId="Centennial_CloudNet_LoadBalancer" />


# Check for OS compatibility

**How to check for OS compatibility**

1. **Windows:** To mount an Azure file share outside of the Azure region it is hosted in, such as on-premises or in a different Azure region, the client's OS must support SMB 3.0 with encryption

        Check the following table to see if the client that you used to mount the file share supports SMB 3.0

2. **Linux:** To mount an Azure file share outside of the Azure region it is hosted in, such as on-premises or in a different Azure region, the clients OS must support SMB 3.0 with encryption

        SMB 3.0 encryption support was introduced in Linux kernel version 4.11

**Client: SMB Version Supported Table**

1. Windows Server 2008 R2: SMB 2.1 (access only from VM in same region as share)
2. Windows 7: SMB 2.1 (access only from VM in same region as share)
3. Windows Server 2012: SMB 3.0
4. Windows Server 2012 R2: SMB 3.0
5. Windows 8.1: SMB 3.0
6. Windows 10 (versions 1507, 1607, 1703, and 1709.): SMB 3.0
7. Windows Server 2016: SMB 3.0
8. Windows Server Semi-Annual Channel (version 1709): SMB 3.0
9. Ubuntu Server 14.04+: SMB 2.1 and 3.0
10. CentOS 7+: SMB 2.1 and 3.0
11. Open SUSE 13.2+: SMB 2.1 and 3.0
12. SUSE Linux Enterprise Server 12+: SMB 2.1 and 3

<!---

---

**This is the end of the work flow. Did this TSG resolve your issue?**

1. Yes
2. No

-->