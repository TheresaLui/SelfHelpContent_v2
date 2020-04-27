<properties
	pageTitle="Check if a port is listening and firewall is open"
	description="Check if a port is listening and firewall is open"
	service="microsoft.network"
	resource="loadBalancers"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds="32588977"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="3e0e741d-d045-4442-bcb5-54e1c69f068d"
	ownershipId="CloudNet_LoadBalancer"
/>

# How to check if a port is listening and OS firewall is open

In order for a network computer (or Azure VM) to respond to a particular network request, it must be listening on a specific port and the OS firewall must allow access.  This guide will show you how to do so on both the Windows and Linux operating systems.

## **Recommended Steps**

1. Use the host-to-guest port scanner diagnostic in ASC > Resource Explorer > SLB > Scan Backend Pool VM
2. Or manually if #1 above doesn't work

**Windows**

Use the command netstat -ano | findstr LISTENING | findstr 3389 where 3389 is the port number you expect the computer to be listening on. If you do not see any result, the application is not listening on that port and you should troubleshoot the application. If you see output like the following, you know the application is listening:

~~~powershell
C:\Users\dgoddard>netstat -ano | findstr LISTENING | findstr 3389
  TCP    0.0.0.0:3389           0.0.0.0:0              LISTENING       1540
  TCP    [::]:3389              [::]:0                 LISTENING       1540
~~~

In this example, we see that the application is listening on IPv4 which we know because the second column starts with 0.0.0.0. And, it is listening on IPv6, which we know because the second column is [::]. The last column is the Windows process (PID) of the network application.

**Linux**

The Linux command is similar to Windows: netstat -ano | grep LISTEN | grep 22 where 22 is the port number you expect the computer to be listening on. If you do not see any result, the application is not listening on that port and you should troubleshoot the application. If you see output like the following, you know the application is listening:

~~~bash
dave@tiger:~$ netstat -ano | grep LISTEN | grep 22
tcp        0      0 0.0.0.0:22              0.0.0.0:*               LISTEN      off (0.00/0/0)
tcp6       0      0 :::22                   :::*                    LISTEN      off (0.00/0/0)
~~~

Again, we can see that the application is running on IPv4 and IPv6.

**Windows Verify the OS firewall is allowing traffic**

1. Disable the firewall

~~~powershell
netsh advfirewall set  currentprofile state off
~~~

1. Manually check for Blocking rules
   1. Windows key, type 'Firewall', select 'Windows Defender Firewall with Advanced Security"
   2. Select 'Inbound Rules' in the left pane
   3. Sort the 'Action' column twice to show the 'Block' values at the top
   4. For each of the the 'Block' rules, review the 'Local Port' column or and the 'Program' column to identify any blocking rules for the customer port or application

**Linux Verify the OS firewall is allowing traffic**

1. Disable the firewall

~~~bash
# /etc/init.d/iptables save
# /etc/init.d/iptables stop
~~~

1. Manually check for blocking rules

~~~bash
sudo iptables -S
~~~

***Important Note:*** Ensure the firewall is turned back on once the test is over and the individual port has been opened.
