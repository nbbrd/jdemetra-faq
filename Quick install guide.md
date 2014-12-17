#Quick Install Guide

This guide provides basic installation instructions of **JDemetra+** for users.

##System requirements

JDemetra+ runs on operating systems that support the Java VM (Virtual Machine) such as:

* Microsoft **Windows**
* **Ubuntu**
* **Solaris** OS
* Macintosh **OS X** 

JDemetra+ should also run on the various other Linux distributions.

##Required software

JDemetra+ runs on the **Java SE Runtime Environment (JRE) version 7 update 25 or later**. You can download the JRE for your platform at [http://www.oracle.com/technetwork/java/javase/downloads](http://www.oracle.com/technetwork/java/javase/downloads).

##Installation instructions

1. Download the platform-independent zip package at:  
   [https://joinup.ec.europa.eu/nexus/content/repositories/releases](https://joinup.ec.europa.eu/nexus/content/repositories/releases/eu/europa/ec/joinup/sat/nbdemetra-app/1.5.4/nbdemetra-app-1.5.4.zip)
2. Extract it to any folder on your system
3. Run the executable file located in the nbdemetra/bin directory:  
   `nbdemetra.exe` for Windows  
   `$ ./nbdemetra` for Linux, Solaris and Mac OS X

##Troubleshooting

If the launching of JDemetra+ fails, you can try the following operations:

1. Check if Java SE Runtime Environment (JRE) is properly installed by typing in the following command in a terminal: `java --version`
2. Check the logs in your home directory:  
   `%appdata%/.nbdemetra/dev/var/log/` for Windows  
   `~/.nbdemetra/dev/var/log/` for Linux and Solaris  
   `~/Library/Application Support/.nbdemetra/dev/var/log/` for Mac OS X
