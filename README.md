## Download RSAT (Remote Server Administration Tools)

Updated: July 9, 2025       
**⬇️ [Download RSAT (Remote Server Administration Tools)](*)**

RSAT enables IT administrators to manage roles and features on Windows Server remotely from a PC running Windows 10 or Windows 7 Service Pack 1.

## Introduction

RSAT cannot be installed on Windows Home or Standard editions. It is supported exclusively on Professional or Enterprise editions of the Windows client operating system. Unless explicitly stated on the download page for a beta, preview, or other prerelease version of Windows, RSAT requires a complete (RTM) release of the OS to install and operate correctly. Some users have tried to manually alter or bypass the RSAT MSU installer in order to use RSAT on unsupported editions or versions of Windows, which is a violation of the Windows end-user license agreement.

Installing RSAT is comparable to installing Adminpak.msi on Windows 2000 or Windows XP client systems. However, unlike those versions, Windows 7 does not automatically activate the tools once the installation is complete. You must manually enable the required tools by navigating to **Start** > **Control Panel** > **Programs and Features**, and then selecting **Turn Windows features on or off**.

For RSAT versions released for Windows 10, all tools are enabled by default. If needed, you can disable specific tools using the **Turn Windows features on or off** interface.

In Windows 7, after executing the RSAT installer package, you need to manually turn on the individual management tools that correspond to the roles and features you intend to manage.

Starting with Windows Server 2012 R2 and onward, if you need tools to manage certain roles or features on remote servers, no separate software installation is required. Just launch the Add Roles and Features Wizard, and on the **Select Features** screen, expand **Remote Server Administration Tools** and check the desired tools. Finish the wizard to complete the installation of those management components.

## RSAT for Windows 10 platform and tools support matrix

