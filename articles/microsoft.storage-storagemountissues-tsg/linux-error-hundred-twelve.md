<properties pageTitle="Mount error(112) 'Host is down'"
            description="Mount error(112) 'Host is down'"
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
            articleId="8d073b95-0ab7-4ffc-8acc-8d65003234f7"
            ownershipId="Centennial_CloudNet_LoadBalancer" />

# Mount error(112) 'Host is down'

Error on existing file shares, you lose access to the share, or the shell hangs when running list commands on the mount point or even when trying to mount for first time

**Possible Causes**

1. This error occurs on the Linux client when the client has been idle for an extended period. When the client is idle for long time, the client disconnects, and the connection times out. The connection can be idle because of various reasons. One reason being network communication failures that prevent reestablishing a TCP connection to the server when soft mount option is used, which is the default.
2. Reconnect fixes which are not present in older Linux kernels
3. New connection Scenario: If you are trying to mount Azure file share fails on Linux for the first time and received the error please check if the Linux distribution is supported. *Note: Customer have reported this issue with Older version of SUSE 11 and older which may see issues connecting to Azure file share using SMB 2.1 or 3*
    1. Ubuntu Server 14.04+
    2. RHEL 7+
    3. CentOS 7+
    4. Debian 8+
    5. OpenSUSE 13.2+
    6. SUSE Linux Enterprise Server 12


**Resolution for existing shares:**

1. Specifying a hard mount will force the client to wait until a connection is established or until explicitly interrupted, and can be used to prevent errors caused by network timeouts
2. However, users should be aware that this could lead to indefinite waits and should handle halting a connection as needed
3. The following change sets fix this reconnect issue now in Linux kernel: (get Linux SME assistance if needed)
	1. [Fix reconnect to not defer smb3 session reconnect long after socket reconnect](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/fs/cifs?id=4fcd1813e6404dd4420c7d12fb483f9320f0bf93)
    2. [Call echo service immediately after socket reconnect](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=b8c600120fc87d53642476f48c8055b38d6e14c7)
    3. [CIFS: Fix a possible memory corruption during reconnect](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=53e0e11efe9289535b060a51d4cf37c25e0d0f2b)
    4. [CIFS: Fix a possible double locking of mutex during reconnect - for kernels v4.9 and higher](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=96a988ffeb90dba33a71c3826086fe67c897a183)

4. However this change may not be ported to all the Linux distributions yet
5. This is the list of known popular Linux kernels that have this and other reconnect fixes: 4.4.40+ 4.8.16+ 4.9.1+
6. You can move to the above recommended kernel versions in order to obtain the latest fix

**Workaround**

1. If you are unable to move to latest kernel versions, to work around this issue, keep a file in the Azure File share that you write to every 30 seconds or less
2. This has to be a write operation, such as rewriting the created or changed date on the file
3. Otherwise, you might receive cached results, and your operation might not trigger the re-connection
	1. Remount the share before you use it
    2. Create a cron job to make some data transfer with the following value:

        ```bash
        **/1 * * * * date>/mnt/MountPointName/time
        ```

4. It will update OS time every minute to a file on the share. The information can also be useful to identify the Last Known Good time for share accessibility.

**Resolution for mounting first time**

Please ask customer to use Supported version of the Linux Distribution mentioned above

<!---

---
**This is the end of the work flow. Did this TSG resolve your issue?**

1. Yes
2. No

-->