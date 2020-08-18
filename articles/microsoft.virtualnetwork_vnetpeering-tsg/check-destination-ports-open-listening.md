<properties
	pageTitle="TSG Content Step: Check Destination Ports Open and Listening"
	description="TSG Content Step: Check Destination Ports Open and Listening"
	service="microsoft.network"
	ownershipid="Centennial_Cloudnet_VirtualNetwork"
	resource="virtualnetwork"
	authors="chadmath"
	ms.author="chadmat"
	selfHelpType="TSG_Content"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="c4d32956-f745-4d2a-b9ce-f2de7c9d690e"
/>
# Check Destination Ports Open and Listening

In order for an Azure VM to respond to a network request, an application on the VM must be listening on that specific port and the OS firewall must allow access on that port.  This guide will show you how to check for these requirements on both the Windows and Linux VMs.

## **Recommended Steps**

***Windows***

1. Determine if the application on the VM is listening. Use the command netstat -ano | findstr LISTENING | findstr 3389 where 3389 is the port number you expect the computer to be listening on. If you do not see any result, the application is not listening on that port and you should troubleshoot the application. If you see output like the following, you know the application is listening:

~~~powershell
C:\Users\dgoddard>netstat -ano | findstr LISTENING | findstr 3389
  TCP    0.0.0.0:3389           0.0.0.0:0              LISTENING       1540
  TCP    [::]:3389              [::]:0                 LISTENING       1540
~~~

In this example, we see that the application is listening on IPv4 which we know because the second column starts with 0.0.0.0. And, it is listening on IPv6, which we know because the second column is [::]. The last column is the Windows process (PID) of the network application.

2. Disable the firewall with powershell or manually check for blocking rules

~~~powershell
netsh advfirewall set currentprofile state off
~~~

Manually check for Blocking rules

   1. Windows key, type 'Firewall', select 'Windows Defender Firewall with Advanced Security"
   2. Select 'Inbound Rules' in the left pane
   3. Sort the 'Action' column twice to show the 'Block' values at the top
   4. For each of the the 'Block' rules, review the 'Local Port' column or and the 'Program' column to identify any blocking rules for the customer port or application


***Linux***

1. Determine if the application on the VM is listening. The Linux command is similar to Windows: netstat -ano | grep LISTEN | grep 22 where 22 is the port number you expect the computer to be listening on. If you do not see any result, the application is not listening on that port and you should troubleshoot the application. If you see output like the following, you know the application is listening:

~~~bash
dave@tiger:~$ netstat -ano | grep LISTEN | grep 22
tcp        0      0 0.0.0.0:22              0.0.0.0:*               LISTEN      off (0.00/0/0)
tcp6       0      0 :::22                   :::*                    LISTEN      off (0.00/0/0)
~~~

Again, we can see that the application is running on IPv4 and IPv6.

2. Disable the firewall with bash or manually check for blocking rules with bash

~~~bash
# /etc/init.d/iptables save
# /etc/init.d/iptables stop
~~~

Manually check for blocking rules

~~~bash
sudo iptables -S
~~~


