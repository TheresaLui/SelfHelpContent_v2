<properties
pageTitle="RDP Licensing"
description="RDP Licensing"
infoBubbleText="RDP License grace period expired"
service="microsoft.compute"
resource="virtualmachines"
authors="manavis"
displayOrder=""
articleId="vmhealthsignal_57876450-c7df-4f23-8aea-a34797fe7e2d"
diagnosticScenario="RDP Licensing"
selfHelpType="diagnostics"
supportTopicIds="32411835"
resourceTags="windows"
productPesIds="14749"
cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>

# RDS licensing grace period expired
<!--issueDescription-->
Grace period of RDS Client Access Licenses required to RDP has expired

Please check for following symptoms:
1. Upon accessing the VM via below error is seen:<br>
    `The remote session was disconnected because there are no remote desktop license servers available to provide a license`

3. If use an administrative session `mstsc /admin`, you are able to log-in.
<!--/issueDescription-->

## **Recommended Steps - Internal**
Please refer to the [internal article](https://www.csssupportwiki.com/index.php/curated:Azure/Virtual_Machine/Can’t_RDP-SSH/TSG/VM_Responding_Bucket/There%27s_any_RDLicense_server_available_to_start_the_session) to RCA and view mitigation steps in detail.

**Root Cause Analysis 1**

The Remote Desktop License server is unreachable to provide any license to start a session. This could happened in different scenarios:

1. The Cx has setup RDSession Host role on the machine, never deployed an RDLicense role on the environment and the grace pediod (180 days) is over.<br>

2. The Cx has setup RDSession Host role on the machine, installed an RDLicense on the environment but never activated <br>

3. The Cx has setup RDSession Host role on the machine, and the RDLicense on the environment doesn't have CALs injected to setup the connection <br>

4. The Cx has setup RDSession Host role on the machine, the RDLicense was installed on the environment, there are available CALs to give away but the Cx has never setup the awareness to the environment where to look for those CALS <br>

5. The Cx has setup RDSession Host role on the machine, and the RDLicense has CALs but is having some problem that is preventing to issue the licenses on the environment <br>

**Root Cause Analysis 2**

Windows Remote Desktop Service allows two concurrent remote administrative connections through the Windows built-in RDP which do not consume RD licenses.

However, any connection through third party RDS protocol (for example, Citrix XenApp RDP proxy protocol extension) consumes a RD license, even though the connection is made using `mstsc /admin`.

This is by design with Citrix XenApp using their own RDS protocol.
