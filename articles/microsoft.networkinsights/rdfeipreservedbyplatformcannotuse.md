<properties
pageTitle="Classic VM and VNet Management Error The address IpAddress is reserved by the platform and cannot be used"
description="Classic VM and VNet Management Error The address IpAddress is reserved by the platform and cannot be used"
infoBubbleText="Classic VM and VNet Management Error The address IpAddress is reserved by the platform and cannot be used"
service="microsoft.classiccompute, microsoft.classicnetwork"
resource="ClassicVirtualMachine, ClassicVirtualNetwork"
authors="aconkle"
ms.author="aconkle"
displayOrder="10"
articleId="RdfeIpReservedByPlatformCannotUse"
diagnosticScenario="RdfeIpReservedByPlatformCannotUse"
selfHelpType="Diagnostics"
supportTopicIds="b25271d3-6431-dfbc-5f12-5693326809b3, 98e5cec8-2650-28c1-92e8-0ecaa232eec0, cddd3eb5-1830-b494-44fd-782f691479dc, de8937fc-74cc-daa7-2639-e1fe433dcb87, 722ccc66-c988-d2ac-1ec6-b7aebc857f2d, 2340ae8b-c745-572f-6ea8-661d68c08bd7, 6f16735c-b0ae-b275-ad3a-03479cfa1396"
resourceTags="windows"
productPesIds="15526, 14749, 16470, 16454, 15797, 15571, 16065, 16215"
cloudEnvironments="Public, Fairfax, usnat, ussec"
ownershipId="Compute_ComputePlatform"
/>
# Classic VM and VNet Management Error The address IpAddress is reserved by the platform and cannot be used
<!--issueDescription-->
Customers were unable to make any service management operations on a subset of classic Virtual Networks. Customers would have received error The address IpAddress is reserved by the platform and cannot be used.
<!--/issueDescription-->

### Root Cause

This root cause of this issue is due to a recent change in a networking configuration subsystem used in Azure. The change introduced a check that prevented invalid subnet prefixes used in Virtual Networks and subnets. For example, a subnet may be configured as CIDR prefix 10.0.0.1/24 instead of the proper 10.0.0.0/24. Because of this check, existing Virtual Networks provisioned as invalid CIDR prefixes will fail any configuration changes. This only affects classic Virtual Networks, and there is no communication or data path impact.

### Next Steps

Microsoft is manually updating Virtual Network configurations to proper CIDR prefix for any affected customers to unblock
Microsoft is developing a code fix for this regression
Microsoft is developing internal alerting to quickly identify issues such as these going forward
