#Which tools and software do we need?

We will need some software when applying the dynamic analysis method. Let's take a look at these software categories.


##Virtualization Software

We do not want to conduct dynamic analysis on our own system as we need to run the malware to be able to examine its activities. For this reason, we should make use of Virtualization Software that helps us work on some virtual systems.

Thanks to these software, you can use a different operating system on your host operating system. If they are configured properly, you can perform your analysis safely, as malicious software cannot escape from this virtual operating system. It is useful to make a small note here on these virtualization software. Since these virtualization environments are essentially software, various vulnerabilities that allow malwares to escape out of these virtual environments and allow code executions on the host operating system may occur on these environments. For this reason, It is crucial to keep your virtualization software up-to-date.

Some of the frequently used virtualization software are as follows;

VMware Workstation
VMware Fusion
Oracle Virtualbox
An ideal isolated dynamic analysis environment consists of a completely separate physical device and a separate network. However, setting up this complex environment is both very costly and it is not necessary to begin with.


##Utility Softwares

After installing your own virtual operating system, you need to install software that will be useful in dynamic analysis. For example, we will not be able to perform dynamic analysis of office files with file extensions such as docx, xlsx without installing Microsoft Office or similar software on the system.

Microsoft Office
Adobe Reader
Browser (Chrome, Firefox etc.)
WinRAR
Text Editors (Notepad++, Sublime Text etc.)
The attackers are very familiar with the dynamic analysis method. Therefore they check whether frequently used software is installed or not on the target system to be able determine if the malware is running on a virtual operating system before performing malicious activities on the devices they compromised.


##Debuggers

Debuggers are software that are generally used by programmers to test the codes and catch the errors. Debuggers help to see the instructions of a process and change the flow of the program

Malware analysts frequently make use of debuggers to learn the working structure of the malware and disable some prevention mechanisms by making changes to the malware codes.

For instance, you want to analyze a malware that does not work when the device name is not “John”. With the help of the Debugger, you can disable this control by making changes to the codes in which this control is made, and ensure that the malware continues to run.

Since this training addresses the beginner topics, we will not go in detail about debugging, but since we will use them in our future training, installing debuggers now will make our work easier.

Some debuggers that are frequently preferred by malware analysts are as follows.

Ollydbg
X64dbg
Windbg
Radare2

##Network Monitoring Tools

Information such as the network connections established by the malware, the addresses it communicates with and how it communicates with those should be reported as a result of the malware analysis.

We need some software to detect the network activities of the malware. Some of them are as follows.

Wireshark
Fiddler
Burp Suite

##Process Monitoring Tools

A new process is created for the program we run for malware analysis. In order to monitor these processes, we should use process monitoring tools.

Windows already comes with a process monitoring tool called “Task Manager”. However, other process monitoring tools are more useful in terms of usage and features for malware analysis.

You can install the following process monitoring tools in the virtual operating system we will create for dynamic malware analysis.

Process Hacker
Process Explorer (SysInternals)
Procmon (SysInternals)

##File Activity Monitoring Tools

File activities are one of the first activities that should be followed in dynamic analysis. Malware can read files to collect information from the operating system, write other components of the malware to the file system, and move itself to the startup folder to ensure the persistence. Malware can be involved in various activities in the file system for these and other reasons. We should detect and indicate these activities in the malware analysis report.

You can use the following tools to see file activities.

Sysmon

##Other Tools

SysInternal Tools
CFF Explorer
PEView
TriDNet
BinText
PEiD
Regshot
HashMyFiles
