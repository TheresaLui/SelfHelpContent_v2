<properties
          pageTitle="Robocopy"
          description="Robocopy"
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
          articleId="7fdb5635-5537-4361-967d-5d35853fa539"
           ownershipId="Centennial_CloudNet_LoadBalancer"
    />

# Robocopy

**Move data with Robocopy**

Robocopy is a well known copy tool that ships with Windows and Windows Server. 

Robocopy may be used to transfer data into Azure Files by mounting the file share locally and then using the mounted location as the destination in the Robocopy command.

Run this command: 
```dos
robocopy <source> <target> /mir /copyall /mt:16 /DCOPY:T
```

For more information on Robocopy commands, visit the following link: https://docs.microsoft.com/windows-server/administration/windows-commands/robocopy#syntax

<!---

questionAnswer
--

Question: 


**This is the end of the work flow. Did this TSG resolve your issue?**

Answers:

1: Yes

2: No

-->



