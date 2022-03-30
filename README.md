# Windows11-VMware-Fusion-M1
Windows 11 Image for VMware Fusion in Apple M1

Network Problem FIX

Open CMD (as admin):

Type
“bcdedit /debug on”

Open control panel, then select Device Manager:

Device Manager > Other Devices > Ethernet Controller > Update Driver > Browse my computer for drivers > Let me pick from a list of available drivers on my computer > Network Adapters > Microsoft > Microsoft Kernel Debug Network Adapter.

In CMD type:
bcdedit /dbgsettings net hostip:xxx.xxx.xxx.xxx port:yyyyy”

What this does is configuring the Windows 11 arm VM to use an Ethernet connection for debugging and specifies the IP address of the host (Mac m1) computer. The command also specifies a port number that the host computer can use to connect to the target computer. This gives the Windows 11 Arm VM connectivity to the host.

Solution by: bumwarrior69 --> the thread https://www.reddit.com/r/vmware/comments/obpg4c/windows_11_on_arm/
