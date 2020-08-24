<properties pageTitle="The command Net Use or New-SmbMapping runs successfully but no folder with a drive letter in My Computer"
            description="The command Net Use or New-SmbMapping runs successfully but no folder with a drive letter in My Computer"
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
            articleId="5db3eb95-6818-4e48-a97f-44e5611a5622"
            ownershipId="Centennial_CloudNet_LoadBalancer" />

# The command Net Use or New-SmbMapping runs successfully but no folder with a drive letter in My Computer

**Cause**

1. By default, Windows File Explorer does not run as an administrator
2. If you run net use from an administrative command prompt, you map the network drive as an administrator
3. Because mapped drives are user-centric, the user account that is logged in does not display the drives if they are mounted under a different user account

**Resolution 1**

Mount the share from a non-administrator command line

**Resolution 2**

Alternatively, you can follow this TechNet topic to configure the [EnableLinkedConnections](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/ee844140(v%3Dws.10)) registry value. To work around this problem, configure the EnableLinkedConnections registry value. This value enables Windows Vista and Windows 7 to share network connections between the filtered access token and the full administrator access token for a member of the Administrators group. After you configure this registry value, LSA checks whether there is another access token that is associated with the current user session if a network resource is mapped to an access token. If LSA determines that there is a linked access token, it adds the network share to the linked location.

To configure the EnableLinkedConnections registry value

1. Click Start, type regedit in the search programs and files box, and then press ENTER
2. Locate and then right-click the registry subkey **HKEY_LOCAL_MACHINE>SOFTWARE>Microsoft>Windows>CurrentVersion>Policies>System**
3. Point to New, and then click DWORD Value
4. Type EnableLinkedConnections, and then press ENTER
5. Right-click EnableLinkedConnections, and then click Modify
6. In the Value data box, type 1, and then click OK
7. Exit Registry Editor, and then restart the computer

**Recommended Documents**

More info: [https://docs.microsoft.com/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/ee844140(v=ws.10)](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/ee844140(v=ws.10))

<!---

---
**This is the end of the work flow. Did this TSG resolve your issue?**
1. Yes
2. No

-->