| Remote Server Administration Tools Technology | Description | Manages technology in Windows Server 2012 R2 | Manages technology in Windows Server 2016 Technical Preview and Windows Server 2012 R2 |
|-----------------------------------------------|-------------|----------------------------------------------|----------------------------------------------------------------------------------------|
| **Active Directory Certificate Services (AD CS) tools** | AD CS tools include the Certification Authority, Certificate Templates, Enterprise PKI, and Online Responder Management snap-ins. | **√** | **√** |
| **Active Directory Domain Services (AD DS) tools and Active Directory Lightweight Directory Services (AD LDS) tools** | AD DS and AD LDS tools include the following tools:<br><br>- Active Directory Administrative Center <br>- Active Directory Domains and Trusts<br>- Active Directory Sites and Services<br>- Active Directory Users and Computers<br>- ADSI Edit<br>- Active Directory module for Windows PowerShell <br>- Tools such as <ul><li>DCPromo.exe</li><li> LDP.exe</li>  <li>NetDom.exe</li><li>NTDSUtil.exe</li><li>RepAdmin.exe</li><li>DCDiag.exe</li><li>DSACLs.exe</li><li>DSAdd.exe</li><li>DSDBUtil.exe</li><li>DSMgmt.exe</li><li>DSMod.exe</li><li>DSMove.exe</li><li>DSQuery.exe</li><li>DSRm.exe</li><li>GPFixup.exe</li><li>NlTest.exe</li><li>NSLookup.exe</li><li>W32tm.exe</li></ul> |  | **√** |
| **Best Practices Analyzer** | Best Practices Analyzer cmdlets for Windows PowerShell | **√** | **√** |
| **BitLocker Drive Encryption Administration Utilities** | `Manage-bde`, Windows PowerShell cmdlets for BitLocker, BitLocker Recovery Password Viewer for Active Directory | **√** | **√** |
| **DHCP Server tools** | DHCP Server tools include the DHCP Management Console, the DHCP Server cmdlet module for Windows PowerShell, and the **Netsh** command-line tool. | **√** | **√** |
| **DirectAccess, Routing, and Remote Access** | - Routing and Remote Access management console<br> - Connection Manager Administration Kit console<br>- Remote Access provider for Windows PowerShell<br> - Web Application Proxy | **√** | **√** |
| **DNS Server tools** | DNS Server tools include the DNS Manager snap-in, the DNS module for Windows PowerShell, and the **Ddnscmd.exe** command-line tool. | **√** | **√** |
| **Failover Clustering tools** | Failover Clustering tools consist of Failover Cluster Manager, Failover Clusters (Windows PowerShell cmdlets), MSClus, Cluster.exe, the Cluster-Aware Updating management console, and Cluster-Aware Updating cmdlets for Windows PowerShell. | **√** | **√**  <br><br>GUI tools support Windows Server 2016 Technical Preview and Windows Server 2012 R2. Only PowerShell tools work in Windows Server 2012. |
| **File Services tools** | File Services tools include the following tools: <br><br>- Share and Storage Management tools<br>- Distributed File System tools<ul><li>The DFS Management snap-in</li><li>The `Dfsradmin.exe`, `Dfsrdiag.exe`, `Dfscmd.exe`, `Dfsdiag.exe`, and `Dfsutil.exe` command-line tools</li><li> PowerShell modules for DFSN and DFSR</li></ul><br>- File Server Resource Manager tools<ul><li> The File Server Resource Manager snap-in </li><li>The `Dirquota.exe`, `Filescrn.exe`, and `Storrept.exe` command-line tools.</li></ul><br>- Services for NFS Administration tools<br>- iSCSI management cmdlets for Windows PowerShell<br>- Work Folders Management tools | **√** | **√**  <br><br>The Share and Storage Management snap-in was deprecated following the release of Windows Server 2016. Storage Replica, introduced in Windows Server 2016 Technical Preview, is not compatible with Windows Server 2012 R2. |
| **Group Policy Management tools** | Group Policy Management tools include Group Policy Management Console, Group Policy Management Editor, and Group Policy Starter GPO Editor. | **√** | **√**  <br><br>Group Policy has some new features in Windows Server 2016 Technical Preview that aren't available on older operating systems. |
| **Hyper-V tools** | Hyper-V tools include the Hyper-V Manager snap-in and the Virtual Machine Connection remote access tool. | Hyper-V tools are not included in Remote Server Administration Tools for Windows 10. These tools come built into Windows 10, so installing RSAT is not necessary to use them. The Hyper-V Manager console in Windows Server 2016 Technical Preview does not support managing Hyper-V servers running Server 2008 or Server 2008 R2. However, Hyper-V on Windows 10 can manage Hyper-V on Windows Server 2012 R2. |
| **IP Address Management (IPAM) Management tools** | IP Address Management client console | **√**<br><br> IPAM tools in Remote Server Administration Tools for Windows 10 can't be used to manage IPAM running in Windows Server 2012 R2. | **√**<br><br> IPAM tools in Remote Server Administration Tools for Windows 10 can't be used to manage IPAM running in Windows Server 2012 R2. |
| **Network Adapter Teaming, or NIC Teaming** | NIC Teaming management console | **√** | **√** |
| **Network Controller** | Network Controller PowerShell module | Not available | **√** |
| **Network Load Balancing tools** | Network Load Balancing tools include the Network Load Balancing Manager, Network Load Balancing Windows PowerShell cmdlets, and the **NLB.exe** and **WLBS.exe** command-line tools. | **√** | **√** |
| **Remote Desktop Services tools** | Remote Desktop Services tools include: <br> - Remote Desktop snap-ins<br> - RD Gateway Manager<br> - `tsgateway.msc`<br> - RD Licensing Manager<br> - licmgr.exe<br> - RD Licensing Diagnoser<br> - `lsdiag.msc`  <br><br>Use Server Manager to administer all other RDS role services except RD Gateway and RD Licensing. | **√** | **√** |
| **Server for NIS tools** | Server for NIS tools include an extension to the Active Directory Users and Computers snap-in, and the **Ypclear.exe** command-line tool | These tools aren't available in RSAT for Windows 10 and later releases. |  |
| **Server Manager** | Server Manager includes the Server Manager console.<br><br>Remote management with Server Manager is available in Windows Server 2016 Technical Preview, Windows Server 2012 R2, and Windows Server 2012. | **√** | **√** |
| **Simple Mail Transfer Protocol (SMTP) Server tools** | SMTP Server tools include the SMTP snap-in. | These tools aren't available in RSAT for Windows 8 and later releases. |  |
| **Storage Explorer tools** | Storage Explorer tools include the Storage Explorer snap-in. | These tools aren't available in RSAT for Windows 8 and later releases. |  |
| **Storage Manager for Storage Area Network (SAN) tools** | Storage Manager for SAN tools include the Storage Manager for SAN snap-in and the **Provisionstorage.exe** command-line utility. | These tools aren't available in RSAT for Windows 8 and later releases. |  |
| **Volume Activation** | Manage Volume Activation, vmw.exe | **√** | **√** |
| **Windows System Resource Manager tools** | Windows System Resource Manager tools consist of the Windows System Resource Manager snap-in and the **Wsrmc.exe** command-line utility. | **√**<br><br> WSRM was deprecated starting with Windows Server 2012 R2. Management tools for WSRM are not included in RSAT for Windows 8.1 and subsequent RSAT versions. |  |
| **Windows Server Update Services tools** | Windows Server Update Services tools comprise the Windows Server Update Services snap-in, WSUS.msc, and PowerShell cmdlets. | **√** | **√** |


## RSAT for Windows 10, version 1809 or later versions

> **Note**  
> You can't use the Turn Windows features on and off dialog from the Control Panel.

Installing the RSAT Tools on Windows 10 version 1809 and newer is slightly different from earlier releases. RSAT is now included as part of the Operating System and can be installed through **Optional Features**.

To activate the tools, go to **Start** > **Settings** > **Apps** (for Windows 10 version 22H2 or later, choose **System** instead), then click on **Optional features**. Next, open the **Add a feature** section and type *Remote* into the search field.
