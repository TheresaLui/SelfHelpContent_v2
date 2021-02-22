<properties
pageTitle="Port Scan Results For Load Balancer Resource."
description="Port Scan Results For Load Balancer Resource."
infoBubbleText="Port scan results for your load balancer resource. See details on the right."
service="microsoft.network"
resource="LoadBalancer"
authors="irenehua"
ms.author="irenehua"
displayOrder="10"
articleId="PortScanResults"
diagnosticScenario="PortScanResults"
selfHelpType="Diagnostics"
supportTopicIds="32436964,32436960,32582828,32582829,32582830,32582825,32582826,32582827,32582831,32582832,32436961,32573483,32582834,32436962,32565734,32565735,32565736,32582833"
resourceTags="windows"
productPesIds="16098"
cloudEnvironments="public, fairfax, usnat, ussec"
ownershipId="Cloudnet_NetworkWatcher"
/>
# Cannot connect to Virtual Machine because of blocked ports
<!--issueDescription-->
We have identified that your virtual machine(s), **'<!--$VMArray-->VMArray<!--/$VMArray-->'** have firewall or application issues blocking port(s) **'<!--$PortsArray-->PortsArray<!--/$PortsArray-->'**.
<!--/issueDescription-->

This issue is caused by a virtual machine (VM) application and/or firewall misconfiguration that is blocking network traffic to the application. By default, VM applications have to be configured to listen on particular TCP/UDP ports to receive requests from the networking layer. A firewall rule must also be configured to allow this traffic through. 

## **Recommended Steps**

### Windows

1. Determine if the application on the VM is listening on the expected port. Use PowerShell or the command prompt and enter the command: ***netstat -ano | findstr LISTENING | findstr [portNumber]*** where [portNumber] is the port number you expect the VM to be listening on. If you do not see any result, the application is not listening on that port and you should troubleshoot the application. If you see output like the following, you know the application is listening:

~~~powershell
C:\Users\username>netstat -ano | findstr LISTENING | findstr 3389
  TCP    0.0.0.0:3389           0.0.0.0:0              LISTENING       1540
  TCP    [::]:3389              [::]:0                 LISTENING       1540
~~~

In this example, we see that the application is listening on IPv4 which we know because the second column starts with 0.0.0.0. And, it is listening on IPv6, which we know because the second column is [::]. The last column is the Windows process (PID) of the network application.

2. Disable the firewall with powershell or manually check for blocking rules:

~~~powershell
netsh advfirewall set currentprofile state off
~~~

Manually check for blocking rules:

   1. Windows key, type 'Firewall', select 'Windows Defender Firewall with Advanced Security"
   2. Select 'Inbound Rules' in the left pane
   3. Sort the 'Action' column twice to show the 'Block' values at the top
   4. For each of the the 'Block' rules, review the 'Local Port' column or and the 'Program' column to identify any blocking rules for the customer port or application

### Linux

1. Determine if the application on the VM is listening. The Linux command is similar to Windows: ***netstat -ano | grep LISTEN | grep 22*** where 22 is the port number you expect the computer to be listening on. If you do not see any result, the application is not listening on that port and you should troubleshoot the application. If you see output like the following, you know the application is listening:

~~~bash
dave@tiger:~$ netstat -ano | grep LISTEN | grep 22
tcp        0      0 0.0.0.0:22              0.0.0.0:*               LISTEN      off (0.00/0/0)
tcp6       0      0 :::22                   :::*                    LISTEN      off (0.00/0/0)
~~~

Again, we can see that the application is running on IPv4 and IPv6.

2. Disable the firewall with bash or manually check for blocking rules with bash:

~~~bash
# /etc/init.d/iptables save
# /etc/init.d/iptables stop
~~~

3. Manually check for blocking rules:

~~~bash
sudo iptables -S
~~~

### Important!: Do not leave your firewall disabled. Enable your firewall again after testing.

## **Recommended Documents**

* https://docs.microsoft.com/azure/network-watcher/
* https://docs.microsoft.com/azure/network-watcher/diagnose-vm-network-traffic-filtering-problem
* https://docs.microsoft.com/azure/network-watcher/network-watcher-next-hop-overview
