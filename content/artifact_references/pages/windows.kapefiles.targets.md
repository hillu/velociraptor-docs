---
title: Windows.KapeFiles.Targets
hidden: true
tags: [Client Artifact]
---


Kape is a popular bulk collector tool for triaging a system
quickly. While KAPE itself is not an opensource tool, the logic it
uses to decide which files to collect is encoded in YAML files
hosted on the KapeFiles project
(https://github.com/EricZimmerman/KapeFiles) and released under an
MIT license.

This artifact is automatically generated from these YAML files,
contributed and maintained by the community. This artifact only
encapsulates the KAPE "Targets" - basically a bunch of glob
expressions used for collecting files on the endpoint. We do not
do any post processing these files - we just collect them.

We recommend that timeouts and upload limits be used
conservatively with this artifact because we can upload really
vast quantities of data very quickly.


```yaml
name: Windows.KapeFiles.Targets
description: |

    Kape is a popular bulk collector tool for triaging a system
    quickly. While KAPE itself is not an opensource tool, the logic it
    uses to decide which files to collect is encoded in YAML files
    hosted on the KapeFiles project
    (https://github.com/EricZimmerman/KapeFiles) and released under an
    MIT license.

    This artifact is automatically generated from these YAML files,
    contributed and maintained by the community. This artifact only
    encapsulates the KAPE "Targets" - basically a bunch of glob
    expressions used for collecting files on the endpoint. We do not
    do any post processing these files - we just collect them.

    We recommend that timeouts and upload limits be used
    conservatively with this artifact because we can upload really
    vast quantities of data very quickly.

reference:
  - https://www.kroll.com/en/insights/publications/cyber/kroll-artifact-parser-extractor-kape
  - https://github.com/EricZimmerman/KapeFiles

parameters:
  - name: UseAutoAccessor
    description: Uses file accessor when possible instead of ntfs parser - this is much faster.
    type: bool
    default: Y
  - name: Device
    description: Name of the drive letter to search.
    default: "C:"
  - name: VSSAnalysis
    type: bool
    default:
    description: If set we run the collection across all VSS and collect only unique changes.

  - name: _BasicCollection
    description: "Basic Collection (by Phill Moore): $Boot, $J, $J, $LogFile, $MFT, $Max, $Max, $T, $T, Amcache, Amcache, Amcache transaction files, Amcache transaction files, AppCompat PCA Folder, Desktop LNK Files, Desktop LNK Files XP, Event logs Win7+, Event logs Win7+, Event logs XP, GatherLogs, LNK Files from C:\ProgramData, LNK Files from Microsoft Office Recent, LNK Files from Recent, LNK Files from Recent (XP), Local Service registry hive, Local Service registry hive, Local Service registry transaction files, Local Service registry transaction files, NTUSER.DAT DEFAULT registry hive, NTUSER.DAT DEFAULT registry hive, NTUSER.DAT DEFAULT transaction files, NTUSER.DAT DEFAULT transaction files, NTUSER.DAT registry hive, NTUSER.DAT registry hive XP, NTUSER.DAT registry transaction files, Network Service registry hive, Network Service registry hive, Network Service registry transaction files, Network Service registry transaction files, PowerShell Console Log, Prefetch, Prefetch, RECYCLER - WinXP, RecentFileCache, RecentFileCache, Recycle Bin - Windows Vista+, RegBack registry transaction files, RegBack registry transaction files, Restore point LNK Files XP, SAM registry hive, SAM registry hive, SAM registry hive (RegBack), SAM registry hive (RegBack), SAM registry transaction files, SAM registry transaction files, SECURITY registry hive, SECURITY registry hive, SECURITY registry hive (RegBack), SECURITY registry hive (RegBack), SECURITY registry transaction files, SECURITY registry transaction files, SOFTWARE registry hive, SOFTWARE registry hive, SOFTWARE registry hive, SOFTWARE registry hive, SOFTWARE registry hive (RegBack), SOFTWARE registry hive (RegBack), SOFTWARE registry transaction files, SOFTWARE registry transaction files, SOFTWARE registry transaction files, SOFTWARE registry transaction files, SRUM, SRUM, SYSTEM registry hive, SYSTEM registry hive, SYSTEM registry hive (RegBack), SYSTEM registry hive (RegBack), SYSTEM registry hive (RegBack), SYSTEM registry hive (RegBack), SYSTEM registry transaction files, SYSTEM registry transaction files, Setupapi.log Win7+, Setupapi.log Win7+, Setupapi.log XP, Start Menu LNK Files, Syscache, Syscache transaction files, System Profile registry hive, System Profile registry hive, System Profile registry transaction files, System Profile registry transaction files, System Restore Points Registry Hives (XP), Thumbcache DB, UsrClass.dat registry hive, UsrClass.dat registry transaction files, WindowsIndexSearch, XML, XML, at .job, at .job, at SchedLgU.txt, at SchedLgU.txt"
    type: bool
  - name: _SANS_Triage
    description: "SANS Triage Collection (by Mark Hallman): $Boot, $J, $J, $LogFile, $MFT, $Max, $Max, $T, $T, AVG AV Logs, AVG AV Logs (XP), AVG AV Report Logs (XP), AVG FileInfo DB, AVG Persistent Logs, AVG Report Logs, AVG lsdbj2 JSON, ActivitiesCache.db, Addons, Addons XP, Amcache, Amcache, Amcache transaction files, Amcache transaction files, Ammyy Program Data, AnyDesk Chat Logs - User Profile, AnyDesk Logs - ProgramData - *.conf, AnyDesk Logs - ProgramData - *.trace, AnyDesk Logs - ProgramData - connection_trace.txt, AnyDesk Logs - System User Account, AnyDesk Logs - User Profile - *.conf, AnyDesk Logs - User Profile - *.trace, AnyDesk Logs - User Profile - connection_trace.txt, AnyDesk Videos, AppCompat PCA Folder, Application Event Log Win7+, Application Event Log Win7+, Application Event Log XP, Application Event Log XP, Avast AV Index, Avast AV Logs, Avast AV Logs (XP), Avast AV User Logs, Avast Icarus Logs, Avast Persistent Data Logs, Avira Activity Logs, Avira Security Logs, Avira VPN Logs, Bitdefender Endpoint Security Logs, Bitdefender Internet Security Logs, Bitdefender SQLite DB Files, Bookmarks, Bookmarks, Bookmarks, Box Drive Application Metadata, Box Sync Application Metadata, Chrome Cookies, Chrome Cookies XP, Chrome Current Session, Chrome Current Session XP, Chrome Current Tabs, Chrome Current Tabs XP, Chrome Download Metadata, Chrome Extension Cookies, Chrome Favicons, Chrome Favicons XP, Chrome History, Chrome History XP, Chrome Last Session, Chrome Last Session XP, Chrome Last Tabs, Chrome Last Tabs XP, Chrome Login Data, Chrome Login Data XP, Chrome Media History, Chrome Network Action Predictor, Chrome Network Persistent State, Chrome Preferences, Chrome Preferences XP, Chrome Quota Manager, Chrome Reporting and NEL, Chrome Sessions Folder, Chrome Shortcuts, Chrome Shortcuts XP, Chrome SyncData Database, Chrome Top Sites, Chrome Top Sites XP, Chrome Trust Tokens, Chrome Visited Links, Chrome Visited Links XP, Chrome Web Data, Chrome Web Data XP, Chrome bookmarks, Chrome bookmarks XP, Cisco Jabber Database, ComboFix, Cookies, Cookies, Cookies, Cookies XP, Current Session, Current Tabs, Cybereason Anti-Ransomware Logs, Cybereason Application Control and NGAV Logs, Cybereason Sensor Communications and Anti-Malware Logs, Delivery Optimization Trace Logs, Desktop LNK Files, Desktop LNK Files XP, Discord Cache Files, Discord Local Storage LevelDB Files, Download Metadata, Downloads, Downloads XP, Dropbox Metadata, Dropbox Metadata, Dropbox Metadata, Dropbox Metadata, Dropbox Metadata, ESET NOD32 AV Logs, ESET NOD32 AV Logs, ESET NOD32 AV Logs (XP), ESET Remote Administrator Logs, Edge Bookmarks, Edge Collections, Edge Cookies, Edge Current Session, Edge Current Tabs, Edge Favicons, Edge History, Edge Last Session, Edge Last Tabs, Edge Login Data, Edge Media History, Edge Network Action Predictor, Edge Preferences, Edge Sessions Folder, Edge Shortcuts, Edge Snapshots Folder, Edge SyncData Database, Edge Top Sites, Edge Visited Links, Edge Web Data, Edge bookmarks, Edge folder, Emsisoft Scan Logs, Energy-NTKL Trace Logs, Event logs Win7+, Event logs Win7+, Event logs XP, Extensions, F-Secure Logs, F-Secure Scheduled Scan Reports, F-Secure User Logs, Favicons, Favicons, Favicons XP, Form history, Form history XP, GatherLogs, Google Drive Backup and Sync Metadata, Google Drive for Desktop Metadata, HexChat Chat Logs, History, HitmanPro Alert Logs, HitmanPro Database, HitmanPro Logs, IE 11 Cookies, IE 11 Metadata, IE 9/10 Cookies, IE 9/10 Download History, IE 9/10 History, IceChat Chat Logs, Index.dat History, Index.dat History subdirectory, Index.dat Office, Index.dat Office XP, Index.dat UserData, Index.dat cookies, Kaseya Agent Edge Service Logs, Kaseya Agent Endpoint Service Logs, Kaseya Agent Endpoint Service Logs (XP), Kaseya Agent Service Log, Kaseya Live Connect Logs, Kaseya Live Connect Logs (XP), Kaseya Setup Log, Kaseya Setup Log, Kaseya Setup Log, LNK Files from C:\ProgramData, LNK Files from Microsoft Office Recent, LNK Files from Recent, LNK Files from Recent (XP), Local Internet Explorer folder, Local Service registry hive, Local Service registry hive, Local Service registry transaction files, Local Service registry transaction files, LocalSessionManager Event Logs, LocalSessionManager Event Logs, LogMeIn Application Logs, LogMeIn ProgramData Logs, Login Data, MalwareBytes Anti-Malware Logs, MalwareBytes Anti-Malware Scan Logs, MalwareBytes Anti-Malware Scan Results Logs, MalwareBytes Anti-Malware Service Logs, Mattermost - Chat Logs, McAfee Desktop Protection Logs, McAfee Desktop Protection Logs XP, McAfee Endpoint Security Logs, McAfee Endpoint Security Logs, McAfee VirusScan Logs, McAfee ePO Logs, Microsoft Teams Cache, Microsoft Teams Config, Microsoft Teams IndexedDB Cache, Microsoft Teams Local Storage Cache, Microsoft Teams Logs (Windows 11), NTUSER.DAT DEFAULT registry hive, NTUSER.DAT DEFAULT registry hive, NTUSER.DAT DEFAULT transaction files, NTUSER.DAT DEFAULT transaction files, NTUSER.DAT registry hive, NTUSER.DAT registry hive XP, NTUSER.DAT registry transaction files, Network Action Predictor, Network Persistent State, Network Service registry hive, Network Service registry hive, Network Service registry transaction files, Network Service registry transaction files, OneDrive Metadata Logs, OneDrive Metadata Settings, Opera - Local Folder, Opera - Roaming Folder, Password, Password, Password, Password XP, Password XP, Password XP, Permissions, Places, Places XP, PowerShell Console Log, Preferences, Preferences, Prefetch, Prefetch, Protections, Publisher Info DB/Brave Rewards, Puffin - Autocomplete Data, Puffin - Cookies, Puffin - Image Cache, Puffin - Password (Encrypted), Puffin - Password Forms Data, Puffin - Subscription Data, Puffin - data.db, Quota Manager, RDP Cache Files, RDP Cache Files, RDPClient Event Logs, RDPClient Event Logs, RDPCoreTS Event Logs, RDPCoreTS Event Logs, RECYCLER - WinXP, Radmin Server 32bit Chats, Radmin Server 32bit Log, Radmin Server 64bit Chats, Radmin Server 64bit Log, Radmin Viewer Chats, RealVNC Log, RecentFileCache, RecentFileCache, Recycle Bin - Windows Vista+, RegBack registry transaction files, RegBack registry transaction files, RemoteConnectionManager Event Logs, RemoteConnectionManager Event Logs, RemoteUtilities Connection Logs, RemoteUtilities Install Log, Reporting and NEL, Restore point LNK Files XP, Roaming Internet Explorer folder, RogueKiller Reports, SAM registry hive, SAM registry hive, SAM registry hive (RegBack), SAM registry hive (RegBack), SAM registry transaction files, SAM registry transaction files, SECURITY registry hive, SECURITY registry hive, SECURITY registry hive (RegBack), SECURITY registry hive (RegBack), SECURITY registry transaction files, SECURITY registry transaction files, SOFTWARE registry hive, SOFTWARE registry hive, SOFTWARE registry hive, SOFTWARE registry hive, SOFTWARE registry hive (RegBack), SOFTWARE registry hive (RegBack), SOFTWARE registry transaction files, SOFTWARE registry transaction files, SOFTWARE registry transaction files, SOFTWARE registry transaction files, SRUM, SRUM, SUM Database (.mdb files), SUPERAntiSpyware Logs, SYSTEM registry hive, SYSTEM registry hive, SYSTEM registry hive (RegBack), SYSTEM registry hive (RegBack), SYSTEM registry hive (RegBack), SYSTEM registry hive (RegBack), SYSTEM registry transaction files, SYSTEM registry transaction files, ScreenConnect Session Database, ScreenConnect Session Database, ScreenConnect User Config, Search, Search XP, Secure Preferences, SecureAge Antvirus Logs, SentinelOne EDR Log, Sessions Folder, Sessionstore, Sessionstore Folder, Sessionstore XP, Setupapi.log Win7+, Setupapi.log Win7+, Setupapi.log XP, Shortcuts, Signal Attachments cache, Signal Database, Signal Logs, Signal config.json, Signons, Signons XP, Skype for Destkop v8+ Chromium Cache, Slack - Chat Logs, Slack Cache, Slack Electron Logs, Slack LevelDB Files, Slack Storage, SleepStudy Trace Logs, SleepStudy Trace Logs, Sophos Logs, Sophos Logs (XP), Splashtop Log Files, Splashtop Log Files in ProgramData, Start Menu LNK Files, Storage Sync, Supremo Connection Logs, Supremo File Transfer Inbox, Symantec Endpoint Protection Logs, Symantec Endpoint Protection Logs (XP), Symantec Endpoint Protection Quarantine, Symantec Endpoint Protection Quarantine (XP), Symantec Endpoint Protection User Logs, Symantec Event Log Win7+, Symantec Event Log Win7+, Syscache, Syscache transaction files, System Profile registry hive, System Profile registry hive, System Profile registry transaction files, System Profile registry transaction files, System Restore Points Registry Hives (XP), TeamViewer Application Logs, TeamViewer Configuration Files, TeamViewer Connection Logs, Telegram app folder, Telegram downloaded files, Thumbcache DB, Top Sites, TotalAV Logs, TotalAV Logs, Trend Micro Logs, Trend Micro Security Agent Connection Logs, Trend Micro Security Agent Report Logs, UltraViewer Logs, UltraViewer Logs, UltraViewer Logs, UsrClass.dat registry hive, UsrClass.dat registry transaction files, VIPRE Business Agent Logs, VIPRE Business User Logs (up to v4), VIPRE Business User Logs (v5-v6), VIPRE Business User Logs (v7+), Viber Config Database, Viber Users Avatars Cache, Viber Users Backgrounds Cache, Viber Users Data Database, Viber Users Thumbnails Cache, Visited Links, WBEM, WBEM, WDI Trace Logs 1, WDI Trace Logs 1, WDI Trace Logs 2, WDI Trace Logs 2, WMI Trace Logs, WMI Trace Logs, Web Data, Webappstore, Webappstore XP, Webroot Program Data, WhatsApp Cache, WhatsApp Local Storage, Windows Defender Event Logs, Windows Defender Event Logs, Windows Defender Logs, Windows Defender Logs, Windows Defender Logs, Windows Defender Logs, Windows Firewall Logs, Windows Firewall Logs, Windows Protect Folder, Windows Protect Folder, Windows Protect Folder, Windows.old RDP Cache Files, WindowsIndexSearch, XML, XML, Zoho Assist .conf files, Zoho Assist .conf files in  Program Files*, Zoho Assist .conf files in AppData\Local, Zoho Assist .txt files in  Program Files*, Zoho Assist log files in AppData\Local, Zoho Assist log files in Program Files*, Zoho Assist log files in ProgramData, at .job, at .job, at SchedLgU.txt, at SchedLgU.txt, ccSubSDK Database, leveldb (Skype for Desktop +v8), mIRC Chat Logs (2000/XP), mIRC Chat Logs (Vista+), mRemoteNG Connection Configuration and Backups, mRemoteNG Logs, mRemoteNG Program Settings, main.db (App <v12), main.db Win7+, main.db XP, registrationInfo.xml, s4l-[username].db (App +v8), skype.db (App +v12)"
    type: bool
  - name: _Boot
    description: "$Boot (by Eric Zimmerman): $Boot"
    type: bool
  - name: _J
    description: "$J (by Eric Zimmerman and Andrew Rathbun): $J, $J, $Max, $Max"
    type: bool
  - name: _LogFile
    description: "$LogFile (by Eric Zimmerman): $LogFile"
    type: bool
  - name: _MFT
    description: "$MFT (by Eric Zimmerman): $MFT"
    type: bool
  - name: _MFTMirr
    description: "$MFTMirr (by Teo Kia Meng): $MFTMirr"
    type: bool
  - name: _T
    description: "$T (by Eric Zimmerman and Andrew Rathbun): $T, $T"
    type: bool
  - name: 1Password
    description: "1Password Password Manager (by Matt Dawson): 1Password Backup Databases, 1Password Database, 1Password Logs"
    type: bool
  - name: 4KVideoDownloader
    description: "4K Video Downloader (by Andrew Rathbun): 4K Video Downloader"
    type: bool
  - name: AVG
    description: "AVG Antivirus Data (by Kirtan Shah and Dhiral Panjwani): AVG AV Logs, AVG AV Logs (XP), AVG AV Report Logs (XP), AVG FileInfo DB, AVG Persistent Logs, AVG Report Logs, AVG lsdbj2 JSON"
    type: bool
  - name: AceText
    description: "AceText (by Andrew Rathbun): AceText - Clipboard History"
    type: bool
  - name: AcronisTrueImage
    description: "Acronis True Image (by Andrew Rathbun): Acronis True Image - Database Files, Acronis True Image - Logs, Acronis True Image - Scripts Folder"
    type: bool
  - name: Amcache
    description: "Amcache.hve (by Eric Zimmerman): Amcache, Amcache, Amcache transaction files, Amcache transaction files"
    type: bool
  - name: Ammyy
    description: "Ammyy Data (by Drew Ervin): Ammyy Program Data"
    type: bool
  - name: Antivirus
    description: "Antivirus (by Andrew Rathbun): AVG AV Logs, AVG AV Logs (XP), AVG AV Report Logs (XP), AVG FileInfo DB, AVG Persistent Logs, AVG Report Logs, AVG lsdbj2 JSON, Application Event Log Win7+, Application Event Log Win7+, Application Event Log XP, Application Event Log XP, Avast AV Index, Avast AV Logs, Avast AV Logs (XP), Avast AV User Logs, Avast Icarus Logs, Avast Persistent Data Logs, Avira Activity Logs, Avira Security Logs, Avira VPN Logs, Bitdefender Endpoint Security Logs, Bitdefender Internet Security Logs, Bitdefender SQLite DB Files, ComboFix, Cybereason Anti-Ransomware Logs, Cybereason Application Control and NGAV Logs, Cybereason Sensor Communications and Anti-Malware Logs, ESET NOD32 AV Logs, ESET NOD32 AV Logs, ESET NOD32 AV Logs (XP), ESET Remote Administrator Logs, Emsisoft Scan Logs, F-Secure Logs, F-Secure Scheduled Scan Reports, F-Secure User Logs, HitmanPro Alert Logs, HitmanPro Database, HitmanPro Logs, MalwareBytes Anti-Malware Logs, MalwareBytes Anti-Malware Scan Logs, MalwareBytes Anti-Malware Scan Results Logs, MalwareBytes Anti-Malware Service Logs, McAfee Desktop Protection Logs, McAfee Desktop Protection Logs XP, McAfee Endpoint Security Logs, McAfee Endpoint Security Logs, McAfee VirusScan Logs, McAfee ePO Logs, RogueKiller Reports, SUPERAntiSpyware Logs, SecureAge Antvirus Logs, SentinelOne EDR Log, Sophos Logs, Sophos Logs (XP), Symantec Endpoint Protection Logs, Symantec Endpoint Protection Logs (XP), Symantec Endpoint Protection Quarantine, Symantec Endpoint Protection Quarantine (XP), Symantec Endpoint Protection User Logs, Symantec Event Log Win7+, Symantec Event Log Win7+, TotalAV Logs, TotalAV Logs, Trend Micro Logs, Trend Micro Security Agent Connection Logs, Trend Micro Security Agent Report Logs, VIPRE Business Agent Logs, VIPRE Business User Logs (up to v4), VIPRE Business User Logs (v5-v6), VIPRE Business User Logs (v7+), Webroot Program Data, Windows Defender Event Logs, Windows Defender Event Logs, Windows Defender Logs, Windows Defender Logs, Windows Defender Logs, Windows Defender Logs, ccSubSDK Database, registrationInfo.xml"
    type: bool
  - name: AnyDesk
    description: "AnyDesk (by Andrew Rathbun, Scott Hanson, and Nicole Jao): AnyDesk Chat Logs - User Profile, AnyDesk Logs - ProgramData - *.conf, AnyDesk Logs - ProgramData - *.trace, AnyDesk Logs - ProgramData - connection_trace.txt, AnyDesk Logs - System User Account, AnyDesk Logs - User Profile - *.conf, AnyDesk Logs - User Profile - *.trace, AnyDesk Logs - User Profile - connection_trace.txt, AnyDesk Videos"
    type: bool
  - name: ApacheAccessLog
    description: "Apache Access Log (by Hadar Yudovich): Apache Access Log"
    type: bool
  - name: AppCompatPCA
    description: "AppCompat PCA Folder (by Andrew Rathbun): AppCompat PCA Folder"
    type: bool
  - name: AppData
    description: "AppData (by Phill Moore): AppData"
    type: bool
  - name: ApplicationEvents
    description: "Windows Application Event Log (by Drew Ervin): Application Event Log Win7+, Application Event Log Win7+, Application Event Log XP, Application Event Log XP"
    type: bool
  - name: AsperaConnect
    description: "Aspera Connect Log Files (by Dennis Reneau): Aspera Client Logs, Aspera Server Logs"
    type: bool
  - name: AssetAdvisorLog
    description: "Asset Advisor Log (by Andrew Rathbun): Asset Advisor Log"
    type: bool
  - name: AteraAgent
    description: "AteraAgent (by Andrew Rathbun): AteraAgent .ini files, AteraAgent Logs, AteraAgent Logs, AteraAgent Logs, AteraAgent Logs"
    type: bool
  - name: Avast
    description: "Avast Antivirus Data (by Drew Ervin and Dhiral Panjwani): Avast AV Index, Avast AV Logs, Avast AV Logs (XP), Avast AV User Logs, Avast Icarus Logs, Avast Persistent Data Logs"
    type: bool
  - name: AviraAVLogs
    description: "Avira Logs (by Fabian Murer and Dhiral Panjwani): Avira Activity Logs, Avira Security Logs, Avira VPN Logs"
    type: bool
  - name: BCD
    description: "Boot Configuration Files (by Troy Larson): BCD, BCD Logs"
    type: bool
  - name: BITS
    description: "Microsoft BITS (Background Intelligent Transer Service) persistent files (by Jos Clephas): BITS files"
    type: bool
  - name: BitTorrent
    description: "BitTorrent (by Banaanhangwagen): TorrentClients - BitTorrent"
    type: bool
  - name: Bitdefender
    description: "Bitdefender Antivirus Data (by Drew Ervin, Ahmed Elshaer): Bitdefender Endpoint Security Logs, Bitdefender Internet Security Logs, Bitdefender SQLite DB Files"
    type: bool
  - name: BoxDrive_Metadata
    description: "Box Cloud Storage Metadata (by Chad Tilbury): Box Drive Application Metadata, Box Sync Application Metadata"
    type: bool
  - name: BoxDrive_UserFiles
    description: "Box Cloud Storage Files (by Chad Tilbury): Box Drive User Files, Box Sync User Files"
    type: bool
  - name: BraveBrowser
    description: "Brave Browser (by Cassie Doemel): Bookmarks, Cookies, Current Session, Current Tabs, Download Metadata, Favicons, History, Login Data, Network Action Predictor, Network Persistent State, Preferences, Publisher Info DB/Brave Rewards, Quota Manager, Reporting and NEL, Secure Preferences, Sessions Folder, Shortcuts, Top Sites, Visited Links, Web Data"
    type: bool
  - name: BrowserCache
    description: "Browser Caches (by Bjorn Vanhaeren): Brave Cache Folder, Chrome Cache Folder, Chromium Edge Cache Folder, Edge WebcacheV01.dat, Firefox Cache Folder, IE 11 Cache, IE 9/10 Cache, IE Index.dat temp internet files"
    type: bool
  - name: CertUtil
    description: "Certutil (by NVISO (@NVISOsecurity)): INetCache, System CryptnetUrlCache, User CryptnetUrlCache"
    type: bool
  - name: Chrome
    description: "Chrome (by Eric Zimmerman and Andrew Rathbun): Chrome Cookies, Chrome Cookies XP, Chrome Current Session, Chrome Current Session XP, Chrome Current Tabs, Chrome Current Tabs XP, Chrome Download Metadata, Chrome Extension Cookies, Chrome Favicons, Chrome Favicons XP, Chrome History, Chrome History XP, Chrome Last Session, Chrome Last Session XP, Chrome Last Tabs, Chrome Last Tabs XP, Chrome Login Data, Chrome Login Data XP, Chrome Media History, Chrome Network Action Predictor, Chrome Network Persistent State, Chrome Preferences, Chrome Preferences XP, Chrome Quota Manager, Chrome Reporting and NEL, Chrome Sessions Folder, Chrome Shortcuts, Chrome Shortcuts XP, Chrome SyncData Database, Chrome Top Sites, Chrome Top Sites XP, Chrome Trust Tokens, Chrome Visited Links, Chrome Visited Links XP, Chrome Web Data, Chrome Web Data XP, Chrome bookmarks, Chrome bookmarks XP, Windows Protect Folder"
    type: bool
  - name: ChromeExtensions
    description: "Chrome Extension Files (by piesecurity): Chrome Extension Files, Chrome Extension Files XP"
    type: bool
  - name: ChromeFileSystem
    description: "Chrome HTML5 File System Contents (by Chad Tilbury): Chrome HTML5 File System Folder"
    type: bool
  - name: CiscoJabber
    description: "Jabber (by Andrew Bannon): Cisco Jabber Database"
    type: bool
  - name: ClipboardMaster
    description: "ClipboardMaster (by Andrew Rathbun): ClipboardMaster - Clipboard History - Backups, ClipboardMaster - Clipboard History - Images, ClipboardMaster - Clipboard History - Text"
    type: bool
  - name: CloudStorage_All
    description: "Cloud Storage Contents and Metadata (by Chad Tilbury and Andrew Rathbun): Box Drive Application Metadata, Box Drive User Files, Box Sync Application Metadata, Box Sync User Files, Dropbox Metadata, Dropbox Metadata, Dropbox Metadata, Dropbox Metadata, Dropbox Metadata, Dropbox User Files, Google Drive Backup and Sync Metadata, Google Drive Backup and Sync User Files, Google Drive for Desktop Metadata, OneDrive Metadata Logs, OneDrive Metadata Settings, OneDrive User Files, SugarSync - My SugarSync (Default Location), SugarSync - Shared Folders (Default Location), SugarSync Log File, Windows Protect Folder, pCloud Database, pCloud Database Shared Memory File, pCloud Database WAL File"
    type: bool
  - name: CloudStorage_Metadata
    description: "Cloud Storage Metadata (by Chad Tilbury and Andrew Rathbun): Box Drive Application Metadata, Box Sync Application Metadata, Dropbox Metadata, Dropbox Metadata, Dropbox Metadata, Dropbox Metadata, Dropbox Metadata, Google Drive Backup and Sync Metadata, Google Drive for Desktop Metadata, OneDrive Metadata Logs, OneDrive Metadata Settings, Windows Protect Folder"
    type: bool
  - name: CloudStorage_OneDriveExplorer
    description: "OneDrive and other files used with OneDriveExplorer (by Brian Maloney): NTUSER.DAT DEFAULT registry hive, NTUSER.DAT DEFAULT registry hive, NTUSER.DAT DEFAULT transaction files, NTUSER.DAT DEFAULT transaction files, NTUSER.DAT registry hive, NTUSER.DAT registry hive XP, NTUSER.DAT registry transaction files, OneDrive Metadata Logs, OneDrive Metadata Settings, RECYCLER - WinXP, RECYCLER - WinXP, Recycle Bin - Windows Vista+, Recycle Bin - Windows Vista+, Recycle Bin - Windows Vista+, UsrClass.dat registry hive, UsrClass.dat registry transaction files"
    type: bool
  - name: CombinedLogs
    description: "Collect Event logs, Trace logs, Windows Firewall and PowerShell console (by Mike Cary, Mark Hallman added the USBDevicelogs target): Delivery Optimization Trace Logs, Energy-NTKL Trace Logs, Event logs Win7+, Event logs Win7+, Event logs XP, PowerShell Console Log, Setupapi.log Win7+, Setupapi.log Win7+, Setupapi.log XP, SleepStudy Trace Logs, SleepStudy Trace Logs, WDI Trace Logs 1, WDI Trace Logs 1, WDI Trace Logs 2, WDI Trace Logs 2, WMI Trace Logs, WMI Trace Logs, Windows Firewall Logs, Windows Firewall Logs"
    type: bool
  - name: Combofix
    description: "ComboFix Antivirus Data (by Drew Ervin): ComboFix"
    type: bool
  - name: ConfluenceLogs
    description: "Confluence Log Files (by Eric Capuano): Confluence Wiki Log Files, Confluence Wiki Log Files"
    type: bool
  - name: Cybereason
    description: "Cybereason Sensor/Detection Logs (by piesecurity): Cybereason Anti-Ransomware Logs, Cybereason Application Control and NGAV Logs, Cybereason Sensor Communications and Anti-Malware Logs"
    type: bool
  - name: DC__
    description: "DC++ (by Andrew Rathbun): DC++ Chat Logs"
    type: bool
  - name: DWAgent
    description: "DWAgent Log Files (by Ron Rader): DWAgent Log Files"
    type: bool
  - name: Debian
    description: "Debian on Windows Subsystem for Linux (by Matt Dawson): Debian WSL .bash_history, Debian WSL .bashrc, Debian WSL .profile, Debian WSL /etc/bash.bashrc, Debian WSL /etc/crontab, Debian WSL /etc/debian_version, Debian WSL /etc/fstab, Debian WSL /etc/group, Debian WSL /etc/hostname, Debian WSL /etc/hosts, Debian WSL /etc/os-release, Debian WSL /etc/passwd, Debian WSL /etc/profile, Debian WSL /etc/shadow, Debian WSL /etc/timezone, Debian WSL Apt Logs, Debian WSL User Crontabs, Debian WSL ext4.vhdx"
    type: bool
  - name: DirectoryOpus
    description: "Directory Opus (by Andrew Rathbun): Directory Opus, Directory Opus, Directory Opus, Directory Opus, Directory Opus, Directory Opus, Directory Opus, Directory Opus, Directory Opus"
    type: bool
  - name: DirectoryTraversal_AudioFiles
    description: "Find audio files covering a multitude of formats (by Andrew Rathbun): Audio files"
    type: bool
  - name: DirectoryTraversal_ExcelDocuments
    description: "Find Excel and Excel alternative documents (by Andrew Rathbun): Excel and Excel-like Documents"
    type: bool
  - name: DirectoryTraversal_PDFDocuments
    description: "Find PDF and PDF alternative documents (by Andrew Rathbun): PDF and PDF-like Documents"
    type: bool
  - name: DirectoryTraversal_PictureFiles
    description: "Find picture files covering a multitude of formats (by Andrew Rathbun): Picture files"
    type: bool
  - name: DirectoryTraversal_SQLiteDatabases
    description: "Find files with common SQLite file extensions (by Andrew Rathbun): SQLite Files (.db* and .sqlite*)"
    type: bool
  - name: DirectoryTraversal_VideoFiles
    description: "Find video files covering a multitude of formats (by Andrew Rathbun): Video files"
    type: bool
  - name: DirectoryTraversal_WildCardExample
    description: "Find zip archives (by Eric Zimmerman): Zips"
    type: bool
  - name: DirectoryTraversal_WordDocuments
    description: "Find Word and Word alternative documents (by Andrew Rathbun): Word and Word-like Documents"
    type: bool
  - name: Discord
    description: "Discord Cache and LevelDB Files (by Christian Johansen and Matt Dawson): Discord Cache Files, Discord Local Storage LevelDB Files"
    type: bool
  - name: DoubleCommander
    description: "Double Commander (by Andrew Rathbun): Double Commander - FTP Log, Double Commander - doublecmd.xml, Double Commander - history.xml, Double Commander - multiarc.ini, Double Commander - pixmaps.txt, Double Commander - session.ini, Double Commander - shortcuts.scf"
    type: bool
  - name: Dropbox_Metadata
    description: "Dropbox Cloud Storage Metadata (by Chad Tilbury and Andrew Rathbun): Dropbox Metadata, Dropbox Metadata, Dropbox Metadata, Dropbox Metadata, Dropbox Metadata, Windows Protect Folder"
    type: bool
  - name: Dropbox_UserFiles
    description: "Dropbox Cloud Storage Files (by Chad Tilbury): Dropbox User Files"
    type: bool
  - name: EFCommander
    description: "EF Commander (by Andrew Rathbun): EF Commander - .ini File"
    type: bool
  - name: ESET
    description: "ESET Antivirus Data (by Drew Ervin): ESET NOD32 AV Logs, ESET NOD32 AV Logs, ESET NOD32 AV Logs (XP), ESET Remote Administrator Logs"
    type: bool
  - name: Edge
    description: "Edge (by Phill Moore): Edge folder"
    type: bool
  - name: EdgeChromium
    description: "Microsoft Edge Chromium Artifacts (by Chad Tilbury and Andrew Rathbun): Edge Bookmarks, Edge Collections, Edge Cookies, Edge Current Session, Edge Current Tabs, Edge Favicons, Edge History, Edge Last Session, Edge Last Tabs, Edge Login Data, Edge Media History, Edge Network Action Predictor, Edge Preferences, Edge Sessions Folder, Edge Shortcuts, Edge Snapshots Folder, Edge SyncData Database, Edge Top Sites, Edge Visited Links, Edge Web Data, Edge bookmarks, Windows Protect Folder"
    type: bool
  - name: Emsisoft
    description: "Emsisoft Antivirus Logs (by blueskycyber): Emsisoft Scan Logs"
    type: bool
  - name: EncapsulationLogging
    description: "EncapsulationLogging (by Troy Larson): EncapsulationLogging, EncapsulationLogging, EncapsulationLogging Logs, EncapsulationLogging Logs"
    type: bool
  - name: EventLogs_RDP
    description: "Collect Win7+ RDP related Event logs (by Mark Hallman): Event logs Win7+, Event logs Win7+, Event logs Win7+, Event logs Win7+, Event logs Win7+, Event logs Win7+"
    type: bool
  - name: EventLogs
    description: "Event logs (by Eric Zimmerman): Event logs Win7+, Event logs Win7+, Event logs XP"
    type: bool
  - name: EventTraceLogs
    description: "Event Trace Logs (by Mark Hallman): Delivery Optimization Trace Logs, Energy-NTKL Trace Logs, SleepStudy Trace Logs, SleepStudy Trace Logs, WDI Trace Logs 1, WDI Trace Logs 1, WDI Trace Logs 2, WDI Trace Logs 2, WMI Trace Logs, WMI Trace Logs"
    type: bool
  - name: EventTranscriptDB
    description: "EventTranscript.db (and other files related to Telemetry and Diagnostic Data) (by Andrew Rathbun and Josh Mitchell): EventTranscript.db, EventTranscript.db, Microsoft Office Diagnostic Logs"
    type: bool
  - name: Evernote
    description: "Evernote (by Matt Dawson): Evernote Accounts, Evernote Notebook Snippets, Evernote Notebooks"
    type: bool
  - name: Everything__VoidTools_
    description: "Everything (VoidTools) (by Andrew Rathbun): Everything (VoidTools), Everything (VoidTools) - .ini file, Everything (VoidTools) - Run History, Everything (VoidTools) - Search History"
    type: bool
  - name: EvidenceOfExecution
    description: "Evidence of execution related files (by Eric Zimmerman): Amcache, Amcache, Amcache transaction files, Amcache transaction files, AppCompat PCA Folder, Prefetch, Prefetch, RecentFileCache, RecentFileCache, Syscache, Syscache transaction files"
    type: bool
  - name: Exchange
    description: "Exchange Log Files (by Keith Twombley): Exchange TransportRoles log files, Exchange client access log files"
    type: bool
  - name: ExchangeClientAccess
    description: "Exchange Client Access Log Files (by Keith Twombley): Exchange client access log files"
    type: bool
  - name: ExchangeCve_2021_26855
    description: "Exchange Server Vulnerability *.Compiled Files (by Dennis Reneau): Exchange Server Modified Compiled Files, Exchange Server Modified Compiled Files, Exchange Server Modified Compiled Files, Exchange Server Modified Compiled Files"
    type: bool
  - name: ExchangeTransport
    description: "Exchange Transport Log Files (by Keith Twombley): Exchange TransportRoles log files"
    type: bool
  - name: FSecure
    description: "F-Secure Antivirus Data (by Drew Ervin): F-Secure Logs, F-Secure Scheduled Scan Reports, F-Secure User Logs"
    type: bool
  - name: FTPClients
    description: "FTP Clients (by Andrew Rathbun): FileZilla Log Files, FileZilla SQLite3 Log Files, FileZilla Server XML Log Files, FileZilla XML Log Files, WinSCP (.ini file)"
    type: bool
  - name: Fences
    description: "Fences (by Andrew Rathbun): Fences - Desktop Screenshots"
    type: bool
  - name: FileExplorerReplacements
    description: "File Explorer Replacements (by Andrew Rathbun): Directory Opus, Directory Opus, Directory Opus, Directory Opus, Directory Opus, Directory Opus, Directory Opus, Directory Opus, Directory Opus, Double Commander - FTP Log, Double Commander - doublecmd.xml, Double Commander - history.xml, Double Commander - multiarc.ini, Double Commander - pixmaps.txt, Double Commander - session.ini, Double Commander - shortcuts.scf, EF Commander - .ini File, Free Commander - Backup Settings, Free Commander - FTP Log, Free Commander - FTP Related Information, Free Commander - FreeCommander.fav.xml, Free Commander - FreeCommander.ftp.ini, Free Commander - FreeCommander.hist.ini, Free Commander - FreeCommander.ini, Midnight Commander -- All Configuation Files, Multi Commander - Application Folder, Multi Commander - Config Folder, Multi Commander - Log File, Multi Commander - Log Folder, Multi Commander - UserData Folder, One Commander - All Configuration Files, One Commander - Other Configuration Files, Q-Dir - .ini File, Q-Dir - .qdr file, SpeedCommander - .ini File, Tablacus Explorer - remember.xml, Tablacus Explorer - window.xml, Tablacus Explorer - window1.xml, Total Commander - .ini File, Total Commander - FTP .ini File, Total Commander - FTP Logs, Total Commander - File Tree, Total Commander - Log File, Total Commander - Temp Files Created During Folder Traversal, XYplorer - .dat files, XYplorer - .ini file, XYplorer - .ini file for each respective pane, XYplorer - AutoBackup folder"
    type: bool
  - name: FileSystem
    description: "File system metadata (by Eric Zimmerman): $Boot, $J, $J, $LogFile, $MFT, $Max, $Max, $T, $T"
    type: bool
  - name: FileZillaClient
    description: "FileZilla XML and SQLite Log Files (by Dennis Reneau): FileZilla SQLite3 Log Files, FileZilla XML Log Files"
    type: bool
  - name: FileZillaServer
    description: "FileZilla Server Logs (by Andrew Rathbun): FileZilla Log Files, FileZilla Server XML Log Files"
    type: bool
  - name: Firefox
    description: "Firefox (by Eric Zimmerman and Andrew Rathbun): Addons, Addons XP, Bookmarks, Bookmarks, Cookies, Cookies, Cookies XP, Downloads, Downloads XP, Extensions, Favicons, Favicons XP, Form history, Form history XP, Password, Password, Password, Password XP, Password XP, Password XP, Permissions, Places, Places XP, Preferences, Protections, Search, Search XP, Sessionstore, Sessionstore Folder, Sessionstore XP, Signons, Signons XP, Storage Sync, Webappstore, Webappstore XP"
    type: bool
  - name: FreeCommander
    description: "FreeCommander XE (by Andrew Rathbun): Free Commander - Backup Settings, Free Commander - FTP Log, Free Commander - FTP Related Information, Free Commander - FreeCommander.fav.xml, Free Commander - FreeCommander.ftp.ini, Free Commander - FreeCommander.hist.ini, Free Commander - FreeCommander.ini"
    type: bool
  - name: FreeDownloadManager
    description: "Free Download Manager (by Matt Dawson): FDM Backup Info, FDM Database, FDM Database (userdata.zip)"
    type: bool
  - name: FreeFileSync
    description: "FreeFileSync (by Andrew Rathbun): FreeFileSync"
    type: bool
  - name: Freenet
    description: "Freenet (by Charlie Rubisoff): Freenet, Freenet, Freenet, Freenet, Freenet"
    type: bool
  - name: FrostWire
    description: "FrostWire (by Andrew Rathbun): FrostWire AppData, FrostWire AppData, FrostWire Downloads"
    type: bool
  - name: Gigatribe
    description: "Gigatribe Files (by Linus Nissi): Gigatribe Files Windows Vista/7/8/10, Gigatribe Files Windows XP, Gigatribe Files Windows XP"
    type: bool
  - name: GoogleDriveBackupSync_UserFiles
    description: "Google Backup and Sync Storage Files (by Chad Tilbury): Google Drive Backup and Sync User Files"
    type: bool
  - name: GoogleDrive_Metadata
    description: "Google Drive Metadata (by Chad Tilbury): Google Drive Backup and Sync Metadata, Google Drive for Desktop Metadata"
    type: bool
  - name: GoogleEarth
    description: "Google Earth (by Guus Beckers): Google Earth My Places Backup file, Google Earth My Places Backup file (XP), Google Earth My Places file, Google Earth My Places file (XP)"
    type: bool
  - name: GroupPolicy
    description: "Current Group Policy Enforcement (by piesecurity): Local Group Policy Files - Registry Policy Files, Local Group Policy Files - Registry Policy Files, Local Group Policy Files - Startup/Shutdown Scripts, Local Group Policy Files - Startup/Shutdown Scripts, Local Group Policy INI Files, Local Group Policy INI Files"
    type: bool
  - name: HeidiSQL
    description: "HeidiSQL (by Hyun Yi @hyuunnn): HeidiSQL (tabs.ini), HeidiSQL Backup files (*.sql)"
    type: bool
  - name: HexChat
    description: "HexChat (by Andrew Rathbun): HexChat Chat Logs"
    type: bool
  - name: HitmanPro
    description: "HitmanPro Antivirus Data (by Drew Ervin): HitmanPro Alert Logs, HitmanPro Database, HitmanPro Logs"
    type: bool
  - name: IISConfiguration
    description: "IIS (by NVISO (@NVISOsecurity)): IIS administration.config, IIS applicationHost.config, IIS redirection.config, web.config"
    type: bool
  - name: IISLogFiles
    description: "IIS Log Files (by Troy Larson): IIS log files, IIS log files, IIS log files, IIS log files, IIS log files, IIS log files"
    type: bool
  - name: IRCClients
    description: "IRC Clients (by Andrew Rathbun): HexChat Chat Logs, IceChat Chat Logs, mIRC Chat Logs (2000/XP), mIRC Chat Logs (Vista+)"
    type: bool
  - name: IceChat
    description: "IceChat (by Andrew Rathbun): IceChat Chat Logs"
    type: bool
  - name: InternetExplorer
    description: "Internet Explorer (by Eric Zimmerman): IE 11 Cookies, IE 11 Metadata, IE 9/10 Cookies, IE 9/10 Download History, IE 9/10 History, Index.dat History, Index.dat History subdirectory, Index.dat Office, Index.dat Office XP, Index.dat UserData, Index.dat cookies, Local Internet Explorer folder, Roaming Internet Explorer folder"
    type: bool
  - name: IrfanView
    description: "IrfanView (by Andrew Rathbun): IrfanView Configuration File"
    type: bool
  - name: JDownloader2
    description: "JDownloader 2 (by Matt Dawson): JDownloader 2.0 Download Lists, JDownloader 2.0 General Settings, JDownloader 2.0 Link Collector, JDownloader 2.0 Link Grabber Settings, JDownloader 2.0 Proxy Settings"
    type: bool
  - name: JavaWebCache
    description: "Java WebStart Cache - (IDX Files) (by piesecurity): Java WebStart Cache System level, Java WebStart Cache System level, Java WebStart Cache System level (SysWow64), Java WebStart Cache System level (SysWow64), Java WebStart Cache System level (SysWow64) - IE Protected Mode, Java WebStart Cache System level (SysWow64) - IE Protected Mode, Java WebStart Cache System level - IE Protected Mode, Java WebStart Cache System level - IE Protected Mode, Java WebStart Cache User Level - Default, Java WebStart Cache User Level - IE Protected Mode, Java WebStart Cache User Level - XP"
    type: bool
  - name: Kali
    description: "Kali on Windows Subsystem for Linux (by Matt Dawson): Kali WSL .bash_history, Kali WSL .bashrc, Kali WSL .profile, Kali WSL /etc/bash.bashrc, Kali WSL /etc/crontab, Kali WSL /etc/debian_version, Kali WSL /etc/fstab, Kali WSL /etc/group, Kali WSL /etc/hostname, Kali WSL /etc/hosts, Kali WSL /etc/os-release, Kali WSL /etc/passwd, Kali WSL /etc/profile, Kali WSL /etc/shadow, Kali WSL /etc/timezone, Kali WSL Apt Logs, Kali WSL User Crontabs, Kali WSL ext4.vhdx"
    type: bool
  - name: KapeTriage
    description: "Kape Triage collections that will collect most of the files needed for a DFIR Investigation.  This module pulls evidence from File System files, Registry Hives, Event Logs, Scheduled Tasks, Evidence of Execution, SRUM data, SUM data, Web Browser data (IE/Edge, Chrome, Mozilla history), LNK Files, Jump Lists, 3rd party remote access software logs, 3rd party antivirus software logs, Windows 10 Timeline database, and $I Recycle Bin data files. (by Scott Downie): $Boot, $J, $J, $LogFile, $MFT, $Max, $Max, $T, $T, AVG AV Logs, AVG AV Logs (XP), AVG AV Report Logs (XP), AVG FileInfo DB, AVG Persistent Logs, AVG Report Logs, AVG lsdbj2 JSON, ActivitiesCache.db, Addons, Addons XP, Amcache, Amcache, Amcache transaction files, Amcache transaction files, Ammyy Program Data, AnyDesk Chat Logs - User Profile, AnyDesk Logs - ProgramData - *.conf, AnyDesk Logs - ProgramData - *.trace, AnyDesk Logs - ProgramData - connection_trace.txt, AnyDesk Logs - System User Account, AnyDesk Logs - User Profile - *.conf, AnyDesk Logs - User Profile - *.trace, AnyDesk Logs - User Profile - connection_trace.txt, AnyDesk Videos, AppCompat PCA Folder, Application Event Log Win7+, Application Event Log Win7+, Application Event Log XP, Application Event Log XP, Avast AV Index, Avast AV Logs, Avast AV Logs (XP), Avast AV User Logs, Avast Icarus Logs, Avast Persistent Data Logs, Avira Activity Logs, Avira Security Logs, Avira VPN Logs, Bitdefender Endpoint Security Logs, Bitdefender Internet Security Logs, Bitdefender SQLite DB Files, Bookmarks, Bookmarks, Bookmarks, Chrome Cookies, Chrome Cookies XP, Chrome Current Session, Chrome Current Session XP, Chrome Current Tabs, Chrome Current Tabs XP, Chrome Download Metadata, Chrome Extension Cookies, Chrome Favicons, Chrome Favicons XP, Chrome History, Chrome History XP, Chrome Last Session, Chrome Last Session XP, Chrome Last Tabs, Chrome Last Tabs XP, Chrome Login Data, Chrome Login Data XP, Chrome Media History, Chrome Network Action Predictor, Chrome Network Persistent State, Chrome Preferences, Chrome Preferences XP, Chrome Quota Manager, Chrome Reporting and NEL, Chrome Sessions Folder, Chrome Shortcuts, Chrome Shortcuts XP, Chrome SyncData Database, Chrome Top Sites, Chrome Top Sites XP, Chrome Trust Tokens, Chrome Visited Links, Chrome Visited Links XP, Chrome Web Data, Chrome Web Data XP, Chrome bookmarks, Chrome bookmarks XP, ComboFix, Cookies, Cookies, Cookies, Cookies XP, Current Session, Current Tabs, Cybereason Anti-Ransomware Logs, Cybereason Application Control and NGAV Logs, Cybereason Sensor Communications and Anti-Malware Logs, Desktop LNK Files, Desktop LNK Files XP, Download Metadata, Downloads, Downloads XP, ESET NOD32 AV Logs, ESET NOD32 AV Logs, ESET NOD32 AV Logs (XP), ESET Remote Administrator Logs, Edge Bookmarks, Edge Collections, Edge Cookies, Edge Current Session, Edge Current Tabs, Edge Favicons, Edge History, Edge Last Session, Edge Last Tabs, Edge Login Data, Edge Media History, Edge Network Action Predictor, Edge Preferences, Edge Sessions Folder, Edge Shortcuts, Edge Snapshots Folder, Edge SyncData Database, Edge Top Sites, Edge Visited Links, Edge Web Data, Edge bookmarks, Edge folder, Emsisoft Scan Logs, Event logs Win7+, Event logs Win7+, Event logs XP, Extensions, F-Secure Logs, F-Secure Scheduled Scan Reports, F-Secure User Logs, Favicons, Favicons, Favicons XP, Form history, Form history XP, History, HitmanPro Alert Logs, HitmanPro Database, HitmanPro Logs, IE 11 Cookies, IE 11 Metadata, IE 9/10 Cookies, IE 9/10 Download History, IE 9/10 History, Index.dat History, Index.dat History subdirectory, Index.dat Office, Index.dat Office XP, Index.dat UserData, Index.dat cookies, Kaseya Agent Edge Service Logs, Kaseya Agent Endpoint Service Logs, Kaseya Agent Endpoint Service Logs (XP), Kaseya Agent Service Log, Kaseya Live Connect Logs, Kaseya Live Connect Logs (XP), Kaseya Setup Log, Kaseya Setup Log, Kaseya Setup Log, LNK Files from C:\ProgramData, LNK Files from Microsoft Office Recent, LNK Files from Recent, LNK Files from Recent (XP), Local Internet Explorer folder, Local Service registry hive, Local Service registry hive, Local Service registry transaction files, Local Service registry transaction files, LocalSessionManager Event Logs, LocalSessionManager Event Logs, LogMeIn Application Logs, LogMeIn ProgramData Logs, Login Data, MalwareBytes Anti-Malware Logs, MalwareBytes Anti-Malware Scan Logs, MalwareBytes Anti-Malware Scan Results Logs, MalwareBytes Anti-Malware Service Logs, McAfee Desktop Protection Logs, McAfee Desktop Protection Logs XP, McAfee Endpoint Security Logs, McAfee Endpoint Security Logs, McAfee VirusScan Logs, McAfee ePO Logs, NTUSER.DAT DEFAULT registry hive, NTUSER.DAT DEFAULT registry hive, NTUSER.DAT DEFAULT transaction files, NTUSER.DAT DEFAULT transaction files, NTUSER.DAT registry hive, NTUSER.DAT registry hive XP, NTUSER.DAT registry transaction files, Network Action Predictor, Network Persistent State, Network Service registry hive, Network Service registry hive, Network Service registry transaction files, Network Service registry transaction files, Opera - Local Folder, Opera - Roaming Folder, Password, Password, Password, Password XP, Password XP, Password XP, Permissions, Places, Places XP, PowerShell Console Log, Preferences, Preferences, Prefetch, Prefetch, Protections, Publisher Info DB/Brave Rewards, Puffin - Autocomplete Data, Puffin - Cookies, Puffin - Image Cache, Puffin - Password (Encrypted), Puffin - Password Forms Data, Puffin - Subscription Data, Puffin - data.db, Quota Manager, RDP Cache Files, RDP Cache Files, RDPClient Event Logs, RDPClient Event Logs, RDPCoreTS Event Logs, RDPCoreTS Event Logs, RECYCLER - WinXP, Radmin Server 32bit Chats, Radmin Server 32bit Log, Radmin Server 64bit Chats, Radmin Server 64bit Log, Radmin Viewer Chats, RealVNC Log, RecentFileCache, RecentFileCache, Recycle Bin - Windows Vista+, RegBack registry transaction files, RegBack registry transaction files, RemoteConnectionManager Event Logs, RemoteConnectionManager Event Logs, RemoteUtilities Connection Logs, RemoteUtilities Install Log, Reporting and NEL, Restore point LNK Files XP, Roaming Internet Explorer folder, RogueKiller Reports, SAM registry hive, SAM registry hive, SAM registry hive (RegBack), SAM registry hive (RegBack), SAM registry transaction files, SAM registry transaction files, SECURITY registry hive, SECURITY registry hive, SECURITY registry hive (RegBack), SECURITY registry hive (RegBack), SECURITY registry transaction files, SECURITY registry transaction files, SOFTWARE registry hive, SOFTWARE registry hive, SOFTWARE registry hive, SOFTWARE registry hive, SOFTWARE registry hive (RegBack), SOFTWARE registry hive (RegBack), SOFTWARE registry transaction files, SOFTWARE registry transaction files, SOFTWARE registry transaction files, SOFTWARE registry transaction files, SRUM, SRUM, SUM Database (.mdb files), SUPERAntiSpyware Logs, SYSTEM registry hive, SYSTEM registry hive, SYSTEM registry hive (RegBack), SYSTEM registry hive (RegBack), SYSTEM registry hive (RegBack), SYSTEM registry hive (RegBack), SYSTEM registry transaction files, SYSTEM registry transaction files, ScreenConnect Session Database, ScreenConnect Session Database, ScreenConnect User Config, Search, Search XP, Secure Preferences, SecureAge Antvirus Logs, SentinelOne EDR Log, Sessions Folder, Sessionstore, Sessionstore Folder, Sessionstore XP, Shortcuts, Signons, Signons XP, Sophos Logs, Sophos Logs (XP), Splashtop Log Files, Splashtop Log Files in ProgramData, Start Menu LNK Files, Storage Sync, Supremo Connection Logs, Supremo File Transfer Inbox, Symantec Endpoint Protection Logs, Symantec Endpoint Protection Logs (XP), Symantec Endpoint Protection Quarantine, Symantec Endpoint Protection Quarantine (XP), Symantec Endpoint Protection User Logs, Symantec Event Log Win7+, Symantec Event Log Win7+, Syscache, Syscache transaction files, System Profile registry hive, System Profile registry hive, System Profile registry transaction files, System Profile registry transaction files, System Restore Points Registry Hives (XP), TeamViewer Application Logs, TeamViewer Configuration Files, TeamViewer Connection Logs, Top Sites, TotalAV Logs, TotalAV Logs, Trend Micro Logs, Trend Micro Security Agent Connection Logs, Trend Micro Security Agent Report Logs, UltraViewer Logs, UltraViewer Logs, UltraViewer Logs, UsrClass.dat registry hive, UsrClass.dat registry transaction files, VIPRE Business Agent Logs, VIPRE Business User Logs (up to v4), VIPRE Business User Logs (v5-v6), VIPRE Business User Logs (v7+), Visited Links, Web Data, Webappstore, Webappstore XP, Webroot Program Data, Windows Defender Event Logs, Windows Defender Event Logs, Windows Defender Logs, Windows Defender Logs, Windows Defender Logs, Windows Defender Logs, Windows Protect Folder, Windows Protect Folder, Windows.old RDP Cache Files, XML, XML, Zoho Assist .conf files, Zoho Assist .conf files in  Program Files*, Zoho Assist .conf files in AppData\Local, Zoho Assist .txt files in  Program Files*, Zoho Assist log files in AppData\Local, Zoho Assist log files in Program Files*, Zoho Assist log files in ProgramData, at .job, at .job, at SchedLgU.txt, at SchedLgU.txt, ccSubSDK Database, mRemoteNG Connection Configuration and Backups, mRemoteNG Logs, mRemoteNG Program Settings, registrationInfo.xml"
    type: bool
  - name: Kaseya
    description: "Kaseya Data (by Drew Ervin and Andrew Rathbun): Kaseya Agent Edge Service Logs, Kaseya Agent Endpoint Service Logs, Kaseya Agent Endpoint Service Logs (XP), Kaseya Agent Service Log, Kaseya Live Connect Logs, Kaseya Live Connect Logs (XP), Kaseya Setup Log, Kaseya Setup Log, Kaseya Setup Log"
    type: bool
  - name: Keepass
    description: "Keepass (by Vito Alfano): Keepass Application Details, Keepass Config Xml, Keepass User Config"
    type: bool
  - name: KeepassXC
    description: "KeepassXC (by Vito Alfano): Keepass Local Ini, Keepass Roaming Ini"
    type: bool
  - name: LNKFilesAndJumpLists
    description: "LNK Files and jump lists (by Eric Zimmerman, Andrew Rathbun, Yogesh Khatri): Desktop LNK Files, Desktop LNK Files XP, LNK Files from C:\ProgramData, LNK Files from Microsoft Office Recent, LNK Files from Recent, LNK Files from Recent (XP), Restore point LNK Files XP, Start Menu LNK Files"
    type: bool
  - name: LinuxOnWindowsProfileFiles
    description: "Linux on Windows Profile Files (by Troy Larson): .bash_history, .bash_logout, .bashrc, .profile"
    type: bool
  - name: LiveUserFiles
    description: "Live User Files (by Mark Hallman): User Files - Desktop, User Files - Documents, User Files - Downloads, User Files - Dropbox"
    type: bool
  - name: LogFiles
    description: "LogFiles (includes SUM) (by Fabian Murer): LogFiles, LogFiles"
    type: bool
  - name: LogMeIn
    description: "LogMeIn Data (by Drew Ervin): Application Event Log Win7+, Application Event Log Win7+, Application Event Log XP, Application Event Log XP, LogMeIn Application Logs, LogMeIn ProgramData Logs"
    type: bool
  - name: MOF
    description: "MOF files (WMI) (by Eric Zimmerman): MOF files"
    type: bool
  - name: MSSQLErrorLog
    description: "MS SQL ErrorLogs (by Troy Larson): MS SQL Errorlog, MS SQL Errorlogs"
    type: bool
  - name: MacriumReflect
    description: "Macrium Reflect (by Andrew Rathbun): Macrium Reflect, Macrium Reflect, Macrium Reflect"
    type: bool
  - name: Malwarebytes
    description: "Malwarebytes Data (by Drew Ervin & Kirtan Shah): MalwareBytes Anti-Malware Logs, MalwareBytes Anti-Malware Scan Logs, MalwareBytes Anti-Malware Scan Results Logs, MalwareBytes Anti-Malware Service Logs"
    type: bool
  - name: ManageEngineLogs
    description: "ManageEngine Desktop Central Log Files (by Whitney Champion): ManageEngine Desktop Central Log Files"
    type: bool
  - name: Mattermost
    description: "Mattermost (by Andrew Rathbun): Mattermost - Chat Logs"
    type: bool
  - name: McAfee
    description: "McAfee Log Files (by Sam Smoker): McAfee Desktop Protection Logs, McAfee Desktop Protection Logs XP, McAfee Endpoint Security Logs, McAfee Endpoint Security Logs, McAfee VirusScan Logs"
    type: bool
  - name: McAfee_ePO
    description: "McAfee ePO Log Files (by Doug Metz): McAfee ePO Logs"
    type: bool
  - name: MediaMonkey
    description: "MediaMonkey (by Andrew Rathbun): MediaMonkey - Media SQLite Database, MediaMonkey - MediaMonkey.ini"
    type: bool
  - name: MemoryFiles
    description: "Memory Files (by Ahmed Elshaer, Teo Kia Meng): Small Memory Dump directory, Small Memory Dump directory, hiberfil.sys, pagefile.sys, swapfile.sys"
    type: bool
  - name: MessagingClients
    description: "Messaging and communication apps (by Gregor Wegberg): Cisco Jabber Database, Discord Cache Files, Discord Local Storage LevelDB Files, HexChat Chat Logs, IceChat Chat Logs, Mattermost - Chat Logs, Microsoft Teams Cache, Microsoft Teams Config, Microsoft Teams IndexedDB Cache, Microsoft Teams Local Storage Cache, Microsoft Teams Logs (Windows 11), Signal Attachments cache, Signal Database, Signal Logs, Signal config.json, Skype for Destkop v8+ Chromium Cache, Slack - Chat Logs, Slack Cache, Slack Electron Logs, Slack LevelDB Files, Slack Storage, Telegram app folder, Telegram downloaded files, Viber Config Database, Viber Users Avatars Cache, Viber Users Backgrounds Cache, Viber Users Data Database, Viber Users Thumbnails Cache, WhatsApp Cache, WhatsApp Local Storage, leveldb (Skype for Desktop +v8), mIRC Chat Logs (2000/XP), mIRC Chat Logs (Vista+), main.db (App <v12), main.db Win7+, main.db XP, s4l-[username].db (App +v8), skype.db (App +v12)"
    type: bool
  - name: MicrosoftOfficeBackstage
    description: "Microsoft Office Backstage (by Brian Maloney): Microsoft Office Backstage"
    type: bool
  - name: MicrosoftOneNote
    description: "Microsoft OneNote (by Andrew Rathbun): Microsoft OneNote - AccessibilityCheckerIndex, Microsoft OneNote - FullTextSearchIndex, Microsoft OneNote - RecentNotebooks_SeenURLs, Microsoft OneNote - RecentSearches, Microsoft OneNote - User NoteTags"
    type: bool
  - name: MicrosoftStickyNotes
    description: "Microsoft Sticky Notes (by Andrew Rathbun): Microsoft Sticky Notes - 1607 and later, Microsoft Sticky Notes - Windows 7, 8, and 10 version 1511 and earlier"
    type: bool
  - name: MicrosoftTeams
    description: "Microsoft Teams (by Matt Dawson and Andrew Rathbun): Microsoft Teams Cache, Microsoft Teams Config, Microsoft Teams IndexedDB Cache, Microsoft Teams Local Storage Cache, Microsoft Teams Logs (Windows 11)"
    type: bool
  - name: MicrosoftToDo
    description: "Microsoft To Do (by Andrew Rathbun): Microsoft To Do - SQLite Database of To Do tasks, Microsoft To Do - User Avatar"
    type: bool
  - name: MidnightCommander
    description: "Midnight Commander (by Andrew Rathbun): Midnight Commander -- All Configuation Files"
    type: bool
  - name: MiniTimelineCollection
    description: "MFT, Registry and Event Logs to generate a mini timeline (by Mari DeGrazia): $Boot, $J, $J, $LogFile, $MFT, $Max, $Max, $T, $T, Event logs Win7+, Event logs Win7+, Event logs XP, Local Service registry hive, Local Service registry hive, Local Service registry transaction files, Local Service registry transaction files, NTUSER.DAT DEFAULT registry hive, NTUSER.DAT DEFAULT registry hive, NTUSER.DAT DEFAULT transaction files, NTUSER.DAT DEFAULT transaction files, NTUSER.DAT registry hive, NTUSER.DAT registry hive XP, NTUSER.DAT registry transaction files, Network Service registry hive, Network Service registry hive, Network Service registry transaction files, Network Service registry transaction files, RegBack registry transaction files, RegBack registry transaction files, SAM registry hive, SAM registry hive, SAM registry hive (RegBack), SAM registry hive (RegBack), SAM registry transaction files, SAM registry transaction files, SECURITY registry hive, SECURITY registry hive, SECURITY registry hive (RegBack), SECURITY registry hive (RegBack), SECURITY registry transaction files, SECURITY registry transaction files, SOFTWARE registry hive, SOFTWARE registry hive, SOFTWARE registry hive (RegBack), SOFTWARE registry hive (RegBack), SOFTWARE registry transaction files, SOFTWARE registry transaction files, SYSTEM registry hive, SYSTEM registry hive, SYSTEM registry hive (RegBack), SYSTEM registry hive (RegBack), SYSTEM registry hive (RegBack), SYSTEM registry hive (RegBack), SYSTEM registry transaction files, SYSTEM registry transaction files, System Profile registry hive, System Profile registry hive, System Profile registry transaction files, System Profile registry transaction files, System Restore Points Registry Hives (XP), UsrClass.dat registry hive, UsrClass.dat registry transaction files"
    type: bool
  - name: MultiCommander
    description: "Multi Commander (by Andrew Rathbun): Multi Commander - Application Folder, Multi Commander - Config Folder, Multi Commander - Log File, Multi Commander - Log Folder, Multi Commander - UserData Folder"
    type: bool
  - name: NETCLRUsageLogs
    description: ".NET CLR UsageLogs (by Matias Davaro): .NET CLR UsageLogs"
    type: bool
  - name: NGINXLogs
    description: "NGINX Log Files (by Eric Capuano): NGINX Log Files"
    type: bool
  - name: NZBGet
    description: "NZBGet (by Andrew Rathbun): Usenet Clients - NZBGet Log File, Usenet Clients - NZBGet NZBs"
    type: bool
  - name: Nessus
    description: "Nessus (by Andrew Rathbun): Nessus Logs, Nessus Logs"
    type: bool
  - name: NewsbinPro
    description: "Newsbin Pro (by Andrew Rathbun): Usenet Clients - Newsbin Pro"
    type: bool
  - name: Newsleecher
    description: "Newsleecher (by Andrew Rathbun): Usenet Clients - Newsleecher"
    type: bool
  - name: Nicotine__
    description: "Nicotine++ (by Andrew Rathbun): Nicotine++ Buddyfileindex.db, Nicotine++ Buddyfiles.db, Nicotine++ Buddymtimes.db, Nicotine++ Buddystreams.db, Nicotine++ Buddywordindex.db, Nicotine++ Config Files, Nicotine++ Downloads.json, Nicotine++ Incomplete Downloads, Nicotine++ Logs, Nicotine++ Uploads.json, Nicotine++ User Shares"
    type: bool
  - name: Notepad__
    description: "Notepad++ Backups, recently searched/replaced terms and recently opened documents (by Banaanhangwagen and Matt Dawson): Notepad++ Config, Notepad++ Session, Notepad++ Unsaved Edits"
    type: bool
  - name: OfficeAutosave
    description: "Office Autosave (by Russ Taylor): Excel Autosave Location, Powerpoint Autosave Location, Publisher Autosave Location, Word Autosave Location"
    type: bool
  - name: OfficeDiagnostics
    description: "Office Diagnostics (by teddy-ROxPin): Office Diagnostics, Office Elevated Diagnostics"
    type: bool
  - name: OfficeDocumentCache
    description: "Office Document Cache (by Banaanhangwagen): Office Document Cache"
    type: bool
  - name: OneCommander
    description: "One Commander (by Andrew Rathbun): One Commander - All Configuration Files, One Commander - Other Configuration Files"
    type: bool
  - name: OneDrive_Metadata
    description: "Microsoft OneDrive Storage Metadata (by Chad Tilbury): OneDrive Metadata Logs, OneDrive Metadata Settings"
    type: bool
  - name: OneDrive_UserFiles
    description: "Microsoft OneDrive Storage Files (by Chad Tilbury): OneDrive User Files"
    type: bool
  - name: OpenSSHClient
    description: "OpenSSH Client config, known hosts and keys (by Matt Dawson): OpenSSH Config File, OpenSSH Default DSA Private Key, OpenSSH Default ECDSA Private Key, OpenSSH Default ECDSA-SK Private Key, OpenSSH Default ED25519 Private Key, OpenSSH Default ED25519-SK Private Key, OpenSSH Default RSA Private Key, OpenSSH Known Hosts, OpenSSH Public Keys"
    type: bool
  - name: OpenSSHServer
    description: "OpenSSH Server Config and Logs (by Matt Dawson): OpenSSH Authorized Administrator Keys, OpenSSH Host DSA Key, OpenSSH Host ECDSA Key, OpenSSH Host ED25519 Key, OpenSSH Host RSA Key, OpenSSH Server Config File, OpenSSH Server Logs, OpenSSH User Authorized Keys, OpenSSH User Authorized Keys 2"
    type: bool
  - name: OpenVPNClient
    description: "OpenVPN Client Config and Log (by Mathias Frank): OpenVPN Client Config, OpenVPN Client Config, OpenVPN Client Config"
    type: bool
  - name: Opera
    description: "Opera (by Andrew Rathbun): Opera - Local Folder, Opera - Roaming Folder"
    type: bool
  - name: OutlookPSTOST
    description: "Outlook PST and OST files (by Eric Zimmerman and Chad Tilbury): NST, OST, OST (2013 or 2016), OST XP, Outlook Attachment Temporary Storage, PST, PST (2013 or 2016), PST XP"
    type: bool
  - name: P2PClients
    description: "P2P Clients (by Andrew Rathbun): DC++ Chat Logs, FrostWire AppData, FrostWire AppData, FrostWire Downloads, Gigatribe Files Windows Vista/7/8/10, Gigatribe Files Windows XP, Gigatribe Files Windows XP, Shareaza Logs, Soulseek Chat Logs, Soulseek Search History/Shared Folders/Settings"
    type: bool
  - name: PeaZip
    description: "PeaZip (by Andrew Rathbun): PeaZip Configuration Files"
    type: bool
  - name: PowerShellConsole
    description: "PowerShell Console Log File (by Mike Cary): PowerShell Console Log"
    type: bool
  - name: Prefetch
    description: "Prefetch files (by Eric Zimmerman): Prefetch, Prefetch"
    type: bool
  - name: ProtonVPN
    description: "ProtonVPN (by Andrew Rathbun): ProtonVPN - Connection Logs"
    type: bool
  - name: PuffinSecureBrowser
    description: "Puffin Secure Browser (by Andrew Rathbun): Puffin - Autocomplete Data, Puffin - Cookies, Puffin - Image Cache, Puffin - Password (Encrypted), Puffin - Password Forms Data, Puffin - Subscription Data, Puffin - data.db"
    type: bool
  - name: Q_Dir
    description: "Q-Dir (by Andrew Rathbun): Q-Dir - .ini File, Q-Dir - .qdr file"
    type: bool
  - name: QFinderPro__QNAP_
    description: "QFinderPro (QNAP) (by Andrew Rathbun): QFinderPro"
    type: bool
  - name: RDPCache
    description: "RDP Cache Files (by Hadar Yudovich): RDP Cache Files, RDP Cache Files, Windows.old RDP Cache Files"
    type: bool
  - name: RDPLogs
    description: "RDP Logs (by Drew Ervin): LocalSessionManager Event Logs, LocalSessionManager Event Logs, RDPClient Event Logs, RDPClient Event Logs, RDPCoreTS Event Logs, RDPCoreTS Event Logs, RemoteConnectionManager Event Logs, RemoteConnectionManager Event Logs"
    type: bool
  - name: Radmin
    description: "Radmin Server/Viewer Logs and Chats (by Mathias Frank): Radmin Server 32bit Chats, Radmin Server 32bit Log, Radmin Server 64bit Chats, Radmin Server 64bit Log, Radmin Viewer Chats"
    type: bool
  - name: RecentFileCache
    description: "RecentFileCache (by Eric Zimmerman): RecentFileCache, RecentFileCache"
    type: bool
  - name: RecycleBin
    description: "Recycle Bin DataAndInfo (by Mark Hallman / Joshua Hickman): RECYCLER - WinXP, RECYCLER - WinXP, Recycle Bin - Windows Vista+, Recycle Bin - Windows Vista+, Recycle Bin - Windows Vista+"
    type: bool
  - name: RecycleBin_DataFiles
    description: "Recycle Bin Data Files (by Joshua Hickman, Andreas Hunkeler (@Karneades), Brian Maloney): RECYCLER - WinXP, Recycle Bin - Windows Vista+, Recycle Bin - Windows Vista+"
    type: bool
  - name: RecycleBin_InfoFiles
    description: "Recycle Bin Info Files (by Joshua Hickman, Andreas Hunkeler (@Karneades)): RECYCLER - WinXP, Recycle Bin - Windows Vista+"
    type: bool
  - name: RegistryHives
    description: "System and user related Registry hives (by Eric Zimmerman): Local Service registry hive, Local Service registry hive, Local Service registry transaction files, Local Service registry transaction files, NTUSER.DAT DEFAULT registry hive, NTUSER.DAT DEFAULT registry hive, NTUSER.DAT DEFAULT transaction files, NTUSER.DAT DEFAULT transaction files, NTUSER.DAT registry hive, NTUSER.DAT registry hive XP, NTUSER.DAT registry transaction files, Network Service registry hive, Network Service registry hive, Network Service registry transaction files, Network Service registry transaction files, RegBack registry transaction files, RegBack registry transaction files, SAM registry hive, SAM registry hive, SAM registry hive (RegBack), SAM registry hive (RegBack), SAM registry transaction files, SAM registry transaction files, SECURITY registry hive, SECURITY registry hive, SECURITY registry hive (RegBack), SECURITY registry hive (RegBack), SECURITY registry transaction files, SECURITY registry transaction files, SOFTWARE registry hive, SOFTWARE registry hive, SOFTWARE registry hive (RegBack), SOFTWARE registry hive (RegBack), SOFTWARE registry transaction files, SOFTWARE registry transaction files, SYSTEM registry hive, SYSTEM registry hive, SYSTEM registry hive (RegBack), SYSTEM registry hive (RegBack), SYSTEM registry hive (RegBack), SYSTEM registry hive (RegBack), SYSTEM registry transaction files, SYSTEM registry transaction files, System Profile registry hive, System Profile registry hive, System Profile registry transaction files, System Profile registry transaction files, System Restore Points Registry Hives (XP), UsrClass.dat registry hive, UsrClass.dat registry transaction files"
    type: bool
  - name: RegistryHivesOther
    description: "Other Registry Hives (by Andrew Rathbun): BBI registry hive, BBI registry hive, BBI registry transaction files, BBI registry transaction files, BCD-Template registry hive, BCD-Template registry hive, BCD-Template registry transaction files, BCD-Template registry transaction files, COMPONENTS registry hive, COMPONENTS registry hive, COMPONENTS registry transaction files, COMPONENTS registry transaction files, DRIVERS registry hive, DRIVERS registry hive, DRIVERS registry transaction files, DRIVERS registry transaction files, ELAM registry hive, ELAM registry hive, ELAM registry transaction files, ELAM registry transaction files, VSMIDK registry hive, VSMIDK registry hive, VSMIDK registry transaction files, VSMIDK registry transaction files, userdiff registry hive, userdiff registry hive, userdiff registry transaction files, userdiff registry transaction files"
    type: bool
  - name: RegistryHivesSystem
    description: "System level/related Registry hives (by Eric Zimmerman / Mark Hallman): Local Service registry hive, Local Service registry hive, Local Service registry transaction files, Local Service registry transaction files, Network Service registry hive, Network Service registry hive, Network Service registry transaction files, Network Service registry transaction files, RegBack registry transaction files, RegBack registry transaction files, SAM registry hive, SAM registry hive, SAM registry hive (RegBack), SAM registry hive (RegBack), SAM registry transaction files, SAM registry transaction files, SECURITY registry hive, SECURITY registry hive, SECURITY registry hive (RegBack), SECURITY registry hive (RegBack), SECURITY registry transaction files, SECURITY registry transaction files, SOFTWARE registry hive, SOFTWARE registry hive, SOFTWARE registry hive (RegBack), SOFTWARE registry hive (RegBack), SOFTWARE registry transaction files, SOFTWARE registry transaction files, SYSTEM registry hive, SYSTEM registry hive, SYSTEM registry hive (RegBack), SYSTEM registry hive (RegBack), SYSTEM registry hive (RegBack), SYSTEM registry hive (RegBack), SYSTEM registry transaction files, SYSTEM registry transaction files, System Profile registry hive, System Profile registry hive, System Profile registry transaction files, System Profile registry transaction files, System Restore Points Registry Hives (XP)"
    type: bool
  - name: RegistryHivesUser
    description: "User Related Registry hives (by Eric Zimmerman / Mark Hallman): NTUSER.DAT DEFAULT registry hive, NTUSER.DAT DEFAULT registry hive, NTUSER.DAT DEFAULT transaction files, NTUSER.DAT DEFAULT transaction files, NTUSER.DAT registry hive, NTUSER.DAT registry hive XP, NTUSER.DAT registry transaction files, UsrClass.dat registry hive, UsrClass.dat registry transaction files"
    type: bool
  - name: RemoteAdmin
    description: "Composite target for files related to remote administration tools (by Drew Ervin, Mathias Frank, Andrew Rathbun): Ammyy Program Data, AnyDesk Chat Logs - User Profile, AnyDesk Logs - ProgramData - *.conf, AnyDesk Logs - ProgramData - *.trace, AnyDesk Logs - ProgramData - connection_trace.txt, AnyDesk Logs - System User Account, AnyDesk Logs - User Profile - *.conf, AnyDesk Logs - User Profile - *.trace, AnyDesk Logs - User Profile - connection_trace.txt, AnyDesk Videos, Application Event Log Win7+, Application Event Log Win7+, Application Event Log XP, Application Event Log XP, Kaseya Agent Edge Service Logs, Kaseya Agent Endpoint Service Logs, Kaseya Agent Endpoint Service Logs (XP), Kaseya Agent Service Log, Kaseya Live Connect Logs, Kaseya Live Connect Logs (XP), Kaseya Setup Log, Kaseya Setup Log, Kaseya Setup Log, LocalSessionManager Event Logs, LocalSessionManager Event Logs, LogMeIn Application Logs, LogMeIn ProgramData Logs, RDP Cache Files, RDP Cache Files, RDPClient Event Logs, RDPClient Event Logs, RDPCoreTS Event Logs, RDPCoreTS Event Logs, Radmin Server 32bit Chats, Radmin Server 32bit Log, Radmin Server 64bit Chats, Radmin Server 64bit Log, Radmin Viewer Chats, RealVNC Log, RemoteConnectionManager Event Logs, RemoteConnectionManager Event Logs, RemoteUtilities Connection Logs, RemoteUtilities Install Log, ScreenConnect Session Database, ScreenConnect Session Database, ScreenConnect User Config, Splashtop Log Files, Splashtop Log Files in ProgramData, Supremo Connection Logs, Supremo File Transfer Inbox, TeamViewer Application Logs, TeamViewer Configuration Files, TeamViewer Connection Logs, UltraViewer Logs, UltraViewer Logs, UltraViewer Logs, Windows.old RDP Cache Files, Zoho Assist .conf files, Zoho Assist .conf files in  Program Files*, Zoho Assist .conf files in AppData\Local, Zoho Assist .txt files in  Program Files*, Zoho Assist log files in AppData\Local, Zoho Assist log files in Program Files*, Zoho Assist log files in ProgramData, mRemoteNG Connection Configuration and Backups, mRemoteNG Logs, mRemoteNG Program Settings"
    type: bool
  - name: RemoteUtilities_app
    description: "Remote Utilities (by Ryan McVicar): RemoteUtilities Connection Logs, RemoteUtilities Install Log"
    type: bool
  - name: RoamingProfile
    description: "User Related Registry Hives, LNK files, etc (by Scott Downie): Amcache, Amcache transaction files, Chrome Cookies, Chrome Cookies, Chrome Current Session, Chrome Current Session, Chrome Current Tabs, Chrome Current Tabs, Chrome Download Metadata, Chrome Download Metadata, Chrome Extension Cookies, Chrome Extension Cookies, Chrome Favicons, Chrome Favicons, Chrome History, Chrome History, Chrome Last Session, Chrome Last Session, Chrome Last Tabs, Chrome Last Tabs, Chrome Login Data, Chrome Login Data, Chrome Media History, Chrome Media History, Chrome Network Action Predictor, Chrome Network Action Predictor, Chrome Network Persistent State, Chrome Network Persistent State, Chrome Preferences, Chrome Preferences, Chrome Quota Manager, Chrome Quota Manager, Chrome Reporting and NEL, Chrome Reporting and NEL, Chrome Sessions Folder, Chrome Sessions Folder, Chrome Shortcuts, Chrome Shortcuts, Chrome SyncData Database, Chrome SyncData Database, Chrome Top Sites, Chrome Top Sites, Chrome Trust Tokens, Chrome Trust Tokens, Chrome Visited Links, Chrome Visited Links, Chrome Web Data, Chrome Web Data, Chrome bookmarks, Chrome bookmarks, Desktop LNK Files, Edge folder, Edge folder, Excel Autosave Location, LNK Files, LNK Files from Microsoft Office Recent, LNK Files from Microsoft Office Recent, LNK Files from Recent, LNK Files from Recent, NTUSER.DAT DEFAULT registry hive, NTUSER.DAT DEFAULT transaction files, NTUSER.DAT registry hive, NTUSER.DAT registry transaction files, Office Document Cache, Office Document Cache, PowerPoint Autosave Location, Publisher Autosave Location, Publisher Autosave Location, UsrClass.dat registry hive, UsrClass.dat registry transaction files, Windows Protect Folder, Windows Protect Folder, Word Autosave Location"
    type: bool
  - name: RogueKiller
    description: "RogueKiller Anti-Malware (by Adlice Software) (by Drew Ervin): RogueKiller Reports"
    type: bool
  - name: SABnbzd
    description: "SABnbzd (by Andrew Rathbun): Usenet Clients - SABnzbd Download Logs, Usenet Clients - SABnzbd History.db"
    type: bool
  - name: SDB
    description: "Shim SDB FIles (by Troy Larson): SDB Files, SDB Files, SDB Files x64, SDB Files x64"
    type: bool
  - name: SOFELK
    description: "SOF-ELK related files of interest (by Tony Knutson and Andrew Rathbun): $Boot, $J, $J, $LogFile, $MFT, $Max, $Max, $T, $T, Amcache, Amcache, Amcache transaction files, Amcache transaction files, AppCompat PCA Folder, Desktop LNK Files, Desktop LNK Files XP, Event logs Win7+, Event logs Win7+, Event logs XP, LNK Files from C:\ProgramData, LNK Files from Microsoft Office Recent, LNK Files from Recent, LNK Files from Recent (XP), Prefetch, Prefetch, RecentFileCache, RecentFileCache, Restore point LNK Files XP, Start Menu LNK Files, Syscache, Syscache transaction files"
    type: bool
  - name: SQLiteDatabases
    description: "SQLDatabases Target for use with SQLECmd Module (by Andrew Rathbun): 4K Video Downloader, ActivitiesCache.db, Addons, Bitdefender SQLite DB Files, Bookmarks, Chrome Cookies, Chrome Cookies XP, Chrome Current Session, Chrome Current Session XP, Chrome Current Tabs, Chrome Current Tabs XP, Chrome Download Metadata, Chrome Extension Cookies, Chrome Favicons, Chrome Favicons XP, Chrome History, Chrome History XP, Chrome Last Session, Chrome Last Session XP, Chrome Last Tabs, Chrome Last Tabs XP, Chrome Login Data, Chrome Login Data XP, Chrome Media History, Chrome Network Action Predictor, Chrome Network Persistent State, Chrome Preferences, Chrome Preferences XP, Chrome Quota Manager, Chrome Reporting and NEL, Chrome Shortcuts, Chrome Shortcuts XP, Chrome SyncData Database, Chrome Top Sites, Chrome Top Sites XP, Chrome Trust Tokens, Chrome Visited Links, Chrome Visited Links XP, Chrome Web Data, Chrome Web Data XP, Chrome bookmarks, Chrome bookmarks XP, Cookies, Cookies, Downloads, Dropbox Metadata, Dropbox Metadata, Dropbox Metadata, Dropbox Metadata, Dropbox Metadata, Dropbox Metadata, Dropbox Metadata, Dropbox Metadata, Dropbox Metadata, Dropbox Metadata, Dropbox Metadata, Edge Bookmarks, Edge Collections, Edge Cookies, Edge Current Session, Edge Current Tabs, Edge Favicons, Edge History, Edge Last Session, Edge Last Tabs, Edge Login Data, Edge Media History, Edge Network Action Predictor, Edge Preferences, Edge Shortcuts, Edge SyncData Database, Edge Top Sites, Edge Visited Links, Edge Web Data, Edge bookmarks, EventTranscript.db, EventTranscript.db, Favicons, FileZilla SQLite3 Log Files, Form history, Google File Stream Metadata, Google File Stream Metadata, Google File Stream Metadata, Google File Stream Metadata, Microsoft OneNote - AccessibilityCheckerIndex, Microsoft OneNote - FullTextSearchIndex, Microsoft OneNote - RecentNotebooks_SeenURLs, Microsoft OneNote - RecentSearches, Microsoft OneNote - User NoteTags, Microsoft Sticky Notes - 1607 and later, Microsoft To Do - SQLite Database of To Do tasks, Permissions, Places, Protections, Search, Signons, Storage Sync, TeraCopy - History Databases, TeraCopy - Main Database, Update Store.db, Webappstore, Windows 10 Notification DB, Windows 10 Notification DB"
    type: bool
  - name: SRUM
    description: "System Resource Usage Monitor (SRUM) Data (by Mark Hallman): SOFTWARE registry hive, SOFTWARE registry hive, SOFTWARE registry transaction files, SOFTWARE registry transaction files, SRUM, SRUM"
    type: bool
  - name: SUM
    description: "SUM Database (by Andrew Rathbun): SUM Database (.mdb files)"
    type: bool
  - name: SUPERAntiSpyware
    description: "SUPERAntiSpyware Data (by Drew Ervin): SUPERAntiSpyware Logs"
    type: bool
  - name: SUSELinuxEnterpriseServer
    description: "SUSE Linux Enterprise Server on Windows Subsystem for Linux (by Matt Dawson): SUSE Linux Enterprise Server WSL .bash_history, SUSE Linux Enterprise Server WSL .bashrc, SUSE Linux Enterprise Server WSL .profile, SUSE Linux Enterprise Server WSL /etc/bash.bashrc, SUSE Linux Enterprise Server WSL /etc/fstab, SUSE Linux Enterprise Server WSL /etc/group, SUSE Linux Enterprise Server WSL /etc/hostname, SUSE Linux Enterprise Server WSL /etc/hosts, SUSE Linux Enterprise Server WSL /etc/os-release, SUSE Linux Enterprise Server WSL /etc/passwd, SUSE Linux Enterprise Server WSL /etc/profile, SUSE Linux Enterprise Server WSL /etc/shadow, SUSE Linux Enterprise Server WSL /etc/timezone, SUSE Linux Enterprise Server WSL ext4.vhdx"
    type: bool
  - name: ScheduledTasks
    description: "Scheduled tasks (*.job and XML) (by Eric Zimmerman): XML, XML, at .job, at .job, at SchedLgU.txt, at SchedLgU.txt"
    type: bool
  - name: ScreenConnect
    description: "ScreenConnect Data (now known as ConnectWise Control) (by Drew Ervin): Application Event Log Win7+, Application Event Log Win7+, Application Event Log XP, Application Event Log XP, ScreenConnect Session Database, ScreenConnect Session Database, ScreenConnect User Config"
    type: bool
  - name: SecureAge
    description: "SecureAge Antivirus Logs (by Andrew Rathbun): SecureAge Antvirus Logs"
    type: bool
  - name: SentinelOne
    description: "Sentinel One Logs (by Kirtan Shah): SentinelOne EDR Log"
    type: bool
  - name: ServerTriage
    description: "A compound target for gathering artifacts common to servers. (by Eric Capuano): Apache Access Log, Confluence Wiki Log Files, Confluence Wiki Log Files, Exchange TransportRoles log files, Exchange client access log files, FileZilla Log Files, FileZilla Server XML Log Files, IIS log files, IIS log files, IIS log files, IIS log files, IIS log files, IIS log files, MS SQL Errorlog, MS SQL Errorlogs, ManageEngine Desktop Central Log Files, NGINX Log Files, OpenSSH Authorized Administrator Keys, OpenSSH Host DSA Key, OpenSSH Host ECDSA Key, OpenSSH Host ED25519 Key, OpenSSH Host RSA Key, OpenSSH Server Config File, OpenSSH Server Logs, OpenSSH User Authorized Keys, OpenSSH User Authorized Keys 2"
    type: bool
  - name: ShareX
    description: "ShareX (by Andrew Rathbun): ShareX"
    type: bool
  - name: Shareaza
    description: "Shareaza (by Andrew Rathbun): Shareaza Logs"
    type: bool
  - name: SiemensTIA
    description: "Copy Siemens TIA Settings (by Olaf Schwarz (@b00010111)): Siemens TIA Settings"
    type: bool
  - name: Signal
    description: "Signal (Please view this tkape file for documentation on decryption!) (by Matt Dawson): Signal Attachments cache, Signal Database, Signal Logs, Signal config.json"
    type: bool
  - name: SignatureCatalog
    description: "Obtain detached signature catalog files (by Mike Pilkington): SignatureCatalog, SignatureCatalog"
    type: bool
  - name: Skype
    description: "Skype (by Eric Zimmerman, Matt Dawson): Skype for Destkop v8+ Chromium Cache, leveldb (Skype for Desktop +v8), main.db (App <v12), main.db Win7+, main.db XP, s4l-[username].db (App +v8), skype.db (App +v12)"
    type: bool
  - name: Slack
    description: "Slack (by Andrew Rathbun and Chad Tilbury): Slack - Chat Logs, Slack Cache, Slack Electron Logs, Slack LevelDB Files, Slack Storage"
    type: bool
  - name: Snagit
    description: "Snagit (by Andrew Rathbun): Snagit - Captures"
    type: bool
  - name: SnipAndSketch
    description: "Snip & Sketch Cached Images (by Kevin Pagano): Snip & Sketch"
    type: bool
  - name: Sophos
    description: "Sophos Data (by Drew Ervin): Application Event Log Win7+, Application Event Log Win7+, Application Event Log XP, Application Event Log XP, Sophos Logs, Sophos Logs (XP)"
    type: bool
  - name: Soulseek
    description: "Soulseek (by Andrew Rathbun): Soulseek Chat Logs, Soulseek Search History/Shared Folders/Settings"
    type: bool
  - name: SpeedCommander
    description: "SpeedCommander (by Andrew Rathbun): SpeedCommander - .ini File"
    type: bool
  - name: Splashtop
    description: "Splashtop (by Andrew Rathbun, Yogesh Khatri): Splashtop Log Files, Splashtop Log Files in ProgramData"
    type: bool
  - name: StartupFolders
    description: "Startup Folders (by Jason Ballard): System-wide startup folder, User startup folders"
    type: bool
  - name: StartupInfo
    description: "StartupInfo XML Files (by Hadar Yudovich): StartupInfo XML Files, StartupInfo XML Files"
    type: bool
  - name: SublimeText
    description: "Sublime Text 2/3 Auto Save Session (by Mathias Frank): SublimeText 2/3 Auto Save Session"
    type: bool
  - name: SugarSync
    description: "SugarSync (by Andrew Rathbun): SugarSync - My SugarSync (Default Location), SugarSync - Shared Folders (Default Location), SugarSync Log File"
    type: bool
  - name: SumatraPDF
    description: "SumatraPDF (by Andrew Rathbun): SumatraPDF Cache, SumatraPDF Settings - SessionData"
    type: bool
  - name: SupremoRemoteDesktop
    description: "Supremo Remote Desktop Control Logs (by Sandro Heckendorn): Supremo Connection Logs, Supremo File Transfer Inbox"
    type: bool
  - name: Symantec_AV_Logs
    description: "Symantec AV Logs (by Brian Maloney): Application Event Log Win7+, Application Event Log Win7+, Application Event Log XP, Application Event Log XP, Symantec Endpoint Protection Logs, Symantec Endpoint Protection Logs (XP), Symantec Endpoint Protection Quarantine, Symantec Endpoint Protection Quarantine (XP), Symantec Endpoint Protection User Logs, Symantec Event Log Win7+, Symantec Event Log Win7+, ccSubSDK Database, registrationInfo.xml"
    type: bool
  - name: Syscache
    description: "syscache.hve (by Phill Moore): Syscache, Syscache transaction files"
    type: bool
  - name: TablacusExplorer
    description: "Tablacus Explorer (by Andrew Rathbun): Tablacus Explorer - remember.xml, Tablacus Explorer - window.xml, Tablacus Explorer - window1.xml"
    type: bool
  - name: TeamViewerLogs
    description: "TeamViewer Logs (by Hadar Yudovich): TeamViewer Application Logs, TeamViewer Configuration Files, TeamViewer Connection Logs"
    type: bool
  - name: Telegram
    description: "Telegram Desktop (by Simone Marinari): Telegram app folder, Telegram downloaded files"
    type: bool
  - name: TeraCopy
    description: "TeraCopy log history (by Kevin Pagano): TeraCopy"
    type: bool
  - name: ThumbCache
    description: "Thumbcache DB (by Eric Zimmerman): Thumbcache DB"
    type: bool
  - name: Thunderbird
    description: "Mozilla Thunderbird Email Client (by Matt Dawson): Mozilla Thunderbird Address Book, Mozilla Thunderbird Attachments, Mozilla Thunderbird Calendar Data, Mozilla Thunderbird Global Messages Database, Mozilla Thunderbird ImapMail INBOX, Mozilla Thunderbird Install Date, Mozilla Thunderbird Mail INBOX, Mozilla Thunderbird Profiles.ini, Mozilla Thunderbird logins.json, Mozilla Thunderbird places.sqlite, Mozilla Thunderbird prefs.js"
    type: bool
  - name: TorrentClients
    description: "Torrent Clients (by Andrew Rathbun): TorrentClients - BitTorrent, TorrentClients - qBittorrent, TorrentClients - qBittorrent, TorrentClients - uTorrent"
    type: bool
  - name: Torrents
    description: "Torrent Files (by Tony Knutson): Torrents"
    type: bool
  - name: TotalAV
    description: "TotalAV Antivirus Data (by Kirtan Shah): TotalAV Logs, TotalAV Logs"
    type: bool
  - name: TotalCommander
    description: "Total Commander (by Andrew Rathbun and Jessica Venturo): Total Commander - .ini File, Total Commander - FTP .ini File, Total Commander - FTP Logs, Total Commander - File Tree, Total Commander - Log File, Total Commander - Temp Files Created During Folder Traversal"
    type: bool
  - name: TreeSize
    description: "TreeSize - Scan History (by Andrew Rathbun): TreeSize - ScanHistory.XML"
    type: bool
  - name: TrendMicro
    description: "Trend Micro Data (by Drew Ervin): Trend Micro Logs, Trend Micro Security Agent Connection Logs, Trend Micro Security Agent Report Logs"
    type: bool
  - name: USBDetective
    description: "Collects files that can be input into USB Detective for parsing (by Kevin Pagano): Amcache, Amcache, Amcache transaction files, Amcache transaction files, Desktop LNK Files, Desktop LNK Files XP, Event logs Win7+, Event logs Win7+, Event logs XP, LNK Files from C:\ProgramData, LNK Files from Microsoft Office Recent, LNK Files from Recent, LNK Files from Recent (XP), Local Service registry hive, Local Service registry hive, Local Service registry transaction files, Local Service registry transaction files, NTUSER.DAT DEFAULT registry hive, NTUSER.DAT DEFAULT registry hive, NTUSER.DAT DEFAULT transaction files, NTUSER.DAT DEFAULT transaction files, NTUSER.DAT registry hive, NTUSER.DAT registry hive XP, NTUSER.DAT registry transaction files, Network Service registry hive, Network Service registry hive, Network Service registry transaction files, Network Service registry transaction files, RegBack registry transaction files, RegBack registry transaction files, Restore point LNK Files XP, SAM registry hive, SAM registry hive, SAM registry hive (RegBack), SAM registry hive (RegBack), SAM registry transaction files, SAM registry transaction files, SECURITY registry hive, SECURITY registry hive, SECURITY registry hive (RegBack), SECURITY registry hive (RegBack), SECURITY registry transaction files, SECURITY registry transaction files, SOFTWARE registry hive, SOFTWARE registry hive, SOFTWARE registry hive (RegBack), SOFTWARE registry hive (RegBack), SOFTWARE registry transaction files, SOFTWARE registry transaction files, SYSTEM registry hive, SYSTEM registry hive, SYSTEM registry hive (RegBack), SYSTEM registry hive (RegBack), SYSTEM registry hive (RegBack), SYSTEM registry hive (RegBack), SYSTEM registry transaction files, SYSTEM registry transaction files, Setupapi.log Win7+, Setupapi.log Win7+, Setupapi.log XP, Start Menu LNK Files, System Profile registry hive, System Profile registry hive, System Profile registry transaction files, System Profile registry transaction files, System Restore Points Registry Hives (XP), UsrClass.dat registry hive, UsrClass.dat registry transaction files"
    type: bool
  - name: USBDevicesLogs
    description: "USB devices log files (by Eric Zimmerman): Setupapi.log Win7+, Setupapi.log Win7+, Setupapi.log XP"
    type: bool
  - name: Ubuntu
    description: "Ubuntu on Windows Subsystem for Linux (by Matt Dawson): Ubuntu WSL .bash_history, Ubuntu WSL .bashrc, Ubuntu WSL .profile, Ubuntu WSL /etc/bash.bashrc, Ubuntu WSL /etc/crontab, Ubuntu WSL /etc/fstab, Ubuntu WSL /etc/group, Ubuntu WSL /etc/hostname, Ubuntu WSL /etc/hosts, Ubuntu WSL /etc/os-release, Ubuntu WSL /etc/passwd, Ubuntu WSL /etc/profile, Ubuntu WSL /etc/shadow, Ubuntu WSL /etc/timezone, Ubuntu WSL Apt Logs, Ubuntu WSL User Crontabs, Ubuntu WSL ext4.vhdx"
    type: bool
  - name: Ultraviewer
    description: "UltraViewer (by Ryan McVicar): UltraViewer Logs, UltraViewer Logs, UltraViewer Logs"
    type: bool
  - name: Usenet
    description: "Usenet (NZB) Files (by Andrew Rathbun): Usenet (NZB) Files"
    type: bool
  - name: UsenetClients
    description: "Usenet Clients (by Andrew Rathbun): Usenet Clients - NZBGet Log File, Usenet Clients - NZBGet NZBs, Usenet Clients - Newsbin Pro, Usenet Clients - Newsleecher, Usenet Clients - SABnzbd Download Logs, Usenet Clients - SABnzbd History.db"
    type: bool
  - name: VIPRE
    description: "VIPRE Data (by Drew Ervin): VIPRE Business Agent Logs, VIPRE Business User Logs (up to v4), VIPRE Business User Logs (v5-v6), VIPRE Business User Logs (v7+)"
    type: bool
  - name: VLC_Media_Player
    description: "VLC Media Player (by Matt Dawson): VLC Recently Opened Files, VLC Recorded Files"
    type: bool
  - name: VMware
    description: "Runs all VMware modules to collect VMware VM config files, logs and Virtual Hard Disks (by Matt Dawson): VDI, VHD, VHDX, VMDK, VMware (Fusion/Workstation/Server/Player), VMware (Fusion/Workstation/Server/Player), VMware (Fusion/Workstation/Server/Player), VMware - Virtual Machine Inventory"
    type: bool
  - name: VMwareInventory
    description: "VMware - Virtual Machine Inventory (by Andrew Rathbun): VMware - Virtual Machine Inventory"
    type: bool
  - name: VMwareMemory
    description: "VMware - Virtual Machine Memory (by Andrew Rathbun): VMware (Fusion/Workstation/Server/Player), VMware (Fusion/Workstation/Server/Player), VMware (Fusion/Workstation/Server/Player)"
    type: bool
  - name: VNCLogs
    description: "VNC Logs (by Phill Moore): Application Event Log Win7+, Application Event Log Win7+, Application Event Log XP, Application Event Log XP, RealVNC Log"
    type: bool
  - name: Viber
    description: "ViberPC Messaging App (by Matt Dawson): Viber Config Database, Viber Users Avatars Cache, Viber Users Backgrounds Cache, Viber Users Data Database, Viber Users Thumbnails Cache"
    type: bool
  - name: VirtualBox
    description: "Runs all VirtualBox modules to collect Virtualbox VM config files, logs and Virtual Hard Disks (by Matt Dawson): VDI, VHD, VHDX, VMDK, VirtualBox, VirtualBox Backup Logs, VirtualBox Hardening Logs, VirtualBox Logs, VirtualBox VM backup configs, VirtualBox VM configs"
    type: bool
  - name: VirtualBoxConfig
    description: "Collects VirtualBox configuration files (by Matt Dawson): VirtualBox VM backup configs, VirtualBox VM configs"
    type: bool
  - name: VirtualBoxLogs
    description: "Collects VirtualBox log files (by Matt Dawson): VirtualBox Backup Logs, VirtualBox Hardening Logs, VirtualBox Logs"
    type: bool
  - name: VirtualBoxMemory
    description: "VirtualBox - Memory (by Andrew Rathbun): VirtualBox"
    type: bool
  - name: VirtualDisks
    description: "Virtual Disks (by Phill Moore): VDI, VHD, VHDX, VMDK"
    type: bool
  - name: WBEM
    description: "Web-Based Enterprise Management (WBEM) (by Mark Hallman): WBEM, WBEM"
    type: bool
  - name: WER
    description: "Windows Error Reporting (by Troy Larson): Crash Dumps, Crash Dumps, Crash Dumps, WER Files"
    type: bool
  - name: WSL
    description: "All Windows Subsystem for Linux targets (by Matt Dawson): Debian WSL .bash_history, Debian WSL .bashrc, Debian WSL .profile, Debian WSL /etc/bash.bashrc, Debian WSL /etc/crontab, Debian WSL /etc/debian_version, Debian WSL /etc/fstab, Debian WSL /etc/group, Debian WSL /etc/hostname, Debian WSL /etc/hosts, Debian WSL /etc/os-release, Debian WSL /etc/passwd, Debian WSL /etc/profile, Debian WSL /etc/shadow, Debian WSL /etc/timezone, Debian WSL Apt Logs, Debian WSL User Crontabs, Debian WSL ext4.vhdx, Kali WSL .bash_history, Kali WSL .bashrc, Kali WSL .profile, Kali WSL /etc/bash.bashrc, Kali WSL /etc/crontab, Kali WSL /etc/debian_version, Kali WSL /etc/fstab, Kali WSL /etc/group, Kali WSL /etc/hostname, Kali WSL /etc/hosts, Kali WSL /etc/os-release, Kali WSL /etc/passwd, Kali WSL /etc/profile, Kali WSL /etc/shadow, Kali WSL /etc/timezone, Kali WSL Apt Logs, Kali WSL User Crontabs, Kali WSL ext4.vhdx, SUSE Linux Enterprise Server WSL .bash_history, SUSE Linux Enterprise Server WSL .bashrc, SUSE Linux Enterprise Server WSL .profile, SUSE Linux Enterprise Server WSL /etc/bash.bashrc, SUSE Linux Enterprise Server WSL /etc/fstab, SUSE Linux Enterprise Server WSL /etc/group, SUSE Linux Enterprise Server WSL /etc/hostname, SUSE Linux Enterprise Server WSL /etc/hosts, SUSE Linux Enterprise Server WSL /etc/os-release, SUSE Linux Enterprise Server WSL /etc/passwd, SUSE Linux Enterprise Server WSL /etc/profile, SUSE Linux Enterprise Server WSL /etc/shadow, SUSE Linux Enterprise Server WSL /etc/timezone, SUSE Linux Enterprise Server WSL ext4.vhdx, Ubuntu WSL .bash_history, Ubuntu WSL .bashrc, Ubuntu WSL .profile, Ubuntu WSL /etc/bash.bashrc, Ubuntu WSL /etc/crontab, Ubuntu WSL /etc/fstab, Ubuntu WSL /etc/group, Ubuntu WSL /etc/hostname, Ubuntu WSL /etc/hosts, Ubuntu WSL /etc/os-release, Ubuntu WSL /etc/passwd, Ubuntu WSL /etc/profile, Ubuntu WSL /etc/shadow, Ubuntu WSL /etc/timezone, Ubuntu WSL Apt Logs, Ubuntu WSL User Crontabs, Ubuntu WSL ext4.vhdx, openSUSE WSL .bash_history, openSUSE WSL .bashrc, openSUSE WSL .profile, openSUSE WSL /etc/bash.bashrc, openSUSE WSL /etc/fstab, openSUSE WSL /etc/group, openSUSE WSL /etc/hostname, openSUSE WSL /etc/hosts, openSUSE WSL /etc/os-release, openSUSE WSL /etc/passwd, openSUSE WSL /etc/profile, openSUSE WSL /etc/shadow, openSUSE WSL /etc/timezone, openSUSE WSL ext4.vhdx"
    type: bool
  - name: WebBrowsers
    description: "Web browser history, bookmarks, etc. (by Eric Zimmerman): Addons, Addons XP, Bookmarks, Bookmarks, Bookmarks, Chrome Cookies, Chrome Cookies XP, Chrome Current Session, Chrome Current Session XP, Chrome Current Tabs, Chrome Current Tabs XP, Chrome Download Metadata, Chrome Extension Cookies, Chrome Favicons, Chrome Favicons XP, Chrome History, Chrome History XP, Chrome Last Session, Chrome Last Session XP, Chrome Last Tabs, Chrome Last Tabs XP, Chrome Login Data, Chrome Login Data XP, Chrome Media History, Chrome Network Action Predictor, Chrome Network Persistent State, Chrome Preferences, Chrome Preferences XP, Chrome Quota Manager, Chrome Reporting and NEL, Chrome Sessions Folder, Chrome Shortcuts, Chrome Shortcuts XP, Chrome SyncData Database, Chrome Top Sites, Chrome Top Sites XP, Chrome Trust Tokens, Chrome Visited Links, Chrome Visited Links XP, Chrome Web Data, Chrome Web Data XP, Chrome bookmarks, Chrome bookmarks XP, Cookies, Cookies, Cookies, Cookies XP, Current Session, Current Tabs, Download Metadata, Downloads, Downloads XP, Edge Bookmarks, Edge Collections, Edge Cookies, Edge Current Session, Edge Current Tabs, Edge Favicons, Edge History, Edge Last Session, Edge Last Tabs, Edge Login Data, Edge Media History, Edge Network Action Predictor, Edge Preferences, Edge Sessions Folder, Edge Shortcuts, Edge Snapshots Folder, Edge SyncData Database, Edge Top Sites, Edge Visited Links, Edge Web Data, Edge bookmarks, Edge folder, Extensions, Favicons, Favicons, Favicons XP, Form history, Form history XP, History, IE 11 Cookies, IE 11 Metadata, IE 9/10 Cookies, IE 9/10 Download History, IE 9/10 History, Index.dat History, Index.dat History subdirectory, Index.dat Office, Index.dat Office XP, Index.dat UserData, Index.dat cookies, Local Internet Explorer folder, Login Data, Network Action Predictor, Network Persistent State, Opera - Local Folder, Opera - Roaming Folder, Password, Password, Password, Password XP, Password XP, Password XP, Permissions, Places, Places XP, Preferences, Preferences, Protections, Publisher Info DB/Brave Rewards, Puffin - Autocomplete Data, Puffin - Cookies, Puffin - Image Cache, Puffin - Password (Encrypted), Puffin - Password Forms Data, Puffin - Subscription Data, Puffin - data.db, Quota Manager, Reporting and NEL, Roaming Internet Explorer folder, Search, Search XP, Secure Preferences, Sessions Folder, Sessionstore, Sessionstore Folder, Sessionstore XP, Shortcuts, Signons, Signons XP, Storage Sync, Top Sites, Visited Links, Web Data, Webappstore, Webappstore XP, Windows Protect Folder, Windows Protect Folder"
    type: bool
  - name: WebServers
    description: "Logs from all known web server applications and supporting services (by Eric Capuano): Apache Access Log, IIS log files, IIS log files, IIS log files, IIS log files, IIS log files, IIS log files, MS SQL Errorlog, MS SQL Errorlogs, NGINX Log Files"
    type: bool
  - name: Webroot
    description: "Webroot Antivirus (by Drew Ervin): Webroot Program Data"
    type: bool
  - name: WhatsApp
    description: "WhatsApp Local Files (by Matt Dawson): WhatsApp Cache, WhatsApp Local Storage"
    type: bool
  - name: WinDefendDetectionHist
    description: "Windows Defender Threat DetectionHistory files (by Jordan Klepser): DetectionHistory"
    type: bool
  - name: WinSCP
    description: "WinSCP (by Andrew Rathbun): WinSCP (.ini file)"
    type: bool
  - name: WindowsDefender
    description: "Windows Defender Data (by Drew Ervin): Windows Defender Event Logs, Windows Defender Event Logs, Windows Defender Logs, Windows Defender Logs, Windows Defender Logs, Windows Defender Logs"
    type: bool
  - name: WindowsFirewall
    description: "Windows Firewall Logs (by Mike Cary): Windows Firewall Logs, Windows Firewall Logs"
    type: bool
  - name: WindowsHello
    description: "Windows Hello (by Kevin Pagano): Cryptokeys, Masterkey, NGC, SECURITY registry hive, SECURITY registry hive, SECURITY registry hive (RegBack), SECURITY registry hive (RegBack), SECURITY registry transaction files, SECURITY registry transaction files, SOFTWARE registry hive, SOFTWARE registry hive, SOFTWARE registry hive (RegBack), SOFTWARE registry hive (RegBack), SOFTWARE registry transaction files, SOFTWARE registry transaction files, SYSTEM registry hive, SYSTEM registry hive, SYSTEM registry hive (RegBack), SYSTEM registry hive (RegBack), SYSTEM registry hive (RegBack), SYSTEM registry hive (RegBack), SYSTEM registry transaction files, SYSTEM registry transaction files"
    type: bool
  - name: WindowsIndexSearch
    description: "Windows Index Search (by Mark Hallman): GatherLogs, WindowsIndexSearch"
    type: bool
  - name: WindowsNotificationsDB
    description: "Windows 10 Notification DB (by Hadar Yudovich): Windows 10 Notification DB, Windows 10 Notification DB"
    type: bool
  - name: WindowsOSUpgradeArtifacts
    description: "Windows OS Upgrade Artifacts (by Andrew Rathbun): FolderMoveLog.txt, HumanReadable.xml, MigLog.xml, Setupact.log, Update Store.db"
    type: bool
  - name: WindowsPowerDiagnostics
    description: "Windows Power Diagnostics (by Andrew Rathbun): Windows Power Diagnostics"
    type: bool
  - name: WindowsSubsystemforAndroid
    description: "Windows Subsystem for Android (WSA) (by Andrew Rathbun): App download artifacts (ICO), App download artifacts (PNG), Appcompatdb.json, Diagnostic Logs for WSA, userdata.vhdx"
    type: bool
  - name: WindowsTelemetryDiagnosticsLegacy
    description: "Legacy Windows Telemetry and Diagnostics files (*.rbs) (by Andrew Rathbun and Josh Mitchell): Legacy .rbs files relating to Windows Telemetry and Diagnostics, Legacy .rbs files relating to Windows Telemetry and Diagnostics"
    type: bool
  - name: WindowsTimeline
    description: "ActivitiesCache.db collector (by Lee Whitfield): ActivitiesCache.db"
    type: bool
  - name: WindowsYourPhone
    description: "Windows Your Phone (by Andrew Rathbun): Windows Your Phone - All Databases"
    type: bool
  - name: XPRestorePoints
    description: "XP Restore Points - System Volume Information directory (by Phill Moore): System Volume Information"
    type: bool
  - name: XYplorer
    description: "XYplorer (by Andrew Rathbun): XYplorer - .dat files, XYplorer - .ini file, XYplorer - .ini file for each respective pane, XYplorer - AutoBackup folder"
    type: bool
  - name: ZohoAssist
    description: "Zoho Assist artifacts (by Andrew Rathbun): Zoho Assist .conf files, Zoho Assist .conf files in  Program Files*, Zoho Assist .conf files in AppData\Local, Zoho Assist .txt files in  Program Files*, Zoho Assist log files in AppData\Local, Zoho Assist log files in Program Files*, Zoho Assist log files in ProgramData"
    type: bool
  - name: Zoom
    description: "Zoom client artifacts (by Ryan McVicar): Zoom client logs, Zoom client logs (Windows XP), Zoom client recordings, Zoom plugin (Outlook)"
    type: bool
  - name: iTunesBackup
    description: "iTunes Backups (by Tony Knutson): iTunes Backup Folder, iTunes Backup Folder, iTunes Backup Folder - iOS13"
    type: bool
  - name: mIRC
    description: "mIRC (by Andrew Rathbun): mIRC Chat Logs (2000/XP), mIRC Chat Logs (Vista+)"
    type: bool
  - name: mRemoteNG
    description: "mRemoteNG (by Markus Einarsson (@einarssonm)): mRemoteNG Connection Configuration and Backups, mRemoteNG Logs, mRemoteNG Program Settings"
    type: bool
  - name: openSUSE
    description: "openSUSE on Windows Subsystem for Linux (by Matt Dawson): openSUSE WSL .bash_history, openSUSE WSL .bashrc, openSUSE WSL .profile, openSUSE WSL /etc/bash.bashrc, openSUSE WSL /etc/fstab, openSUSE WSL /etc/group, openSUSE WSL /etc/hostname, openSUSE WSL /etc/hosts, openSUSE WSL /etc/os-release, openSUSE WSL /etc/passwd, openSUSE WSL /etc/profile, openSUSE WSL /etc/shadow, openSUSE WSL /etc/timezone, openSUSE WSL ext4.vhdx"
    type: bool
  - name: pCloudDatabase
    description: "pCloud Database (by Josh Hickman): pCloud Database, pCloud Database Shared Memory File, pCloud Database WAL File"
    type: bool
  - name: qBittorrent
    description: "qBittorrent (by Banaanhangwagen): TorrentClients - qBittorrent, TorrentClients - qBittorrent"
    type: bool
  - name: uTorrent
    description: "uTorrent (by Banaanhangwagen): TorrentClients - uTorrent"
    type: bool

  - name: KapeRules
    type: hidden
    description: A CSV file controlling the different Kape Target Rules
    default: |
      Id,Name,Category,Glob,Accessor,Comment
      1,AVG AV Logs (XP),Antivirus,Documents and Settings\All Users\Application Data\AVG\Antivirus\log\**10,lazy_ntfs,
      2,AVG AV Report Logs (XP),Antivirus,Documents and Settings\All Users\Application Data\AVG\Antivirus\report\**10,lazy_ntfs,
      3,AVG AV Logs,Antivirus,ProgramData\AVG\Antivirus\log\**10,lazy_ntfs,
      4,AVG Report Logs,Antivirus,ProgramData\AVG\Antivirus\report\**10,lazy_ntfs,
      5,AVG Persistent Logs,Antivirus,ProgramData\AVG\Persistent Data\Antivirus\Logs\**10,lazy_ntfs,
      6,AVG FileInfo DB,Antivirus,ProgramData\AVG\Antivirus\**10\FileInfo2.db,lazy_ntfs,
      7,AVG lsdbj2 JSON,Antivirus,ProgramData\AVG\Antivirus\lsdb2.json,lazy_ntfs,
      8,Avast AV Logs (XP),Antivirus,Documents And Settings\All Users\Application Data\Avast Software\Avast\Log\**10,lazy_ntfs,
      9,Avast AV Logs,Antivirus,ProgramData\Avast Software\Avast\Log\**10,lazy_ntfs,
      10,Avast AV User Logs,Antivirus,Users\*\Avast Software\Avast\Log\**10,lazy_ntfs,
      11,Avast AV Index,Antivirus,ProgramData\Avast Software\Avast\Chest\index.xml,lazy_ntfs,
      12,Avast Persistent Data Logs,Antivirus,ProgramData\Avast Software\Persistent Data\Avast\Logs\**10,lazy_ntfs,
      13,Avast Icarus Logs,Antivirus,ProgramData\Avast Software\Icarus\Logs\**10,lazy_ntfs,
      14,Avira Activity Logs,Antivirus,ProgramData\Avira\Antivirus\LOGFILES\**10,lazy_ntfs,Collects the scan logs of Avira Antivirus
      15,Avira Security Logs,Antivirus,ProgramData\Avira\Security\Logs\**10,lazy_ntfs,
      16,Avira VPN Logs,Antivirus,ProgramData\Avira\VPN\**10,lazy_ntfs,Collects the VPN logs
      17,Bitdefender Endpoint Security Logs,Antivirus,ProgramData\Bitdefender\Endpoint Security\Logs\**10,lazy_ntfs,
      18,Bitdefender Internet Security Logs,Antivirus,ProgramData\Bitdefender\Desktop\Profiles\Logs\**10,lazy_ntfs,
      19,Bitdefender SQLite DB Files,Antivirus,Program Files*\Bitdefender*\**10\regex:*.+\.(db|db-wal|db-shm),ntfs,Bitdefender SQLite databases
      20,ComboFix,Antivirus,ComboFix.txt,lazy_ntfs,
      21,Cybereason Anti-Ransomware Logs,Antivirus,ProgramData\crs1\Logs\**10,lazy_ntfs,
      22,Cybereason Sensor Communications and Anti-Malware Logs,Antivirus,ProgramData\apv2\Logs\**10,lazy_ntfs,
      23,Cybereason Application Control and NGAV Logs,Antivirus,ProgramData\crb1\Logs\**10,lazy_ntfs,
      24,ESET NOD32 AV Logs (XP),Antivirus,Documents and Settings\All Users\Application Data\ESET\ESET NOD32 Antivirus\Logs\**10,lazy_ntfs,
      25,ESET NOD32 AV Logs,Antivirus,ProgramData\ESET\ESET NOD32 Antivirus\Logs\**10,lazy_ntfs,Parser available at https://github.com/laciKE/EsetLogParser
      26,ESET NOD32 AV Logs,Antivirus,ProgramData\ESET\ESET Security\Logs\**10,lazy_ntfs,
      27,ESET Remote Administrator Logs,Antivirus,ProgramData\ESET\RemoteAdministrator\Agent\EraAgentApplicationData\Logs,lazy_ntfs,Remote Administrator logs include information on tasks executed on the target.
      28,Emsisoft Scan Logs,ApplicationLogs,ProgramData\Emsisoft\Reports\scan*.txt,lazy_ntfs,Can contain file detection and quarantine info
      29,F-Secure Logs,Antivirus,ProgramData\F-Secure\Log\**10,lazy_ntfs,
      30,F-Secure User Logs,Antivirus,Users\*\AppData\Local\F-Secure\Log\**10,lazy_ntfs,
      31,F-Secure Scheduled Scan Reports,Antivirus,ProgramData\F-Secure\Antivirus\ScheduledScanReports\**10,lazy_ntfs,
      32,HitmanPro Logs,Antivirus,ProgramData\HitmanPro\Logs\**10,lazy_ntfs,
      33,HitmanPro Alert Logs,Antivirus,ProgramData\HitmanPro.Alert\Logs\**10,lazy_ntfs,
      34,HitmanPro Database,Antivirus,ProgramData\HitmanPro.Alert\excalibur.db,lazy_ntfs,SQLite DB
      35,MalwareBytes Anti-Malware Logs,Antivirus,ProgramData\Malwarebytes\Malwarebytes Anti-Malware\Logs\mbam-log-*.xml,lazy_ntfs,
      36,MalwareBytes Anti-Malware Service Logs,Antivirus,ProgramData\Malwarebytes\MBAMService\logs\mbamservice.log*,lazy_ntfs,
      37,MalwareBytes Anti-Malware Scan Logs,Antivirus,Users\*\AppData\Roaming\Malwarebytes\Malwarebytes Anti-Malware\Logs\**10,lazy_ntfs,
      38,MalwareBytes Anti-Malware Scan Results Logs,Antivirus,ProgramData\Malwarebytes\MBAMService\ScanResults\**10,lazy_ntfs,
      39,McAfee Desktop Protection Logs XP,Antivirus,Users\All Users\Application Data\McAfee\DesktopProtection\**10,lazy_ntfs,
      40,McAfee Desktop Protection Logs,Antivirus,ProgramData\McAfee\DesktopProtection\**10,lazy_ntfs,
      41,McAfee Endpoint Security Logs,Antivirus,ProgramData\McAfee\Endpoint Security\Logs\**10,lazy_ntfs,
      42,McAfee Endpoint Security Logs,Antivirus,ProgramData\McAfee\Endpoint Security\Logs_Old\**10,lazy_ntfs,
      43,McAfee VirusScan Logs,Antivirus,ProgramData\Mcafee\VirusScan\**10,lazy_ntfs,
      44,McAfee ePO Logs,Antivirus,ProgramData\McAfee\Endpoint Security\Logs\**10,lazy_ntfs,
      45,RogueKiller Reports,Antivirus,ProgramData\RogueKiller\logs\AdliceReport_*.json,lazy_ntfs,
      46,SUPERAntiSpyware Logs,Antivirus,Users\*\AppData\Roaming\SUPERAntiSpyware\Logs\**10,lazy_ntfs,
      47,SecureAge Antvirus Logs,Antivirus,ProgramData\SecureAge Technology\SecureAge\log\**10,lazy_ntfs,
      48,SentinelOne EDR Log,Antivirus,programdata\sentinel\logs\**10,lazy_ntfs,Logs are in Binary Format (.binlog)
      49,Sophos Logs (XP),Antivirus,Documents and Settings\All Users\Application Data\Sophos\Sophos *\Logs\**10,lazy_ntfs,"Includes Anti-Virus, Client Firewall, Data Control, Device Control, Endpoint Defense, Network Threat Detection, Management Communications System, Patch Control, Tamper Protection"
      50,Sophos Logs,Antivirus,ProgramData\Sophos\Sophos *\Logs\**10,lazy_ntfs,"Includes Anti-Virus, Client Firewall, Data Control, Device Control, Endpoint Defense, Network Threat Detection, Management Communications System, Patch Control, Tamper Protection"
      51,Symantec Endpoint Protection Logs (XP),Antivirus,Documents and Settings\All Users\Application Data\Symantec\Symantec Endpoint Protection\Logs\AV\**10,lazy_ntfs,
      52,Symantec Endpoint Protection Logs,Antivirus,ProgramData\Symantec\Symantec Endpoint Protection\*\Data\Logs\**10,lazy_ntfs,
      53,Symantec Endpoint Protection User Logs,Antivirus,Users\*\AppData\Local\Symantec\Symantec Endpoint Protection\Logs\**10,lazy_ntfs,
      54,Symantec Event Log Win7+,EventLogs,Windows\System32\winevt\logs\Symantec Endpoint Protection Client.evtx,lazy_ntfs,Symantec specific Windows event log
      55,Symantec Event Log Win7+,EventLogs,Windows.old\Windows\System32\winevt\logs\Symantec Endpoint Protection Client.evtx,lazy_ntfs,Symantec specific Windows event log
      56,Symantec Endpoint Protection Quarantine (XP),Antivirus,Documents and Settings\All Users\Application Data\Symantec\Symantec Endpoint Protection\Quarantine\**10,lazy_ntfs,
      57,Symantec Endpoint Protection Quarantine,Antivirus,ProgramData\Symantec\Symantec Endpoint Protection\*\Data\Quarantine\**10,lazy_ntfs,
      58,ccSubSDK Database,Antivirus,ProgramData\Symantec\Symantec Endpoint Protection\*\Data\CmnClnt\ccSubSDK\**10,lazy_ntfs,
      59,registrationInfo.xml,Antivirus,ProgramData\Symantec\Symantec Endpoint Protection\*\Data\registrationInfo.xml,lazy_ntfs,
      60,TotalAV Logs,Antivirus,Program Files*\TotalAV\logs\**10,lazy_ntfs,
      61,TotalAV Logs,Antivirus,ProgramData\TotalAV\logs\**10,lazy_ntfs,
      62,Trend Micro Logs,Antivirus,ProgramData\Trend Micro\**10,lazy_ntfs,
      63,Trend Micro Security Agent Report Logs,Antivirus,Program Files*\Trend Micro\Security Agent\Report\*.log,lazy_ntfs,
      64,Trend Micro Security Agent Connection Logs,Antivirus,Program Files*\Trend Micro\Security Agent\ConnLog\*.log,lazy_ntfs,
      65,VIPRE Business Agent Logs,Antivirus,ProgramData\VIPRE Business Agent\Logs\**10,lazy_ntfs,
      66,VIPRE Business User Logs (v7+),Antivirus,Users\*\AppData\Roaming\VIPRE Business\**10,lazy_ntfs,
      67,VIPRE Business User Logs (v5-v6),Antivirus,Users\*\AppData\Roaming\GFI Software\AntiMalware\Logs\**10,lazy_ntfs,
      68,VIPRE Business User Logs (up to v4),Antivirus,Users\*\AppData\Roaming\Sunbelt Software\AntiMalware\Logs\**10,lazy_ntfs,
      69,Webroot Program Data,Antivirus,ProgramData\WRData\WRLog.log,lazy_ntfs,
      70,DetectionHistory,Antivirus,ProgramData\Microsoft\Windows Defender\Scans\History\Service\DetectionHistory\*\**10,lazy_ntfs,
      71,Windows Defender Logs,Antivirus,ProgramData\Microsoft\Microsoft AntiMalware\Support\**10,lazy_ntfs,
      72,Windows Defender Event Logs,EventLogs,Windows\System32\winevt\Logs\Microsoft-Windows-Windows Defender*.evtx,lazy_ntfs,
      73,Windows Defender Event Logs,EventLogs,Windows.old\Windows\System32\winevt\Logs\Microsoft-Windows-Windows Defender*.evtx,lazy_ntfs,
      74,Windows Defender Logs,Antivirus,ProgramData\Microsoft\Windows Defender\Support\**10,lazy_ntfs,
      75,Windows Defender Logs,Antivirus,Windows\Temp\MpCmdRun.log,lazy_ntfs,
      76,Windows Defender Logs,Antivirus,Windows.old\Windows\Temp\MpCmdRun.log,lazy_ntfs,
      77,Apache Access Log,Webservers,**10\access.log,lazy_ntfs,
      78,IIS log files,Logs,Windows\System32\LogFiles\W3SVC*\*.log,lazy_ntfs,
      79,IIS log files,Logs,Windows.old\Windows\System32\LogFiles\W3SVC*\*.log,lazy_ntfs,
      80,IIS log files,Logs,inetpub\logs\LogFiles\*.log,lazy_ntfs,
      81,IIS log files,Logs,inetpub\logs\LogFiles\W3SVC*\*.log,lazy_ntfs,
      82,IIS log files,Logs,Resources\Directory\*\LogFiles\Web\W3SVC*\*.log,lazy_ntfs,
      83,IIS log files,Logs,Windows\system32\LogFiles\HTTPERR\*.log,lazy_ntfs,
      84,MS SQL Errorlog,SQL Exploitation,Program Files\Microsoft SQL Server\*\MSSQL\LOG\ERRORLOG,lazy_ntfs,
      85,MS SQL Errorlogs,SQL Exploitation,Program Files\Microsoft SQL Server\*\MSSQL\LOG\ERRORLOG.*,lazy_ntfs,
      86,ManageEngine Desktop Central Log Files,Logs,ManageEngine\DesktopCentral_Server\logs\**10,lazy_ntfs,
      87,NGINX Log Files,Logs,nginx\logs\*.log,lazy_ntfs,
      88,PowerShell Console Log,PowerShellConsoleLog,Users\*\AppData\Roaming\Microsoft\Windows\PowerShell\PSReadline\ConsoleHost_history.txt,lazy_ntfs,
      89,4K Video Downloader,SQLDatabases,Users\*\AppData\Local\4kdownload.com\4K Video Downloader\4K Video Downloader\*.sqlite,lazy_ntfs,Grabs database(s) that stores user download history
      90,Microsoft OneNote - FullTextSearchIndex,SQLDatabases,Users\*\AppData\Local\Packages\Microsoft.Office.OneNote_8wekyb3d8bbwe\LocalState\AppData\Local\OneNote\*\FullTextSearchIndex,lazy_ntfs,Grabs database(s) comprising of each OneNote notebook's text content
      91,Microsoft OneNote - RecentNotebooks_SeenURLs,SQLDatabases,Users\*\AppData\Local\Packages\Microsoft.Office.OneNote_8wekyb3d8bbwe\LocalState\AppData\Local\OneNote\Notifications\RecentNotebooks_SeenURLs,lazy_ntfs,Grabs a file that appears to record recently seen OneNote notebooks
      92,Microsoft OneNote - AccessibilityCheckerIndex,SQLDatabases,Users\*\AppData\Local\Packages\Microsoft.Office.OneNote_8wekyb3d8bbwe\LocalState\AppData\Local\OneNote\16.0\AccessibilityCheckerIndex,lazy_ntfs,Grabs database(s) comprising of each OneNote notebook's version sync error history
      93,Microsoft OneNote - User NoteTags,SQLDatabases,Users\*\AppData\Local\Packages\Microsoft.Office.OneNote_8wekyb3d8bbwe\LocalState\AppData\Local\OneNote\16.0\NoteTags\*LiveId.db,lazy_ntfs,Grabs a database that stores the user specified tags within OneNote to be used application-wide
      94,Microsoft OneNote - RecentSearches,SQLDatabases,Users\*\AppData\Local\Packages\Microsoft.Office.OneNote_8wekyb3d8bbwe\LocalState\AppData\Local\OneNote\16.0\RecentSearches\RecentSearches.db,lazy_ntfs,Grabs a database that stores the user's recent searches within OneNote
      95,Microsoft Sticky Notes - 1607 and later,SQLDatabases,Users\*\AppData\Local\Packages\Microsoft.MicrosoftStickyNotes*\LocalState\plum.sqlite*,lazy_ntfs,
      96,Microsoft To Do - SQLite Database of To Do tasks,SQLDatabases,Users\*\AppData\Local\Packages\Microsoft.Todos_8wekyb3d8bbwe\LocalState\AccountsRoot\*\todosqlite.db*,lazy_ntfs,
      97,TeraCopy - History Databases,SQLDatabases,Users\*\AppData\Roaming\TeraCopy\History\*.db,lazy_ntfs,
      98,TeraCopy - Main Database,SQLDatabases,Users\*\AppData\Roaming\TeraCopy\main.db,lazy_ntfs,
      99,Dropbox Metadata,SQLDatabases,Users\*\AppData\Local\Dropbox\*\filecache.db*,lazy_ntfs,Getting individual files because folder may contain very large extraneous files
      100,Dropbox Metadata,SQLDatabases,Users\*\AppData\Local\Dropbox\*\config.dbx,lazy_ntfs,Getting individual files because folder may contain very large extraneous files
      101,Dropbox Metadata,SQLDatabases,Users\*\AppData\Local\Dropbox\*\home.db,lazy_ntfs,SQlite database which appears to keep track of the user's recent Dropbox activity
      102,Dropbox Metadata,SQLDatabases,Users\*\AppData\Local\Dropbox\*\icon.db,lazy_ntfs,SQLite database which appears to keep track of icons in the user's Drobox sync history which can give an indication as to which files and folders are present
      103,Dropbox Metadata,SQLDatabases,Users\*\AppData\Local\Dropbox\*\sync_history.db,lazy_ntfs,SQLite database which appears to keep track of the user's Drobox sync history
      104,Dropbox Metadata,SQLDatabases,Users\*\AppData\Local\Dropbox\*\sync\nucleus.sqlite3*,lazy_ntfs,SQLite database which appears to contain a table for deleted files
      105,Dropbox Metadata,SQLDatabases,Users\*\AppData\Local\Dropbox\host.db,lazy_ntfs,"SQLite database which contains the local path of the user's Dropbox folder encoded in BASE64. Decode each line separately, not together."
      106,Dropbox Metadata,SQLDatabases,Users\*\AppData\Local\Dropbox\host.dbx,lazy_ntfs,"SQLite database which contains the local path of the user's Dropbox folder encoded in BASE64. Decode each line separately, not together."
      107,Dropbox Metadata,SQLDatabases,Users\*\AppData\Local\Dropbox\*\sync\aggregation.dbx,lazy_ntfs,SQLite database which appears to contain snapshot table of the user's Dropbox contents in JSON with timestamps in UNIX Epoch
      108,Dropbox Metadata,SQLDatabases,Users\*\AppData\Local\Dropbox\*\avatarcache.db,lazy_ntfs,SQLite database which appears to contain the ID's of account(s) on the user's system where Dropbox is installed
      109,Dropbox Metadata,SQLDatabases,Users\*\AppData\Local\Dropbox\*\avatarcache.db,lazy_ntfs,SQLite database which appears to contain the ID's of account(s) on the user's system where Dropbox is installed
      110,Google File Stream Metadata,SQLDatabases,Users\*\AppData\Local\Google\Drive\*\cloud_graph\cloud_graph.db,lazy_ntfs,Windows_GoogleDrive_CloudGraphDB.smap
      111,Google File Stream Metadata,SQLDatabases,Users\*\AppData\Local\Google\Drive\*\TempData\*\change_buffer\**10,lazy_ntfs,DB(s) with seemingly randomized filename(s) that track file system changes within Google Drive
      112,Google File Stream Metadata,SQLDatabases,Users\*\AppData\Local\Google\Drive\*\snapshot.db,lazy_ntfs,Windows_GoogleDrive_SnapshotDB.smap
      113,Google File Stream Metadata,SQLDatabases,Users\*\AppData\Local\Google\Drive\*\sync_config.db,lazy_ntfs,Windows_GoogleDrive_SyncConfigDB.smap
      114,FileZilla SQLite3 Log Files,SQLDatabases,Users\*\AppData\Roaming\FileZilla\*.sqlite3*,lazy_ntfs,
      115,Chrome bookmarks XP,SQLDatabases,Documents and Settings\*\Local Settings\Application Data\Google\Chrome\User Data\*\Bookmarks*,lazy_ntfs,
      116,Chrome Cookies XP,SQLDatabases,Documents and Settings\*\Local Settings\Application Data\Google\Chrome\User Data\*\Cookies*,lazy_ntfs,
      117,Chrome Current Session XP,SQLDatabases,Documents and Settings\*\Local Settings\Application Data\Google\Chrome\User Data\*\Current Session,lazy_ntfs,
      118,Chrome Current Tabs XP,SQLDatabases,Documents and Settings\*\Local Settings\Application Data\Google\Chrome\User Data\*\Current Tabs,lazy_ntfs,
      119,Chrome Favicons XP,SQLDatabases,Documents and Settings\*\Local Settings\Application Data\Google\Chrome\User Data\*\Favicons*,lazy_ntfs,
      120,Chrome History XP,SQLDatabases,Documents and Settings\*\Local Settings\Application Data\Google\Chrome\User Data\*\History*,lazy_ntfs,
      121,Chrome Last Session XP,SQLDatabases,Documents and Settings\*\Local Settings\Application Data\Google\Chrome\User Data\*\Last Session,lazy_ntfs,
      122,Chrome Last Tabs XP,SQLDatabases,Documents and Settings\*\Local Settings\Application Data\Google\Chrome\User Data\*\Last Tabs,lazy_ntfs,
      123,Chrome Login Data XP,SQLDatabases,Documents and Settings\*\Local Settings\Application Data\Google\Chrome\User Data\*\Login Data,lazy_ntfs,
      124,Chrome Preferences XP,SQLDatabases,Documents and Settings\*\Local Settings\Application Data\Google\Chrome\User Data\*\Preferences,lazy_ntfs,
      125,Chrome Shortcuts XP,SQLDatabases,Documents and Settings\*\Local Settings\Application Data\Google\Chrome\User Data\*\Shortcuts*,lazy_ntfs,
      126,Chrome Top Sites XP,SQLDatabases,Documents and Settings\*\Local Settings\Application Data\Google\Chrome\User Data\*\Top Sites*,lazy_ntfs,
      127,Chrome Visited Links XP,SQLDatabases,Documents and Settings\*\Local Settings\Application Data\Google\Chrome\User Data\*\Visited Links,lazy_ntfs,
      128,Chrome Web Data XP,SQLDatabases,Documents and Settings\*\Local Settings\Application Data\Google\Chrome\User Data\*\Web Data*,lazy_ntfs,
      129,Chrome bookmarks,SQLDatabases,Users\*\AppData\Local\Google\Chrome\User Data\*\Bookmarks*,lazy_ntfs,
      130,Chrome Cookies,SQLDatabases,Users\*\AppData\Local\Google\Chrome\User Data\*\Cookies*,lazy_ntfs,
      131,Chrome Current Session,SQLDatabases,Users\*\AppData\Local\Google\Chrome\User Data\*\Current Session,lazy_ntfs,
      132,Chrome Current Tabs,SQLDatabases,Users\*\AppData\Local\Google\Chrome\User Data\*\Current Tabs,lazy_ntfs,
      133,Chrome Download Metadata,SQLDatabases,Users\*\AppData\Local\Google\Chrome\User Data\*\Download Metadata,lazy_ntfs,
      134,Chrome Extension Cookies,SQLDatabases,Users\*\AppData\Local\Google\Chrome\User Data\*\Extension Cookies,lazy_ntfs,
      135,Chrome Favicons,SQLDatabases,Users\*\AppData\Local\Google\Chrome\User Data\*\Favicons*,lazy_ntfs,
      136,Chrome History,SQLDatabases,Users\*\AppData\Local\Google\Chrome\User Data\*\History*,lazy_ntfs,
      137,Chrome Last Session,SQLDatabases,Users\*\AppData\Local\Google\Chrome\User Data\*\Last Session,lazy_ntfs,
      138,Chrome Last Tabs,SQLDatabases,Users\*\AppData\Local\Google\Chrome\User Data\*\Last Tabs,lazy_ntfs,
      139,Chrome Login Data,SQLDatabases,Users\*\AppData\Local\Google\Chrome\User Data\*\Login Data,lazy_ntfs,
      140,Chrome Media History,SQLDatabases,Users\*\AppData\Local\Google\Chrome\User Data\*\Media History*,lazy_ntfs,
      141,Chrome Network Action Predictor,SQLDatabases,Users\*\AppData\Local\Google\Chrome\User Data\*\Network Action Predictor,lazy_ntfs,
      142,Chrome Network Persistent State,SQLDatabases,Users\*\AppData\Local\Google\Chrome\User Data\*\Network Persistent State,lazy_ntfs,
      143,Chrome Preferences,SQLDatabases,Users\*\AppData\Local\Google\Chrome\User Data\*\Preferences,lazy_ntfs,
      144,Chrome Quota Manager,SQLDatabases,Users\*\AppData\Local\Google\Chrome\User Data\*\QuotaManager,lazy_ntfs,
      145,Chrome Reporting and NEL,SQLDatabases,Users\*\AppData\Local\Google\Chrome\User Data\*\Reporting and NEL,lazy_ntfs,
      146,Chrome Shortcuts,SQLDatabases,Users\*\AppData\Local\Google\Chrome\User Data\*\Shortcuts*,lazy_ntfs,
      147,Chrome Top Sites,SQLDatabases,Users\*\AppData\Local\Google\Chrome\User Data\*\Top Sites*,lazy_ntfs,
      148,Chrome Trust Tokens,SQLDatabases,Users\*\AppData\Local\Google\Chrome\User Data\*\Trust Tokens*,lazy_ntfs,
      149,Chrome SyncData Database,SQLDatabases,Users\*\AppData\Local\Google\Chrome\User Data\*\Sync Data\SyncData.sqlite3,lazy_ntfs,
      150,Chrome Visited Links,SQLDatabases,Users\*\AppData\Local\Google\Chrome\User Data\*\Visited Links,lazy_ntfs,
      151,Chrome Web Data,SQLDatabases,Users\*\AppData\Local\Google\Chrome\User Data\*\Web Data*,lazy_ntfs,
      152,Edge bookmarks,SQLDatabases,Users\*\AppData\Local\Microsoft\Edge\User Data\*\Bookmarks*,lazy_ntfs,
      153,Edge Collections,SQLDatabases,Users\*\AppData\Local\Microsoft\Edge\User Data\*\Collections\collectionsSQLite,lazy_ntfs,
      154,Edge Cookies,SQLDatabases,Users\*\AppData\Local\Microsoft\Edge\User Data\*\Cookies*,lazy_ntfs,
      155,Edge Current Session,SQLDatabases,Users\*\AppData\Local\Microsoft\Edge\User Data\*\Current Session,lazy_ntfs,
      156,Edge Current Tabs,SQLDatabases,Users\*\AppData\Local\Microsoft\Edge\User Data\*\Current Tabs,lazy_ntfs,
      157,Edge Favicons,SQLDatabases,Users\*\AppData\Local\Microsoft\Edge\User Data\*\Favicons*,lazy_ntfs,
      158,Edge History,SQLDatabases,Users\*\AppData\Local\Microsoft\Edge\User Data\*\History*,lazy_ntfs,
      159,Edge Last Session,SQLDatabases,Users\*\AppData\Local\Microsoft\Edge\User Data\*\Last Session,lazy_ntfs,
      160,Edge Last Tabs,SQLDatabases,Users\*\AppData\Local\Microsoft\Edge\User Data\*\Last Tabs,lazy_ntfs,
      161,Edge Login Data,SQLDatabases,Users\*\AppData\Local\Microsoft\Edge\User Data\*\Login Data,lazy_ntfs,
      162,Edge Media History,SQLDatabases,Users\*\AppData\Local\Microsoft\Edge\User Data\*\Media History*,lazy_ntfs,
      163,Edge Network Action Predictor,SQLDatabases,Users\*\AppData\Local\Microsoft\Edge\User Data\*\Network Action Predictor,lazy_ntfs,
      164,Edge Preferences,SQLDatabases,Users\*\AppData\Local\Microsoft\Edge\User Data\*\Preferences,lazy_ntfs,
      165,Edge Shortcuts,SQLDatabases,Users\*\AppData\Local\Microsoft\Edge\User Data\*\Shortcuts*,lazy_ntfs,
      166,Edge Top Sites,SQLDatabases,Users\*\AppData\Local\Microsoft\Edge\User Data\*\Top Sites*,lazy_ntfs,
      167,Edge SyncData Database,SQLDatabases,Users\*\AppData\Local\Microsoft\Edge\User Data\*\Sync Data\SyncData.sqlite3,lazy_ntfs,
      168,Edge Bookmarks,SQLDatabases,Users\*\AppData\Local\Microsoft\Edge\User Data\*\Bookmarks*,lazy_ntfs,
      169,Edge Visited Links,SQLDatabases,Users\*\AppData\Local\Microsoft\Edge\User Data\*\Visited Links,lazy_ntfs,
      170,Edge Web Data,SQLDatabases,Users\*\AppData\Local\Microsoft\Edge\User Data\*\Web Data*,lazy_ntfs,
      171,Addons,SQLDatabases,Users\*\AppData\Roaming\Mozilla\Firefox\Profiles\*\addons.sqlite*,lazy_ntfs,
      172,Bookmarks,SQLDatabases,Users\*\AppData\Roaming\Mozilla\Firefox\Profiles\*\weave\bookmarks.sqlite*,lazy_ntfs,
      173,Cookies,SQLDatabases,Users\*\AppData\Roaming\Mozilla\Firefox\Profiles\*\cookies.sqlite*,lazy_ntfs,
      174,Cookies,SQLDatabases,Users\*\AppData\Roaming\Mozilla\Firefox\Profiles\*\firefox_cookies.sqlite*,lazy_ntfs,
      175,Downloads,SQLDatabases,Users\*\AppData\Roaming\Mozilla\Firefox\Profiles\*\downloads.sqlite*,lazy_ntfs,
      176,Favicons,SQLDatabases,Users\*\AppData\Roaming\Mozilla\Firefox\Profiles\*\favicons.sqlite*,lazy_ntfs,
      177,Form history,SQLDatabases,Users\*\AppData\Roaming\Mozilla\Firefox\Profiles\*\formhistory.sqlite*,lazy_ntfs,
      178,Permissions,SQLDatabases,Users\*\AppData\Roaming\Mozilla\Firefox\Profiles\*\permissions.sqlite*,lazy_ntfs,
      179,Places,SQLDatabases,Users\*\AppData\Roaming\Mozilla\Firefox\Profiles\*\places.sqlite*,lazy_ntfs,
      180,Protections,SQLDatabases,Users\*\AppData\Roaming\Mozilla\Firefox\Profiles\*\protections.sqlite*,lazy_ntfs,
      181,Search,SQLDatabases,Users\*\AppData\Roaming\Mozilla\Firefox\Profiles\*\search.sqlite*,lazy_ntfs,
      182,Signons,SQLDatabases,Users\*\AppData\Roaming\Mozilla\Firefox\Profiles\*\signons.sqlite*,lazy_ntfs,
      183,Storage Sync,SQLDatabases,Users\*\AppData\Roaming\Mozilla\Firefox\Profiles\*\storage-sync.sqlite*,lazy_ntfs,
      184,Webappstore,SQLDatabases,Users\*\AppData\Roaming\Mozilla\Firefox\Profiles\*\webappstore.sqlite*,lazy_ntfs,
      185,Windows 10 Notification DB,SQLDatabases,Users\*\AppData\Local\Microsoft\Windows\Notifications\wpndatabase.db,lazy_ntfs,
      186,Windows 10 Notification DB,SQLDatabases,Users\*\AppData\Local\Microsoft\Windows\Notifications\appdb.dat,lazy_ntfs,
      187,ActivitiesCache.db,SQLDatabases,Users\*\AppData\Local\ConnectedDevicesPlatform\*\ActivitiesCache.db*,lazy_ntfs,
      188,Update Store.db,OS Upgrade,ProgramData\USOPrivate\UpdateStore\store.db,lazy_ntfs,
      189,Bitdefender SQLite DB Files,Antivirus,Program Files*\Bitdefender*\**10\regex:*.+\.(db|db-wal|db-shm),ntfs,Bitdefender SQLite databases
      190,EventTranscript.db,SystemEvents,ProgramData\Microsoft\Diagnosis\EventTranscript\EventTranscript.db*,lazy_ntfs,
      191,EventTranscript.db,SystemEvents,Windows.old\ProgramData\Microsoft\Diagnosis\EventTranscript\EventTranscript.db*,lazy_ntfs,
      192,Bookmarks,Communications,Users\*\AppData\Local\BraveSoftware\Brave-Browser\User Data\*\Bookmarks*,lazy_ntfs,
      193,Cookies,Communications,Users\*\AppData\Local\BraveSoftware\Brave-Browser\User Data\*\Cookies*,lazy_ntfs,
      194,Current Session,Communications,Users\*\AppData\Local\BraveSoftware\Brave-Browser\User Data\*\Current Session,lazy_ntfs,
      195,Current Tabs,Communications,Users\*\AppData\Local\BraveSoftware\Brave-Browser\User Data\*\Current Tabs,lazy_ntfs,
      196,Download Metadata,Communications,Users\*\AppData\Local\BraveSoftware\Brave-Browser\User Data\*\DownloadMetadata,lazy_ntfs,
      197,Favicons,Communications,Users\*\AppData\Local\BraveSoftware\Brave-Browser\User Data\*\Favicons*,lazy_ntfs,
      198,History,Communications,Users\*\AppData\Local\BraveSoftware\Brave-Browser\User Data\*\History*,lazy_ntfs,
      199,Sessions Folder,Communications,Users\*\AppData\Local\BraveSoftware\Brave-Browser\User Data\Default\Sessions\*,lazy_ntfs,
      200,Login Data,Communications,Users\*\AppData\Local\BraveSoftware\Brave-Browser\User Data\*\Login Data,lazy_ntfs,
      201,Network Action Predictor,Communications,Users\*\AppData\Local\BraveSoftware\Brave-Browser\User Data\*\Network Action Predictor,lazy_ntfs,
      202,Network Persistent State,Communications,Users\*\AppData\Local\BraveSoftware\Brave-Browser\User Data\*\Network Persistent State,lazy_ntfs,
      203,Preferences,Communications,Users\*\AppData\Local\BraveSoftware\Brave-Browser\User Data\*\Preferences,lazy_ntfs,
      204,Quota Manager,Communications,Users\*\AppData\Local\BraveSoftware\Brave-Browser\User Data\*\QuotaManager,lazy_ntfs,
      205,Reporting and NEL,Communications,Users\*\AppData\Local\BraveSoftware\Brave-Browser\User Data\*\Reporting and NEL,lazy_ntfs,
      206,Shortcuts,Communications,Users\*\AppData\Local\BraveSoftware\Brave-Browser\User Data\*\Shortcuts*,lazy_ntfs,
      207,Publisher Info DB/Brave Rewards,Communications,Users\*\AppData\Local\BraveSoftware\Brave-Browser\User Data\*\publisher_info_db*,lazy_ntfs,"SQLite Database related to ""Brave Rewards"" containing an event_log table"
      208,Top Sites,Communications,Users\*\AppData\Local\BraveSoftware\Brave-Browser\User Data\*\Top Sites*,lazy_ntfs,
      209,Visited Links,Communications,Users\*\AppData\Local\BraveSoftware\Brave-Browser\User Data\*\Visited Links*,lazy_ntfs,
      210,Web Data,Communications,Users\*\AppData\Local\BraveSoftware\Brave-Browser\User Data\*\Web Data*,lazy_ntfs,
      211,Secure Preferences,Communications,Users\*\AppData\Local\BraveSoftware\Brave-Browser\User Data\*\Secure Preferences*,lazy_ntfs,Contains additional preferences data
      212,Chrome Cache Folder,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Cache\**10,lazy_ntfs,
      213,Chromium Edge Cache Folder,Communications,Users\*\AppData\Local\Microsoft\Edge\User Data\*\Cache\**10,lazy_ntfs,
      214,Firefox Cache Folder,Communications,Users\*\AppData\Local\Mozilla\Firefox\Profiles\*\**10,lazy_ntfs,
      215,IE 9/10 Cache,Communications,Users\*\AppData\Local\Microsoft\Windows\Temporary Internet Files\**10,lazy_ntfs,
      216,IE Index.dat temp internet files,Communications,Documents and Settings\*\Local Settings\Temporary Internet Files\Content.IE5\index.dat,lazy_ntfs,
      217,IE 11 Cache,Communications,Users\*\AppData\Local\Microsoft\Windows\INetCache\**10,lazy_ntfs,
      218,Edge WebcacheV01.dat,Communications,Users\*\AppData\Local\Microsoft\Windows\WebCache\*,lazy_ntfs,
      219,Brave Cache Folder,Communications,Users\%users%\AppData\Local\BraveSoftware\Brave-Browser\User Data\Default\Cache\Cache_Data\**10,lazy_ntfs,
      220,Chrome bookmarks XP,Communications,Documents and Settings\*\Local Settings\Application Data\Google\Chrome\User Data\*\Bookmarks*,lazy_ntfs,
      221,Chrome Cookies XP,Communications,Documents and Settings\*\Local Settings\Application Data\Google\Chrome\User Data\*\Cookies*,lazy_ntfs,
      222,Chrome Current Session XP,Communications,Documents and Settings\*\Local Settings\Application Data\Google\Chrome\User Data\*\Current Session,lazy_ntfs,
      223,Chrome Current Tabs XP,Communications,Documents and Settings\*\Local Settings\Application Data\Google\Chrome\User Data\*\Current Tabs,lazy_ntfs,
      224,Chrome Favicons XP,Communications,Documents and Settings\*\Local Settings\Application Data\Google\Chrome\User Data\*\Favicons*,lazy_ntfs,
      225,Chrome History XP,Communications,Documents and Settings\*\Local Settings\Application Data\Google\Chrome\User Data\*\History*,lazy_ntfs,
      226,Chrome Last Session XP,Communications,Documents and Settings\*\Local Settings\Application Data\Google\Chrome\User Data\*\Last Session,lazy_ntfs,
      227,Chrome Last Tabs XP,Communications,Documents and Settings\*\Local Settings\Application Data\Google\Chrome\User Data\*\Last Tabs,lazy_ntfs,
      228,Chrome Login Data XP,Communications,Documents and Settings\*\Local Settings\Application Data\Google\Chrome\User Data\*\Login Data,lazy_ntfs,
      229,Chrome Preferences XP,Communications,Documents and Settings\*\Local Settings\Application Data\Google\Chrome\User Data\*\Preferences,lazy_ntfs,
      230,Chrome Shortcuts XP,Communications,Documents and Settings\*\Local Settings\Application Data\Google\Chrome\User Data\*\Shortcuts*,lazy_ntfs,
      231,Chrome Top Sites XP,Communications,Documents and Settings\*\Local Settings\Application Data\Google\Chrome\User Data\*\Top Sites*,lazy_ntfs,
      232,Chrome Visited Links XP,Communications,Documents and Settings\*\Local Settings\Application Data\Google\Chrome\User Data\*\Visited Links,lazy_ntfs,
      233,Chrome Web Data XP,Communications,Documents and Settings\*\Local Settings\Application Data\Google\Chrome\User Data\*\Web Data*,lazy_ntfs,
      234,Chrome bookmarks,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Bookmarks*,lazy_ntfs,
      235,Chrome Cookies,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\**10\Cookies*,lazy_ntfs,
      236,Chrome Current Session,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Current Session,lazy_ntfs,
      237,Chrome Current Tabs,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Current Tabs,lazy_ntfs,
      238,Chrome Download Metadata,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\DownloadMetadata,lazy_ntfs,
      239,Chrome Extension Cookies,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Extension Cookies,lazy_ntfs,
      240,Chrome Favicons,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Favicons*,lazy_ntfs,
      241,Chrome History,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\History*,lazy_ntfs,
      242,Chrome Last Session,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Last Session,lazy_ntfs,
      243,Chrome Last Tabs,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Last Tabs,lazy_ntfs,
      244,Chrome Sessions Folder,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Sessions\*,lazy_ntfs,
      245,Chrome Login Data,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Login Data,lazy_ntfs,
      246,Chrome Media History,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Media History*,lazy_ntfs,
      247,Chrome Network Action Predictor,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Network Action Predictor,lazy_ntfs,
      248,Chrome Network Persistent State,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Network Persistent State,lazy_ntfs,
      249,Chrome Preferences,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Preferences,lazy_ntfs,
      250,Chrome Quota Manager,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\QuotaManager,lazy_ntfs,
      251,Chrome Reporting and NEL,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Reporting and NEL,lazy_ntfs,
      252,Chrome Shortcuts,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Shortcuts*,lazy_ntfs,
      253,Chrome Top Sites,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Top Sites*,lazy_ntfs,
      254,Chrome Trust Tokens,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Trust Tokens*,lazy_ntfs,
      255,Chrome SyncData Database,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Sync Data\SyncData.sqlite3,lazy_ntfs,
      256,Chrome Visited Links,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Visited Links,lazy_ntfs,
      257,Chrome Web Data,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Web Data*,lazy_ntfs,
      258,Windows Protect Folder,FileSystem,Users\*\AppData\Roaming\Microsoft\Protect\*\**10,lazy_ntfs,Required for offline decryption
      259,Chrome Extension Files,Communication,Users\*\AppData\Local\Google\Chrome\User Data\*\Extensions\**10,lazy_ntfs,
      260,Chrome Extension Files XP,Communications,Documents and Settings\*\Local Settings\Application Data\Google\Chrome\User Data\*\Extensions\**10,lazy_ntfs,
      261,Chrome HTML5 File System Folder,Communication,Users\*\AppData\Local\Google\Chrome\User Data\*\File System\**10,lazy_ntfs,
      262,Edge folder,Communications,Users\*\AppData\Local\Packages\Microsoft.MicrosoftEdge_8wekyb3d8bbwe\**10,lazy_ntfs,
      263,Edge bookmarks,Communications,Users\*\AppData\Local\Microsoft\Edge\User Data\*\Bookmarks*,lazy_ntfs,
      264,Edge Collections,Communications,Users\*\AppData\Local\Microsoft\Edge\User Data\*\Collections\collectionsSQLite,lazy_ntfs,
      265,Edge Cookies,Communications,Users\*\AppData\Local\Microsoft\Edge\User Data\*\Cookies*,lazy_ntfs,
      266,Edge Current Session,Communications,Users\*\AppData\Local\Microsoft\Edge\User Data\*\Current Session,lazy_ntfs,
      267,Edge Current Tabs,Communications,Users\*\AppData\Local\Microsoft\Edge\User Data\*\Current Tabs,lazy_ntfs,
      268,Edge Favicons,Communications,Users\*\AppData\Local\Microsoft\Edge\User Data\*\Favicons*,lazy_ntfs,
      269,Edge History,Communications,Users\*\AppData\Local\Microsoft\Edge\User Data\*\History*,lazy_ntfs,
      270,Edge Last Session,Communications,Users\*\AppData\Local\Microsoft\Edge\User Data\*\Last Session,lazy_ntfs,
      271,Edge Last Tabs,Communications,Users\*\AppData\Local\Microsoft\Edge\User Data\*\Last Tabs,lazy_ntfs,
      272,Edge Sessions Folder,Communications,Users\*\AppData\Local\Microsoft\Edge\User Data\*\Sessions\*,lazy_ntfs,
      273,Edge Login Data,Communications,Users\*\AppData\Local\Microsoft\Edge\User Data\*\Login Data,lazy_ntfs,
      274,Edge Media History,Communications,Users\*\AppData\Local\Microsoft\Edge\User Data\*\Media History*,lazy_ntfs,
      275,Edge Network Action Predictor,Communications,Users\*\AppData\Local\Microsoft\Edge\User Data\*\Network Action Predictor,lazy_ntfs,
      276,Edge Preferences,Communications,Users\*\AppData\Local\Microsoft\Edge\User Data\*\Preferences,lazy_ntfs,
      277,Edge Shortcuts,Communications,Users\*\AppData\Local\Microsoft\Edge\User Data\*\Shortcuts*,lazy_ntfs,
      278,Edge Top Sites,Communications,Users\*\AppData\Local\Microsoft\Edge\User Data\*\Top Sites*,lazy_ntfs,
      279,Edge SyncData Database,Communications,Users\*\AppData\Local\Microsoft\Edge\User Data\*\Sync Data\SyncData.sqlite3,lazy_ntfs,
      280,Edge Bookmarks,Communications,Users\*\AppData\Local\Microsoft\Edge\User Data\*\Bookmarks*,lazy_ntfs,
      281,Edge Visited Links,Communications,Users\*\AppData\Local\Microsoft\Edge\User Data\*\Visited Links,lazy_ntfs,
      282,Edge Web Data,Communications,Users\*\AppData\Local\Microsoft\Edge\User Data\*\Web Data*,lazy_ntfs,
      283,Windows Protect Folder,FileSystem,Users\*\AppData\Roaming\Microsoft\Protect\*\**10,lazy_ntfs,Required for offline DPAPI decryption
      284,Edge Snapshots Folder,Communications,Users\*\AppData\Local\Microsoft\Edge\User Data\Snapshots\*\**10,lazy_ntfs,"Grabs folder that appears to have snapshots of Edge Chromium SQLite DBs organized by version #. In testing, there were 3 previous versions of Edge Chromium separated into different folders"
      285,Addons,Communications,Users\*\AppData\Roaming\Mozilla\Firefox\Profiles\*\addons.sqlite*,lazy_ntfs,
      286,Bookmarks,Communications,Users\*\AppData\Roaming\Mozilla\Firefox\Profiles\*\weave\bookmarks.sqlite*,lazy_ntfs,
      287,Bookmarks,Communications,Users\*\AppData\Roaming\Mozilla\Firefox\Profiles\*\bookmarkbackups\**10,lazy_ntfs,
      288,Cookies,Communications,Users\*\AppData\Roaming\Mozilla\Firefox\Profiles\*\cookies.sqlite*,lazy_ntfs,
      289,Cookies,Communications,Users\*\AppData\Roaming\Mozilla\Firefox\Profiles\*\firefox_cookies.sqlite*,lazy_ntfs,
      290,Downloads,Communications,Users\*\AppData\Roaming\Mozilla\Firefox\Profiles\*\downloads.sqlite*,lazy_ntfs,
      291,Extensions,Communications,Users\*\AppData\Roaming\Mozilla\Firefox\Profiles\*\extensions.json,lazy_ntfs,
      292,Favicons,Communications,Users\*\AppData\Roaming\Mozilla\Firefox\Profiles\*\favicons.sqlite*,lazy_ntfs,
      293,Form history,Communications,Users\*\AppData\Roaming\Mozilla\Firefox\Profiles\*\formhistory.sqlite*,lazy_ntfs,
      294,Permissions,Communications,Users\*\AppData\Roaming\Mozilla\Firefox\Profiles\*\permissions.sqlite*,lazy_ntfs,
      295,Places,Communications,Users\*\AppData\Roaming\Mozilla\Firefox\Profiles\*\places.sqlite*,lazy_ntfs,
      296,Protections,Communications,Users\*\AppData\Roaming\Mozilla\Firefox\Profiles\*\protections.sqlite*,lazy_ntfs,
      297,Search,Communications,Users\*\AppData\Roaming\Mozilla\Firefox\Profiles\*\search.sqlite*,lazy_ntfs,
      298,Signons,Communications,Users\*\AppData\Roaming\Mozilla\Firefox\Profiles\*\signons.sqlite*,lazy_ntfs,
      299,Storage Sync,Communications,Users\*\AppData\Roaming\Mozilla\Firefox\Profiles\*\storage-sync.sqlite*,lazy_ntfs,
      300,Webappstore,Communications,Users\*\AppData\Roaming\Mozilla\Firefox\Profiles\*\webappstore.sqlite*,lazy_ntfs,
      301,Password,Communications,Users\*\AppData\Roaming\Mozilla\Firefox\Profiles\*\key*.db,lazy_ntfs,
      302,Password,Communications,Users\*\AppData\Roaming\Mozilla\Firefox\Profiles\*\signon*.*,lazy_ntfs,
      303,Password,Communications,Users\*\AppData\Roaming\Mozilla\Firefox\Profiles\*\logins.json,lazy_ntfs,
      304,Preferences,Communications,Users\*\AppData\Roaming\Mozilla\Firefox\Profiles\*\prefs.js,lazy_ntfs,
      305,Sessionstore,Communications,Users\*\AppData\Roaming\Mozilla\Firefox\Profiles\*\sessionstore*,lazy_ntfs,
      306,Sessionstore Folder,Communications,Users\*\AppData\Roaming\Mozilla\Firefox\Profiles\*\sessionstore-backups\**10,lazy_ntfs,
      307,Places XP,Communications,Documents and Settings\*\Application Data\Mozilla\Firefox\Profiles\*\places.sqlite*,lazy_ntfs,
      308,Downloads XP,Communications,Documents and Settings\*\Application Data\Mozilla\Firefox\Profiles\*\downloads.sqlite*,lazy_ntfs,
      309,Form history XP,Communications,Documents and Settings\*\Application Data\Mozilla\Firefox\Profiles\*\formhistory.sqlite*,lazy_ntfs,
      310,Cookies XP,Communications,Documents and Settings\*\Application Data\Mozilla\Firefox\Profiles\*\cookies.sqlite*,lazy_ntfs,
      311,Signons XP,Communications,Documents and Settings\*\Application Data\Mozilla\Firefox\Profiles\*\signons.sqlite*,lazy_ntfs,
      312,Webappstore XP,Communications,Documents and Settings\*\Application Data\Mozilla\Firefox\Profiles\*\webappstore.sqlite*,lazy_ntfs,
      313,Favicons XP,Communications,Documents and Settings\*\Application Data\Mozilla\Firefox\Profiles\*\favicons.sqlite*,lazy_ntfs,
      314,Addons XP,Communications,Documents and Settings\*\Application Data\Mozilla\Firefox\Profiles\*\addons.sqlite*,lazy_ntfs,
      315,Search XP,Communications,Documents and Settings\*\Application Data\Mozilla\Firefox\Profiles\*\search.sqlite*,lazy_ntfs,
      316,Password XP,Communications,Documents and Settings\*\Application Data\Mozilla\Firefox\Profiles\*\key*.db,lazy_ntfs,
      317,Password XP,Communications,Documents and Settings\*\Application Data\Mozilla\Firefox\Profiles\*\signon*.*,lazy_ntfs,
      318,Password XP,Communications,Documents and Settings\*\Application Data\Mozilla\Firefox\Profiles\*\logins.json,lazy_ntfs,
      319,Sessionstore XP,Communications,Documents and Settings\*\Application Data\Mozilla\Firefox\Profiles\*\sessionstore*,lazy_ntfs,
      320,Index.dat History,Communications,Documents and Settings\*\Local Settings\History\History.IE5\index.dat,lazy_ntfs,
      321,Index.dat History subdirectory,Communications,Documents and Settings\*\Local Settings\History\History.IE5\*\index.dat,lazy_ntfs,
      322,Index.dat cookies,Communications,Documents and Settings\*\Cookies\index.dat,lazy_ntfs,
      323,Index.dat UserData,Communications,Documents and Settings\*\Application Data\Microsoft\Internet Explorer\UserData\index.dat,lazy_ntfs,
      324,Index.dat Office XP,Communications,Documents and Settings\*\Application Data\Microsoft\Office\Recent\index.dat,lazy_ntfs,
      325,Index.dat Office,Communications,Users\*\AppData\Roaming\Microsoft\Office\Recent\index.dat,lazy_ntfs,
      326,Local Internet Explorer folder,Communications,Users\*\AppData\Local\Microsoft\Internet Explorer\**10,lazy_ntfs,
      327,Roaming Internet Explorer folder,Communications,Users\*\AppData\Roaming\Microsoft\Internet Explorer\**10,lazy_ntfs,
      328,IE 9/10 History,Communications,Users\*\AppData\Local\Microsoft\Windows\History\**10,lazy_ntfs,
      329,IE 9/10 Cookies,Communications,Users\*\AppData\Local\Microsoft\Windows\Cookies\**10,lazy_ntfs,
      330,IE 9/10 Download History,Communications,Users\*\AppData\Local\Microsoft\Windows\IEDownloadHistory\**10,lazy_ntfs,
      331,IE 11 Metadata,Communications,Users\*\AppData\Local\Microsoft\Windows\WebCache\*,lazy_ntfs,
      332,IE 11 Cookies,Communications,Users\*\AppData\Local\Microsoft\Windows\INetCookies\**10,lazy_ntfs,
      333,Opera - Local Folder,Communications,Users\*\AppData\Local\Opera Software\Opera Stable\**10,lazy_ntfs,Grabs entire contents of the Opera AppData\Local folder
      334,Opera - Roaming Folder,Communications,Users\*\AppData\Roaming\Opera Software\Opera Stable\**10,lazy_ntfs,Grabs entire contents of the Opera AppData\Roaming folder
      335,Puffin - data.db,Communications,Users\*\AppData\Local\PuffinSecureBrowser\data.db,lazy_ntfs,Grabs an important database file that contains browser history
      336,Puffin - Autocomplete Data,Communications,Users\*\AppData\Local\PuffinSecureBrowser\autocompletes.dat,lazy_ntfs,Grabs a file that stores autocomplete data
      337,Puffin - Password Forms Data,Communications,Users\*\AppData\Local\PuffinSecureBrowser\passwordForms.dat,lazy_ntfs,Grabs a file that stores some saved password data
      338,Puffin - Password (Encrypted),Communications,Users\*\AppData\Local\PuffinSecureBrowser\credential.dat,lazy_ntfs,Grabs a file that stores passwords in an encrypted format
      339,Puffin - Subscription Data,Communications,Users\*\AppData\Local\PuffinSecureBrowser\subscription,lazy_ntfs,Grabs a file that stores the user's email address that's associated with their Puffin subscription
      340,Puffin - Cookies,Communications,Users\*\AppData\Local\PuffinSecureBrowser\cookies.dat,lazy_ntfs,Grabs a file that stores information related to cookies
      341,Puffin - Image Cache,Communications,Users\*\AppData\Local\PuffinSecureBrowser\image_cache\**10,lazy_ntfs,Grabs a directory that caches images from websites visited
      342,AppData,UserData,Users\*\AppData\**10,lazy_ntfs,
      343,Audio files,Multimedia,**10\regex:*.+\.(3gp|aa|aac|act|aiff|alac|amr|ape|au|awb|dss|dvf|flac|gsm|iklax|ivs|m4a|m4b|m4p|mmf|mp3|mpc|msv|nmf|ogg|oga|mogg|opus|ra|rm|raw|rf64|sln|tta|voc|vox|wav|wma|wv|webm),ntfs,Covers most (if not all) audio file formats
      344,Excel and Excel-like Documents,Documents,**10\regex:*.+\.(xls|xlsx|csv|tsv|xlt|xlm|xlsm|xltx|xltm|xlsb|xla|xlam|xll|xlw|ods|fodp|qpw),ntfs,"Covers all document file formats for Excel, OpenOffice, LibreOffice, Apache OpenOffice, WPS Office, SoftMaker Office, and more"
      345,PDF and PDF-like Documents,Documents,**10\regex:*.+\.(pdf|xps|oxps),ntfs,Covers all PDF and PDF-like document formats
      346,Picture files,Multimedia,**10\regex:*.+\.(ai|bmp|bpg|cdr|cpc|eps|exr|flif|gif|heif|ilbm|ima|jp2|j2k|jpf|jpm|jpg2|j2c|jpc|jpx|mj2jpeg|jpg|jxl|kra|ora|pcx|pgf|pgm|png|pnm|ppm|psb|psd|psp|svg|tga|tiff|webp|xaml|xcf),ntfs,Covers most (if not all) picture file formats
      347,SQLite Files (.db* and .sqlite*),Databases,**10\regex:*.+\.(db*|sqlite*|),ntfs,Covers all common file extensions for SQLite databases
      348,Video files,Multimedia,**10\regex:*.+\.(3g2|3gp|amv|asf|avi|drc|flv|f4v|f4p|f4a|f4b|gif|gifv|m4v|mkv|mov|qt|mp4|m4p|mpg|mpeg|m2v|mp2|mpe|mpv|mts|m2ts|ts|mxf|nsv|ogv|ogg|rm|rmvb|roq|svi|viv|vob|webm|wmv|yuv),ntfs,Covers most (if not all) video file formats
      349,Zips,Archives,**10\*.zip,lazy_ntfs,This is an example of how to walk a drive for a file mask. Probably do not want to use this one as is
      350,Word and Word-like Documents,Documents,**10\regex:*.+\.(doc|docx|docm|dotx|dotm|docb|dot|wbk|odt|fodt|rtf|wp*|tmd),ntfs,"Covers all document file formats for Word, OpenOffice, LibreOffice, Apache OpenOffice, WPS Office, SoftMaker Office, and more"
      351,User Files - Desktop,LiveUserFiles,Users\*\Desktop\**10,lazy_ntfs,
      352,User Files - Documents,LiveUserFiles,Users\*\Documents\**10,lazy_ntfs,
      353,User Files - Downloads,LiveUserFiles,Users\*\Downloads\**10,lazy_ntfs,
      354,User Files - Dropbox,LiveUserFiles,Users\*\Dropbox*\**10,lazy_ntfs,
      355,TorrentClients - BitTorrent,FileDownload,Users\*\AppData\Roaming\BitTorrent\*.dat,lazy_ntfs,
      356,DC++ Chat Logs,FileDownload,Users\*\AppData\Local\DC++\Logs\**10,lazy_ntfs,Locates DC++ hub/chat logs and copies them. Current as of version 0.868.
      357,Freenet,File Downloads,Users\*\AppData\Local\Freenet\node*,lazy_ntfs,
      358,Freenet,File Downloads,Users\*\AppData\Local\Freenet\*completed.list.downloads,lazy_ntfs,
      359,Freenet,File Downloads,Users\*\AppData\Local\Freenet\*completed.list.uploads,lazy_ntfs,
      360,Freenet,File Downloads,Users\*\AppData\Local\Freenet\*.bak,lazy_ntfs,
      361,Freenet,File Downloads,Users\*\AppData\Local\Freenet\downloads\**10,lazy_ntfs,
      362,FrostWire Downloads,FileDownload,Users\*\Documents\FrostWire\Torrent Data\**10,lazy_ntfs,Locates files downloaded that land in the default location as specified by FrostWire
      363,FrostWire AppData,FileDownload,Users\*\.frostwire5\frostwire.props,lazy_ntfs,Locates a file that contains important information about the instance of FrostWire on the user's system
      364,FrostWire AppData,FileDownload,Users\*\.frostwire5\itunes.props,lazy_ntfs,Locates a file that contains important information about the instance of FrostWire on the user's system
      365,Gigatribe Files Windows Vista/7/8/10,FileDownload,Users\*\AppData\Local\Shalsoft\**10,lazy_ntfs,Locates Gigatribe files and copies them
      366,Gigatribe Files Windows XP,FileDownload,Documents and Settings\*\*\Application Data\Gigatribe\**10,lazy_ntfs,Locates Gigatribe files and copies them. Different path depending on the Operating System language. In Swedish the location is C:\Documents and Settings\<username>\Lokala Inställningar\Application Data\Gigatribe
      367,Gigatribe Files Windows XP,FileDownload,Documents and Settings\*\*\Application Data\Shalsoft\**10,lazy_ntfs,Locates Gigatribe files and copies them. Different path depending on the Operating System language. In Swedish the location is C:\Documents and Settings\<username>\Lokala Inställningar\Application Data\Shalsoft
      368,Usenet Clients - NZBGet Log File,FileDownload,ProgramData\NZBGet\nzbget.log,lazy_ntfs,Locates NZBGet download log file
      369,Usenet Clients - NZBGet NZBs,FileDownload,ProgramData\NZBGet\nzb\*,lazy_ntfs,Locates NZBGet NZB files that were used by the user
      370,Usenet Clients - Newsbin Pro,FileDownload,Users\*\AppData\Local\Newsbin\Downloaded.db3,lazy_ntfs,Locates Newsbin Pro download log database
      371,Usenet Clients - Newsleecher,FileDownload,Users\*\AppData\Roaming\NewsLeecher\downloaded.dat,lazy_ntfs,Locates Newsleecher download .dat file
      372,Nicotine++ Logs,FileDownload,Users\%User%\AppData\Roaming\nicotine\logs\**10,lazy_ntfs,"Locates Nicotine++ chat logs, room logs, transfer logs, and debug logs (if enabled)"
      373,Nicotine++ Incomplete Downloads,FileDownload,Users\%User%\AppData\Roaming\nicotine\incomplete\**10,lazy_ntfs,Locates files that did not finish downloading
      374,Nicotine++ Buddyfiles.db,FileDownload,Users\%User%\AppData\Roaming\nicotine\buddyfiles.db\**10,lazy_ntfs,Locates a DB that appears to include shared files from a user's buddy list
      375,Nicotine++ Buddystreams.db,FileDownload,Users\%User%\AppData\Roaming\nicotine\buddystreams.db\**10,lazy_ntfs,Locates a DB that appears to include shared files from a user's buddy list
      376,Nicotine++ Buddymtimes.db,FileDownload,Users\%User%\AppData\Roaming\nicotine\buddymtimes.db\**10,lazy_ntfs,"Locates a DB that appears to enumerate which files the user is sharing to their buddy list, from a folder level"
      377,Nicotine++ Buddyfileindex.db,FileDownload,Users\%User%\AppData\Roaming\nicotine\buddyfileindex.db\**10,lazy_ntfs,"Locates a DB that appears to enumerate which files the user is sharing to their buddy list, from a file level"
      378,Nicotine++ Buddywordindex.db,FileDownload,Users\%User%\AppData\Roaming\nicotine\buddywordindex.db\**10,lazy_ntfs,Unknown what this is for at this time
      379,Nicotine++ Config Files,FileDownload,Users\%User%\AppData\Roaming\nicotine\config\**10,lazy_ntfs,Locates config files
      380,Nicotine++ User Shares,FileDownload,Users\%User%\AppData\Roaming\nicotine\usershares\**10,lazy_ntfs,Locates a DB that appears to store a list of files per user that they are sharing within Nicotine++. Note: this requires the user to right-click -> browse files shared by that user
      381,Nicotine++ Downloads.json,FileDownload,Users\%User%\AppData\Roaming\nicotine\downloads.json*,lazy_ntfs,Locates downloads.json
      382,Nicotine++ Uploads.json,FileDownload,Users\%User%\AppData\Roaming\nicotine\uploads.json*,lazy_ntfs,Locates uploads.json
      383,Usenet Clients - SABnzbd Download Logs,FileDownload,Users\*\AppData\Local\sabnzbd\logs\sabnzbd.log,lazy_ntfs,Locates SABnzbd download log
      384,Usenet Clients - SABnzbd History.db,FileDownload,Users\*\AppData\Local\sabnzbd\admin\history1.db,lazy_ntfs,Locates SABnzbd history log
      385,Shareaza Logs,FileDownload,Users\*\AppData\Roaming\Shareaza\**10,lazy_ntfs,Locates Shareaza logs and copies them.
      386,Soulseek Chat Logs,FileDownload,Users\*\AppData\Local\SoulseekQt\Soulseek Chat Logs\**10,lazy_ntfs,Locates Soulseek chat logs and copies them. Chat logs are in plaintext. Current as of version 2019.7.22.
      387,Soulseek Search History/Shared Folders/Settings,FileDownload,Users\*\AppData\Local\SoulseekQt\1\*.dat,lazy_ntfs,"Locates .dat file(s) containing: search history, active searches (search_record), current shared folders (shared_file_folder), and wish list items (wish_list_item)."
      388,Torrents,FileDownload,**10\*.torrent,lazy_ntfs,
      389,Usenet (NZB) Files,FileDownload,**10\*.nzb,lazy_ntfs,
      390,TorrentClients - qBittorrent,FileDownload,Users\*\AppData\Roaming\qBittorrent\*.ini,lazy_ntfs,
      391,TorrentClients - qBittorrent,FileDownload,Users\*\AppData\Local\qBittorrent\logs\*,lazy_ntfs,
      392,TorrentClients - uTorrent,FileDownload,Users\*\AppData\Roaming\uTorrent\*.dat,lazy_ntfs,
      393,Debian WSL /etc/debian_version,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\TheDebianProject.DebianGNULinux_*\LocalState\rootfs\etc\debian_version,lazy_ntfs,
      394,Debian WSL /etc/fstab,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\TheDebianProject.DebianGNULinux_*\LocalState\rootfs\etc\fstab,lazy_ntfs,
      395,Debian WSL /etc/os-release,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\TheDebianProject.DebianGNULinux_*\LocalState\rootfs\etc\os-release,lazy_ntfs,
      396,Debian WSL /etc/passwd,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\TheDebianProject.DebianGNULinux_*\LocalState\rootfs\etc\passwd,lazy_ntfs,
      397,Debian WSL /etc/group,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\TheDebianProject.DebianGNULinux_*\LocalState\rootfs\etc\group,lazy_ntfs,
      398,Debian WSL /etc/shadow,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\TheDebianProject.DebianGNULinux_*\LocalState\rootfs\etc\shadow,lazy_ntfs,
      399,Debian WSL /etc/timezone,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\TheDebianProject.DebianGNULinux_*\LocalState\rootfs\etc\timezone,lazy_ntfs,
      400,Debian WSL /etc/hostname,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\TheDebianProject.DebianGNULinux_*\LocalState\rootfs\etc\hostname,lazy_ntfs,
      401,Debian WSL /etc/hosts,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\TheDebianProject.DebianGNULinux_*\LocalState\rootfs\etc\hosts,lazy_ntfs,
      402,Debian WSL /etc/crontab,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\TheDebianProject.DebianGNULinux_*\LocalState\rootfs\etc\crontab,lazy_ntfs,
      403,Debian WSL /etc/bash.bashrc,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\TheDebianProject.DebianGNULinux_*\LocalState\rootfs\etc\bash.bashrc,lazy_ntfs,
      404,Debian WSL /etc/profile,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\TheDebianProject.DebianGNULinux_*\LocalState\rootfs\etc\profile,lazy_ntfs,
      405,Debian WSL .bash_history,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\TheDebianProject.DebianGNULinux_*\LocalState\rootfs\**10\.bash_history,lazy_ntfs,
      406,Debian WSL .bashrc,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\TheDebianProject.DebianGNULinux_*\LocalState\rootfs\**10\.bashrc,lazy_ntfs,
      407,Debian WSL .profile,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\TheDebianProject.DebianGNULinux_*\LocalState\rootfs\**10\.profile,lazy_ntfs,
      408,Debian WSL User Crontabs,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\TheDebianProject.DebianGNULinux_*\LocalState\rootfs\var\spool\cron\crontabs\**10,lazy_ntfs,
      409,Debian WSL Apt Logs,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\TheDebianProject.DebianGNULinux_*\LocalState\rootfs\var\log\apt\**10\*.log,lazy_ntfs,
      410,Debian WSL ext4.vhdx,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\TheDebianProject.DebianGNULinux_*\LocalState\ext4.vhdx,lazy_ntfs,
      411,Kali WSL /etc/debian_version,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\KaliLinux.54290C8133FEE_*\LocalState\rootfs\etc\debian_version,lazy_ntfs,
      412,Kali WSL /etc/fstab,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\KaliLinux.54290C8133FEE_*\LocalState\rootfs\etc\fstab,lazy_ntfs,
      413,Kali WSL /etc/os-release,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\KaliLinux.54290C8133FEE_*\LocalState\rootfs\etc\os-release,lazy_ntfs,
      414,Kali WSL /etc/passwd,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\KaliLinux.54290C8133FEE_*\LocalState\rootfs\etc\passwd,lazy_ntfs,
      415,Kali WSL /etc/group,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\KaliLinux.54290C8133FEE_*\LocalState\rootfs\etc\group,lazy_ntfs,
      416,Kali WSL /etc/shadow,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\KaliLinux.54290C8133FEE_*\LocalState\rootfs\etc\shadow,lazy_ntfs,
      417,Kali WSL /etc/timezone,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\KaliLinux.54290C8133FEE_*\LocalState\rootfs\etc\timezone,lazy_ntfs,
      418,Kali WSL /etc/hostname,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\KaliLinux.54290C8133FEE_*\LocalState\rootfs\etc\hostname,lazy_ntfs,
      419,Kali WSL /etc/hosts,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\KaliLinux.54290C8133FEE_*\LocalState\rootfs\etc\hosts,lazy_ntfs,
      420,Kali WSL /etc/crontab,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\KaliLinux.54290C8133FEE_*\LocalState\rootfs\etc\crontab,lazy_ntfs,
      421,Kali WSL /etc/bash.bashrc,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\KaliLinux.54290C8133FEE_*\LocalState\rootfs\etc\bash.bashrc,lazy_ntfs,
      422,Kali WSL /etc/profile,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\KaliLinux.54290C8133FEE_*\LocalState\rootfs\etc\profile,lazy_ntfs,
      423,Kali WSL .bash_history,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\KaliLinux.54290C8133FEE_*\LocalState\rootfs\**10\.bash_history,lazy_ntfs,
      424,Kali WSL .bashrc,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\KaliLinux.54290C8133FEE_*\LocalState\rootfs\**10\.bashrc,lazy_ntfs,
      425,Kali WSL .profile,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\KaliLinux.54290C8133FEE_*\LocalState\rootfs\**10\.profile,lazy_ntfs,
      426,Kali WSL User Crontabs,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\KaliLinux.54290C8133FEE_*\LocalState\rootfs\var\spool\cron\crontabs\**10,lazy_ntfs,
      427,Kali WSL Apt Logs,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\KaliLinux.54290C8133FEE_*\LocalState\rootfs\var\log\apt\**10\*.log,lazy_ntfs,
      428,Kali WSL ext4.vhdx,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\KaliLinux.54290C8133FEE_*\LocalState\ext4.vhdx,lazy_ntfs,
      429,SUSE Linux Enterprise Server WSL /etc/os-release,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\46932SUSE.SUSELinuxEnterpriseServer*\LocalState\rootfs\etc\os-release,lazy_ntfs,
      430,SUSE Linux Enterprise Server WSL /etc/fstab,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\46932SUSE.SUSELinuxEnterpriseServer*\LocalState\rootfs\etc\fstab,lazy_ntfs,
      431,SUSE Linux Enterprise Server WSL /etc/passwd,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\46932SUSE.SUSELinuxEnterpriseServer*\LocalState\rootfs\etc\passwd,lazy_ntfs,
      432,SUSE Linux Enterprise Server WSL /etc/group,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\46932SUSE.SUSELinuxEnterpriseServer*\LocalState\rootfs\etc\group,lazy_ntfs,
      433,SUSE Linux Enterprise Server WSL /etc/shadow,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\46932SUSE.SUSELinuxEnterpriseServer*\LocalState\rootfs\etc\shadow,lazy_ntfs,
      434,SUSE Linux Enterprise Server WSL /etc/timezone,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\46932SUSE.SUSELinuxEnterpriseServer*\LocalState\rootfs\etc\timezone,lazy_ntfs,
      435,SUSE Linux Enterprise Server WSL /etc/hostname,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\46932SUSE.SUSELinuxEnterpriseServer*\LocalState\rootfs\etc\hostname,lazy_ntfs,
      436,SUSE Linux Enterprise Server WSL /etc/hosts,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\46932SUSE.SUSELinuxEnterpriseServer*\LocalState\rootfs\etc\hosts,lazy_ntfs,
      437,SUSE Linux Enterprise Server WSL /etc/bash.bashrc,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\46932SUSE.SUSELinuxEnterpriseServer*\LocalState\rootfs\etc\bash.bashrc,lazy_ntfs,
      438,SUSE Linux Enterprise Server WSL /etc/profile,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\46932SUSE.SUSELinuxEnterpriseServer*\LocalState\rootfs\etc\profile,lazy_ntfs,
      439,SUSE Linux Enterprise Server WSL .bash_history,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\46932SUSE.SUSELinuxEnterpriseServer*\LocalState\rootfs\**10\.bash_history,lazy_ntfs,
      440,SUSE Linux Enterprise Server WSL .bashrc,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\46932SUSE.SUSELinuxEnterpriseServer*\LocalState\rootfs\**10\.bashrc,lazy_ntfs,
      441,SUSE Linux Enterprise Server WSL .profile,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\46932SUSE.SUSELinuxEnterpriseServer*\LocalState\rootfs\**10\.profile,lazy_ntfs,
      442,SUSE Linux Enterprise Server WSL ext4.vhdx,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\46932SUSE.SUSELinuxEnterpriseServer*\LocalState\ext4.vhdx,lazy_ntfs,
      443,Ubuntu WSL /etc/os-release,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\CanonicalGroupLimited.Ubuntu*\LocalState\rootfs\etc\os-release,lazy_ntfs,
      444,Ubuntu WSL /etc/fstab,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\CanonicalGroupLimited.Ubuntu*\LocalState\rootfs\etc\fstab,lazy_ntfs,
      445,Ubuntu WSL /etc/passwd,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\CanonicalGroupLimited.Ubuntu*\LocalState\rootfs\etc\passwd,lazy_ntfs,
      446,Ubuntu WSL /etc/group,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\CanonicalGroupLimited.Ubuntu*\LocalState\rootfs\etc\group,lazy_ntfs,
      447,Ubuntu WSL /etc/shadow,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\CanonicalGroupLimited.Ubuntu*\LocalState\rootfs\etc\shadow,lazy_ntfs,
      448,Ubuntu WSL /etc/timezone,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\CanonicalGroupLimited.Ubuntu*\LocalState\rootfs\etc\timezone,lazy_ntfs,
      449,Ubuntu WSL /etc/hostname,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\CanonicalGroupLimited.Ubuntu*\LocalState\rootfs\etc\hostname,lazy_ntfs,
      450,Ubuntu WSL /etc/hosts,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\CanonicalGroupLimited.Ubuntu*\LocalState\rootfs\etc\hosts,lazy_ntfs,
      451,Ubuntu WSL /etc/crontab,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\CanonicalGroupLimited.Ubuntu*\LocalState\rootfs\etc\crontab,lazy_ntfs,
      452,Ubuntu WSL /etc/bash.bashrc,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\CanonicalGroupLimited.Ubuntu*\LocalState\rootfs\etc\bash.bashrc,lazy_ntfs,
      453,Ubuntu WSL /etc/profile,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\CanonicalGroupLimited.Ubuntu*\LocalState\rootfs\etc\profile,lazy_ntfs,
      454,Ubuntu WSL .bash_history,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\CanonicalGroupLimited.Ubuntu*\LocalState\rootfs\**10\.bash_history,lazy_ntfs,
      455,Ubuntu WSL .bashrc,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\CanonicalGroupLimited.Ubuntu*\LocalState\rootfs\**10\.bashrc,lazy_ntfs,
      456,Ubuntu WSL .profile,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\CanonicalGroupLimited.Ubuntu*\LocalState\rootfs\**10\.profile,lazy_ntfs,
      457,Ubuntu WSL User Crontabs,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\CanonicalGroupLimited.Ubuntu*\LocalState\rootfs\var\spool\cron\crontabs\**10,lazy_ntfs,
      458,Ubuntu WSL Apt Logs,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\CanonicalGroupLimited.Ubuntu*\LocalState\rootfs\var\log\apt\**10\*.log,lazy_ntfs,
      459,Ubuntu WSL ext4.vhdx,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\CanonicalGroupLimited.Ubuntu*\LocalState\ext4.vhdx,lazy_ntfs,
      460,openSUSE WSL /etc/os-release,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\46932SUSE.openSUSE*Leap*\LocalState\rootfs\etc\os-release,lazy_ntfs,
      461,openSUSE WSL /etc/fstab,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\46932SUSE.openSUSE*Leap*\LocalState\rootfs\etc\fstab,lazy_ntfs,
      462,openSUSE WSL /etc/passwd,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\46932SUSE.openSUSE*Leap*\LocalState\rootfs\etc\passwd,lazy_ntfs,
      463,openSUSE WSL /etc/group,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\46932SUSE.openSUSE*Leap*\LocalState\rootfs\etc\group,lazy_ntfs,
      464,openSUSE WSL /etc/shadow,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\46932SUSE.openSUSE*Leap*\LocalState\rootfs\etc\shadow,lazy_ntfs,
      465,openSUSE WSL /etc/timezone,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\46932SUSE.openSUSE*Leap*\LocalState\rootfs\etc\timezone,lazy_ntfs,
      466,openSUSE WSL /etc/hostname,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\46932SUSE.openSUSE*Leap*\LocalState\rootfs\etc\hostname,lazy_ntfs,
      467,openSUSE WSL /etc/hosts,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\46932SUSE.openSUSE*Leap*\LocalState\rootfs\etc\hosts,lazy_ntfs,
      468,openSUSE WSL /etc/bash.bashrc,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\46932SUSE.openSUSE*Leap*\LocalState\rootfs\etc\bash.bashrc,lazy_ntfs,
      469,openSUSE WSL /etc/profile,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\46932SUSE.openSUSE*Leap*\LocalState\rootfs\etc\profile,lazy_ntfs,
      470,openSUSE WSL .bash_history,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\46932SUSE.openSUSE*Leap*\LocalState\rootfs\**10\.bash_history,lazy_ntfs,
      471,openSUSE WSL .bashrc,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\46932SUSE.openSUSE*Leap*\LocalState\rootfs\**10\.bashrc,lazy_ntfs,
      472,openSUSE WSL .profile,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\46932SUSE.openSUSE*Leap*\LocalState\rootfs\**10\.profile,lazy_ntfs,
      473,openSUSE WSL ext4.vhdx,Windows Subsystem for Linux,Users\*\AppData\Local\Packages\46932SUSE.openSUSE*Leap*\LocalState\ext4.vhdx,lazy_ntfs,
      474,Diagnostic Logs for WSA,Windows Subsystem for Android,Users\*\AppData\Local\Packages\MicrosoftCorporationII.WindowsSubsystemForAndroid_8wekyb3d8bbwe\LocalState\diagnostics\logcat\*.log,lazy_ntfs,Filenames should be %timestamp%.log
      475,App download artifacts (PNG),Windows Subsystem for Android,Users\*\AppData\Local\Packages\MicrosoftCorporationII.WindowsSubsystemForAndroid_8wekyb3d8bbwe\LocalCache\*.png,lazy_ntfs,Will provide examiners with indicators of which apps were downloaded
      476,App download artifacts (ICO),Windows Subsystem for Android,Users\*\AppData\Local\Packages\MicrosoftCorporationII.WindowsSubsystemForAndroid_8wekyb3d8bbwe\LocalCache\*.ico,lazy_ntfs,Will provide examiners with indicators of which apps were downloaded WHEN since .ico files appear immediately when download of an application completes
      477,Appcompatdb.json,Windows Subsystem for Android,Users\*\AppData\Local\Packages\MicrosoftCorporationII.WindowsSubsystemForAndroid_8wekyb3d8bbwe\LocalState\appcompatdb.json,lazy_ntfs,"Grabs the appcompatdb.json, unknown exactly what this is but further relevance could be uncovered after more research is conducted"
      478,userdata.vhdx,Windows Subsystem for Android,Users\*\AppData\Local\Packages\MicrosoftCorporationII.WindowsSubsystemForAndroid_8wekyb3d8bbwe\LocalCache\userdata.vhdx,lazy_ntfs,Grabs the user's data which appears to be stored in a VHDX
      479,$Boot,FileSystem,$Boot,ntfs,
      480,$J,FileSystem,$Extend\$UsnJrnl:$J,ntfs,
      481,$Max,FileSystem,$Extend\$UsnJrnl:$Max,ntfs,
      482,$J,FileSystem,$Extend\$J,ntfs,This is for the use case when you're running this Target against a mounted VHDX with these files already pulled from a live system. The above Targets are looking for the files as an ADS whereas once they are already pulled they no longer match the ADS criteria and therefore are missed
      483,$Max,FileSystem,$Extend\$Max,ntfs,This is for the use case when you're running this Target against a mounted VHDX with these files already pulled from a live system. The above Targets are looking for the files as an ADS whereas once they are already pulled they no longer match the ADS criteria and therefore are missed
      484,$LogFile,FileSystem,$LogFile,ntfs,
      485,$MFT,FileSystem,$MFT,ntfs,
      486,$MFTMirr,FileSystem,$MFTMirr,ntfs,$MFTMirr is a redundant copy of the first four (4) records of the MFT.
      487,$T,FileSystem,$Extend\$RmMetadata\$TxfLog\$Tops:$T,ntfs,
      488,$T,FileSystem,$Extend\$RmMetadata\$TxfLog\$T,ntfs,This is for the use case when you're running this Target against a mounted VHDX with these files already pulled from a live system. The above Target is looking for the files as an ADS whereas once they are already pulled they no longer match the ADS criteria and therefore are missed
      489,Amcache,ApplicationCompatibility,Windows\AppCompat\Programs\Amcache.hve,lazy_ntfs,
      490,Amcache,ApplicationCompatibility,Windows.old\Windows\AppCompat\Programs\Amcache.hve,lazy_ntfs,
      491,Amcache transaction files,ApplicationCompatibility,Windows\AppCompat\Programs\Amcache.hve.LOG*,lazy_ntfs,
      492,Amcache transaction files,ApplicationCompatibility,Windows.old\Windows\AppCompat\Programs\Amcache.hve.LOG*,lazy_ntfs,
      493,AppCompat PCA Folder,AppCompat,Windows\appcompat\pca,lazy_ntfs,
      494,Application Event Log XP,EventLogs,Windows\System32\config\AppEvent.evt,lazy_ntfs,
      495,Application Event Log XP,EventLogs,Windows.old\Windows\System32\config\AppEvent.evt,lazy_ntfs,
      496,Application Event Log Win7+,EventLogs,Windows\System32\winevt\logs\application.evtx,lazy_ntfs,
      497,Application Event Log Win7+,EventLogs,Windows.old\Windows\System32\winevt\logs\application.evtx,lazy_ntfs,
      498,Asset Advisor Log,Executables,Windows\CCM\Logs\AssetAdvisor.log\EncapsulationLogging.hve,lazy_ntfs,
      499,BCD,Registry,Boot\BCD,lazy_ntfs,
      500,BCD Logs,Registry,Boot\BCD.LOG*,lazy_ntfs,
      501,BITS files,Persistence,ProgramData\Microsoft\Network\Downloader\**10,lazy_ntfs,
      502,System CryptnetUrlCache,FileKnowledge,Windows\System32\config\systemprofile\AppData\LocalLow\Microsoft\CryptnetUrlCache\**10,lazy_ntfs,
      503,User CryptnetUrlCache,FileKnowledge,Users\*\AppData\LocalLow\Microsoft\CryptnetUrlCache\**10,lazy_ntfs,
      504,INetCache,FileKnowledge,Users\*\AppData\Local\Microsoft\Windows\INetCache\IE\**10,lazy_ntfs,
      505,EncapsulationLogging,Executables,Windows\Appcompat\Programs\EncapsulationLogging.hve,lazy_ntfs,
      506,EncapsulationLogging,Executables,Windows.old\Windows\Appcompat\Programs\EncapsulationLogging.hve,lazy_ntfs,
      507,EncapsulationLogging Logs,Executables,Windows\Appcompat\Programs\EncapsulationLogging.hve.log*,lazy_ntfs,
      508,EncapsulationLogging Logs,Executables,Windows.old\Windows\Appcompat\Programs\EncapsulationLogging.hve.log*,lazy_ntfs,
      509,Event logs Win7+,EventLogs,Windows\System32\winevt\logs\System.evtx,lazy_ntfs,
      510,Event logs Win7+,EventLogs,Windows.old\Windows\System32\winevt\logs\System.evtx,lazy_ntfs,
      511,Event logs Win7+,EventLogs,Windows\System32\winevt\logs\Security.evtx,lazy_ntfs,
      512,Event logs Win7+,EventLogs,Windows.old\Windows\System32\winevt\logs\Security.evtx,lazy_ntfs,
      513,Event logs Win7+,EventLogs,Windows\System32\winevt\Logs\Microsoft-Windows-TerminalServices-LocalSessionManager%4Operational.evtx\Microsoft-Windows-TerminalServices-LocalSessionManager%4Operational.evtx,lazy_ntfs,
      514,Event logs Win7+,EventLogs,Windows\System32\winevt\Logs\Microsoft-Windows-TerminalServices-RemoteConnectionManager%4Operational.evtx,lazy_ntfs,
      515,Event logs XP,EventLogs,Windows\System32\config\*.evt,lazy_ntfs,
      516,Event logs Win7+,EventLogs,Windows\System32\winevt\logs\*.evtx,lazy_ntfs,
      517,Event logs Win7+,EventLogs,Windows.old\Windows\System32\winevt\logs\*.evtx,lazy_ntfs,
      518,WDI Trace Logs 1,Event Trace Logs,Windows\System32\WDI\LogFiles\*.etl*,lazy_ntfs,
      519,WDI Trace Logs 1,Event Trace Logs,Windows.old\Windows\System32\WDI\LogFiles\*.etl*,lazy_ntfs,
      520,WDI Trace Logs 2,Event Trace Logs,Windows\System32\WDI\{*\**10,lazy_ntfs,
      521,WDI Trace Logs 2,Event Trace Logs,Windows.old\Windows\System32\WDI\{*\**10,lazy_ntfs,
      522,WMI Trace Logs,Event Trace Logs,Windows\System32\LogFiles\WMI\**10,lazy_ntfs,
      523,WMI Trace Logs,Event Trace Logs,Windows.old\Windows\System32\LogFiles\WMI\**10,lazy_ntfs,
      524,SleepStudy Trace Logs,Event Trace Logs,Windows\System32\SleepStudy\**10,lazy_ntfs,
      525,SleepStudy Trace Logs,Event Trace Logs,Windows.old\Windows\System32\SleepStudy\**10,lazy_ntfs,
      526,Energy-NTKL Trace Logs,Event Trace Logs,ProgramData\Microsoft\Windows\PowerEfficiency Diagnostics\energy-ntkl.etl,lazy_ntfs,
      527,Delivery Optimization Trace Logs,Event Trace Logs,Windows\ServiceProfiles\NetworkService\AppData\Local\Microsoft\Windows\DeliveryOptimization\Logs\*.etl*,lazy_ntfs,
      528,EventTranscript.db,SystemEvents,ProgramData\Microsoft\Diagnosis\EventTranscript\EventTranscript.db*,lazy_ntfs,
      529,EventTranscript.db,SystemEvents,Windows.old\ProgramData\Microsoft\Diagnosis\EventTranscript\EventTranscript.db*,lazy_ntfs,
      530,Microsoft Office Diagnostic Logs,SystemEvents,Users\%User%\AppData\Local\Temp\Diagnostics\**10,lazy_ntfs,
      531,Exchange client access log files,Logs,Program Files\Microsoft\Exchange Server\*\Logging\**10\*.log,lazy_ntfs,Highly dependent on Exchange configuration
      532,Exchange Server Modified Compiled Files,Apps,Windows\Microsoft.NET\Framework*\v*\Temporary ASP.NET Files\**10\Regex:*.\b[a-zA-Z0-9_-]{8}\b.compiled,ntfs,Highly dependent on Exchange configuration
      533,Exchange Server Modified Compiled Files,Apps,inetpub\wwwroot\aspnet_client\**10\Regex:*.\b[a-zA-Z0-9_-]{8}\b.compiled,ntfs,Highly dependent on Exchange configuration
      534,Exchange Server Modified Compiled Files,Apps,inetpub\wwwroot\aspnet_client\system_web\**10\Regex:*.\b[a-zA-Z0-9_-]{8}\b.compiled,ntfs,Highly dependent on Exchange configuration
      535,Exchange Server Modified Compiled Files,Apps,Program Files\Microsoft\Exchange Server\V15\FrontEnd\HttpProxy\owa\auth\**10\Regex:*.\b[a-zA-Z0-9_-]{8}\b.compiled,ntfs,Highly dependent on Exchange configuration
      536,Local Group Policy INI Files,Communication,Windows\System32\grouppolicy\*.ini,lazy_ntfs,
      537,Local Group Policy INI Files,Communication,Windows.old\Windows\System32\grouppolicy\*.ini,lazy_ntfs,
      538,Local Group Policy Files - Registry Policy Files,Communication,Windows\System32\grouppolicy\*.pol,lazy_ntfs,
      539,Local Group Policy Files - Registry Policy Files,Communication,Windows.old\Windows\System32\grouppolicy\*.pol,lazy_ntfs,
      540,Local Group Policy Files - Startup/Shutdown Scripts,Communication,Windows\System32\grouppolicy\*\Scripts\**10,lazy_ntfs,
      541,Local Group Policy Files - Startup/Shutdown Scripts,Communication,Windows.old\Windows\System32\grouppolicy\*\Scripts\**10,lazy_ntfs,
      542,IIS applicationHost.config,Apps,Windows\System32\inetsrv\config\applicationHost.config,lazy_ntfs,This configuration file stores the settings for all your Web sites and applications.
      543,IIS administration.config,Apps,Windows\System32\inetsrv\config\administration.config,lazy_ntfs,This configuration file stores the settings for IIS management.
      544,IIS redirection.config,Apps,Windows\System32\inetsrv\config\redirection.config,lazy_ntfs,This configuration file contains the settings that indicate the location where the centralized configuration files are stored.
      545,web.config,Apps,inetpub\wwwroot\**10\web.config,lazy_ntfs,The web.config is a file that is read by IIS and the ASP.NET Core Module to configure an app hosted with IIS.
      546,LNK Files from Recent,LNKFiles,Users\*\AppData\Roaming\Microsoft\Windows\Recent\**10,lazy_ntfs,Also includes automatic and custom jumplist directories
      547,LNK Files from Microsoft Office Recent,LNKFiles,Users\*\AppData\Roaming\Microsoft\Office\Recent\**10,lazy_ntfs,
      548,Start Menu LNK Files,LNKFiles,Users\*\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\*.LNK,lazy_ntfs,
      549,LNK Files from Recent (XP),LNKFiles,Documents and Settings\*\Recent\**10,lazy_ntfs,
      550,Desktop LNK Files XP,LNKFiles,Documents and Settings\*\Desktop\*.LNK,lazy_ntfs,
      551,Desktop LNK Files,LNKFiles,Users\*\Desktop\*.LNK,lazy_ntfs,
      552,Restore point LNK Files XP,LNKFiles,System Volume Information\_restore*\RP*\*.LNK,lazy_ntfs,
      553,LNK Files from C:\ProgramData,LNKFiles,ProgramData\Microsoft\Windows\Start Menu\Programs\*.LNK,lazy_ntfs,
      554,.bash_history,Windows Linux Profile,Users\*\AppData\Local\Packages\*\LocalState\rootfs\home\*\.bash_history,lazy_ntfs,
      555,.bash_logout,Windows Linux Profile,Users\*\AppData\Local\Packages\*\LocalState\rootfs\home\*\.bash_logout,lazy_ntfs,
      556,.bashrc,Windows Linux Profile,Users\*\AppData\Local\Packages\*\LocalState\rootfs\home\*\.bashrc,lazy_ntfs,
      557,.profile,Windows Linux Profile,Users\*\AppData\Local\Packages\*\LocalState\rootfs\home\*\.profile,lazy_ntfs,
      558,LogFiles,Logs,Windows\System32\LogFiles\**10,lazy_ntfs,
      559,LogFiles,Logs,Windows.old\Windows\System32\LogFiles\**10,lazy_ntfs,
      560,MOF files,WMI,**10\*.MOF,lazy_ntfs,
      561,hiberfil.sys,Memory,hiberfil.sys,lazy_ntfs,
      562,pagefile.sys,Memory,pagefile.sys,lazy_ntfs,
      563,swapfile.sys,Memory,swapfile.sys,lazy_ntfs,
      564,Small Memory Dump directory,Memory,Windows\Minidump\*.dmp,lazy_ntfs,https://docs.microsoft.com/en-us/windows-hardware/drivers/debugger/small-memory-dump
      565,Small Memory Dump directory,Memory,Windows.old\Windows\Minidump\*.dmp,lazy_ntfs,https://docs.microsoft.com/en-us/windows-hardware/drivers/debugger/small-memory-dump
      566,Microsoft Office Backstage,FileKnowledge,Users\*\AppData\Local\Microsoft\Office\*\BackstageinAppNavCache\**10,lazy_ntfs,
      567,.NET CLR UsageLogs,.NET CLR UsageLogs,Users\*\AppData\Local\Microsoft\CLR_*\UsageLogs\**10,lazy_ntfs,
      568,Word Autosave Location,FileKnowledge,Users\*\AppData\Roaming\Microsoft\Word\**10,lazy_ntfs,
      569,Excel Autosave Location,ApplicationCompatibility,Users\*\AppData\Roaming\Microsoft\Excel\**10,lazy_ntfs,
      570,Powerpoint Autosave Location,FileKnowledge,Users\*\AppData\Roaming\Microsoft\Powerpoint\**10,lazy_ntfs,
      571,Publisher Autosave Location,FileKnowledge,Users\*\AppData\Roaming\Microsoft\Publisher\**10,lazy_ntfs,
      572,Office Diagnostics,Execution,Users\*\AppData\Local\Diagnostics\PCW.debugreport.xml,lazy_ntfs,Payloads for CVE-2022-30190 ('Follina') will be in this log
      573,Office Elevated Diagnostics,Execution,Users\*\AppData\Local\ElevatedDiagnostics\PCW.debugreport.xml,lazy_ntfs,Payloads for CVE-2022-30190 ('Follina') will be in this log
      574,Office Document Cache,FileKnowledge,Users\*\AppData\Local\Microsoft\Office\*\OfficeFileCache\**10,lazy_ntfs,
      575,Prefetch,Prefetch,Windows\prefetch\*.pf,lazy_ntfs,
      576,Prefetch,Prefetch,Windows.old\Windows\prefetch\*.pf,lazy_ntfs,
      577,RDP Cache Files,FileSystem,Users\*\AppData\Local\Microsoft\Terminal Server Client\Cache\*,lazy_ntfs,
      578,Windows.old RDP Cache Files,FileSystem,Windows.old\Users\*\AppData\Local\Microsoft\Terminal Server Client\Cache\*,lazy_ntfs,
      579,RDP Cache Files,FileSystem,Documents and Settings\*\Local Settings\Application Data\Microsoft\Terminal Server Client\Cache\*,lazy_ntfs,
      580,RemoteConnectionManager Event Logs,EventLogs,Windows\System32\winevt\logs\Microsoft-Windows-TerminalServices-RemoteConnectionManager*,lazy_ntfs,
      581,RemoteConnectionManager Event Logs,EventLogs,Windows.old\Windows\System32\winevt\logs\Microsoft-Windows-TerminalServices-RemoteConnectionManager*,lazy_ntfs,
      582,LocalSessionManager Event Logs,EventLogs,Windows\System32\winevt\logs\Microsoft-Windows-TerminalServices-LocalSessionManager*,lazy_ntfs,
      583,LocalSessionManager Event Logs,EventLogs,Windows.old\Windows\System32\winevt\logs\Microsoft-Windows-TerminalServices-LocalSessionManager*,lazy_ntfs,
      584,RDPClient Event Logs,EventLogs,Windows\System32\winevt\logs\Microsoft-Windows-TerminalServices-RDPClient*,lazy_ntfs,
      585,RDPClient Event Logs,EventLogs,Windows.old\Windows\System32\winevt\logs\Microsoft-Windows-TerminalServices-RDPClient*,lazy_ntfs,
      586,RDPCoreTS Event Logs,EventLogs,Windows\System32\winevt\logs\Microsoft-Windows-RemoteDesktopServices-RdpCoreTS*,lazy_ntfs,Can be used to correlate RDP logon failures by originating IP
      587,RDPCoreTS Event Logs,EventLogs,Windows.old\Windows\System32\winevt\logs\Microsoft-Windows-RemoteDesktopServices-RdpCoreTS*,lazy_ntfs,Can be used to correlate RDP logon failures by originating IP
      588,RecentFileCache,ApplicationCompatability,Windows\AppCompat\Programs\RecentFileCache.bcf,lazy_ntfs,
      589,RecentFileCache,ApplicationCompatability,Windows.old\Windows\AppCompat\Programs\RecentFileCache.bcf,lazy_ntfs,
      590,Recycle Bin - Windows Vista+,FileDeletion,$Recycle.Bin\**10\$R*,lazy_ntfs,
      591,Recycle Bin - Windows Vista+,FileDeletion,$Recycle.Bin\*\$R*\**10,lazy_ntfs,
      592,RECYCLER - WinXP,FileDeletion,RECYCLE*\**10\D*,lazy_ntfs,
      593,Recycle Bin - Windows Vista+,FileDeletion,$Recycle.Bin\**10\$I*,lazy_ntfs,
      594,RECYCLER - WinXP,FileDeletion,RECYCLE*\**10\INFO2,lazy_ntfs,
      595,BBI registry hive,Registry,Windows\System32\config\BBI,lazy_ntfs,
      596,BBI registry hive,Registry,Windows.old\Windows\System32\config\BBI,lazy_ntfs,
      597,BBI registry transaction files,Registry,Windows\System32\config\BBI.LOG*,lazy_ntfs,
      598,BBI registry transaction files,Registry,Windows.old\System32\config\BBI.LOG*,lazy_ntfs,
      599,BCD-Template registry hive,Registry,Windows\System32\config\BCD-Template,lazy_ntfs,
      600,BCD-Template registry hive,Registry,Windows.old\Windows\System32\config\BCD-Template,lazy_ntfs,
      601,BCD-Template registry transaction files,Registry,Windows\System32\config\BCD-Template.LOG*,lazy_ntfs,
      602,BCD-Template registry transaction files,Registry,Windows.old\System32\config\BCD-Template.LOG*,lazy_ntfs,
      603,COMPONENTS registry hive,Registry,Windows\System32\config\COMPONENTS,lazy_ntfs,
      604,COMPONENTS registry hive,Registry,Windows.old\Windows\System32\config\COMPONENTS,lazy_ntfs,
      605,COMPONENTS registry transaction files,Registry,Windows\System32\config\COMPONENTS.LOG*,lazy_ntfs,
      606,COMPONENTS registry transaction files,Registry,Windows.old\System32\config\COMPONENTS.LOG*,lazy_ntfs,
      607,DRIVERS registry hive,Registry,Windows\System32\config\DRIVERS,lazy_ntfs,
      608,DRIVERS registry hive,Registry,Windows.old\Windows\System32\config\DRIVERS,lazy_ntfs,
      609,DRIVERS registry transaction files,Registry,Windows\System32\config\DRIVERS.LOG*,lazy_ntfs,
      610,DRIVERS registry transaction files,Registry,Windows.old\System32\config\DRIVERS.LOG*,lazy_ntfs,
      611,ELAM registry hive,Registry,Windows\System32\config\ELAM,lazy_ntfs,
      612,ELAM registry hive,Registry,Windows.old\Windows\System32\config\ELAM,lazy_ntfs,
      613,ELAM registry transaction files,Registry,Windows\System32\config\ELAM.LOG*,lazy_ntfs,
      614,ELAM registry transaction files,Registry,Windows.old\System32\config\ELAM.LOG*,lazy_ntfs,
      615,userdiff registry hive,Registry,Windows\System32\config\userdiff,lazy_ntfs,
      616,userdiff registry hive,Registry,Windows.old\Windows\System32\config\userdiff,lazy_ntfs,
      617,userdiff registry transaction files,Registry,Windows\System32\config\userdiff.LOG*,lazy_ntfs,
      618,userdiff registry transaction files,Registry,Windows.old\System32\config\userdiff.LOG*,lazy_ntfs,
      619,VSMIDK registry hive,Registry,Windows\System32\config\VSMIDK,lazy_ntfs,
      620,VSMIDK registry hive,Registry,Windows.old\Windows\System32\config\VSMIDK,lazy_ntfs,
      621,VSMIDK registry transaction files,Registry,Windows\System32\config\VSMIDK.LOG*,lazy_ntfs,
      622,VSMIDK registry transaction files,Registry,Windows.old\System32\config\VSMIDK.LOG*,lazy_ntfs,
      623,SAM registry transaction files,Registry,Windows\System32\config\SAM.LOG*,lazy_ntfs,
      624,SAM registry transaction files,Registry,Windows.old\Windows\System32\config\SAM.LOG*,lazy_ntfs,
      625,SECURITY registry transaction files,Registry,Windows\System32\config\SECURITY.LOG*,lazy_ntfs,
      626,SECURITY registry transaction files,Registry,Windows.old\Windows\System32\config\SECURITY.LOG*,lazy_ntfs,
      627,SOFTWARE registry transaction files,Registry,Windows\System32\config\SOFTWARE.LOG*,lazy_ntfs,
      628,SOFTWARE registry transaction files,Registry,Windows.old\Windows\System32\config\SOFTWARE.LOG*,lazy_ntfs,
      629,SYSTEM registry transaction files,Registry,Windows\System32\config\SYSTEM.LOG*,lazy_ntfs,
      630,SYSTEM registry transaction files,Registry,Windows.old\Windows\System32\config\SYSTEM.LOG*,lazy_ntfs,
      631,SAM registry hive,Registry,Windows\System32\config\SAM,lazy_ntfs,
      632,SAM registry hive,Registry,Windows.old\Windows\System32\config\SAM,lazy_ntfs,
      633,SECURITY registry hive,Registry,Windows\System32\config\SECURITY,lazy_ntfs,
      634,SECURITY registry hive,Registry,Windows.old\Windows\System32\config\SECURITY,lazy_ntfs,
      635,SOFTWARE registry hive,Registry,Windows\System32\config\SOFTWARE,lazy_ntfs,
      636,SOFTWARE registry hive,Registry,Windows.old\Windows\System32\config\SOFTWARE,lazy_ntfs,
      637,SYSTEM registry hive,Registry,Windows\System32\config\SYSTEM,lazy_ntfs,
      638,SYSTEM registry hive,Registry,Windows.old\Windows\System32\config\SYSTEM,lazy_ntfs,
      639,RegBack registry transaction files,Registry,Windows\System32\config\RegBack\*.LOG*,lazy_ntfs,
      640,RegBack registry transaction files,Registry,Windows.old\Windows\System32\config\RegBack\*.LOG*,lazy_ntfs,
      641,SAM registry hive (RegBack),Registry,Windows\System32\config\RegBack\SAM,lazy_ntfs,
      642,SAM registry hive (RegBack),Registry,Windows.old\Windows\System32\config\RegBack\SAM,lazy_ntfs,
      643,SECURITY registry hive (RegBack),Registry,Windows\System32\config\RegBack\SECURITY,lazy_ntfs,
      644,SECURITY registry hive (RegBack),Registry,Windows.old\Windows\System32\config\RegBack\SECURITY,lazy_ntfs,
      645,SOFTWARE registry hive (RegBack),Registry,Windows\System32\config\RegBack\SOFTWARE,lazy_ntfs,
      646,SOFTWARE registry hive (RegBack),Registry,Windows.old\Windows\System32\config\RegBack\SOFTWARE,lazy_ntfs,
      647,SYSTEM registry hive (RegBack),Registry,Windows\System32\config\RegBack\SYSTEM,lazy_ntfs,
      648,SYSTEM registry hive (RegBack),Registry,Windows.old\Windows\System32\config\RegBack\SYSTEM,lazy_ntfs,
      649,SYSTEM registry hive (RegBack),Registry,Windows\System32\config\RegBack\SYSTEM1,lazy_ntfs,
      650,SYSTEM registry hive (RegBack),Registry,Windows.old\Windows\System32\config\RegBack\SYSTEM1,lazy_ntfs,
      651,System Profile registry hive,Registry,Windows\System32\config\systemprofile\NTUSER.DAT,lazy_ntfs,
      652,System Profile registry hive,Registry,Windows.old\Windows\System32\config\systemprofile\NTUSER.DAT,lazy_ntfs,
      653,System Profile registry transaction files,Registry,Windows\System32\config\systemprofile\NTUSER.DAT.LOG*,lazy_ntfs,
      654,System Profile registry transaction files,Registry,Windows.old\Windows\System32\config\systemprofile\NTUSER.DAT.LOG*,lazy_ntfs,
      655,Local Service registry hive,Registry,Windows\ServiceProfiles\LocalService\NTUSER.DAT,lazy_ntfs,
      656,Local Service registry hive,Registry,Windows.old\Windows\ServiceProfiles\LocalService\NTUSER.DAT,lazy_ntfs,
      657,Local Service registry transaction files,Registry,Windows\ServiceProfiles\LocalService\NTUSER.DAT.LOG*,lazy_ntfs,
      658,Local Service registry transaction files,Registry,Windows.old\Windows\ServiceProfiles\LocalService\NTUSER.DAT.LOG*,lazy_ntfs,
      659,Network Service registry hive,Registry,Windows\ServiceProfiles\NetworkService\NTUSER.DAT,lazy_ntfs,
      660,Network Service registry hive,Registry,Windows.old\Windows\ServiceProfiles\NetworkService\NTUSER.DAT,lazy_ntfs,
      661,Network Service registry transaction files,Registry,Windows\ServiceProfiles\NetworkService\NTUSER.DAT.LOG*,lazy_ntfs,
      662,Network Service registry transaction files,Registry,Windows.old\Windows\ServiceProfiles\NetworkService\NTUSER.DAT.LOG*,lazy_ntfs,
      663,System Restore Points Registry Hives (XP),Registry,System Volume Information\_restore*\RP*\snapshot\_REGISTRY_*,lazy_ntfs,
      664,NTUSER.DAT registry hive XP,Registry,Documents and Settings\*\NTUSER.DAT,lazy_ntfs,
      665,NTUSER.DAT registry hive,Registry,Users\*\NTUSER.DAT,lazy_ntfs,
      666,NTUSER.DAT registry transaction files,Registry,Users\*\NTUSER.DAT.LOG*,lazy_ntfs,
      667,NTUSER.DAT DEFAULT registry hive,Registry,Windows\System32\config\DEFAULT,lazy_ntfs,
      668,NTUSER.DAT DEFAULT registry hive,Registry,Windows.old\Windows\System32\config\DEFAULT,lazy_ntfs,
      669,NTUSER.DAT DEFAULT transaction files,Registry,Windows\System32\config\DEFAULT.LOG*,lazy_ntfs,
      670,NTUSER.DAT DEFAULT transaction files,Registry,Windows.old\Windows\System32\config\DEFAULT.LOG*,lazy_ntfs,
      671,UsrClass.dat registry hive,Registry,Users\*\AppData\Local\Microsoft\Windows\UsrClass.dat,lazy_ntfs,
      672,UsrClass.dat registry transaction files,Registry,Users\*\AppData\Local\Microsoft\Windows\UsrClass.dat.LOG*,lazy_ntfs,
      673,NTUSER.DAT registry hive,Registry,**10\NTUSER.DAT,lazy_ntfs,
      674,NTUSER.DAT registry transaction files,Registry,**10\NTUSER.DAT.LOG*,lazy_ntfs,
      675,NTUSER.DAT DEFAULT registry hive,Registry,**10\DEFAULT,lazy_ntfs,
      676,NTUSER.DAT DEFAULT transaction files,Registry,**10\DEFAULT.LOG*,lazy_ntfs,
      677,UsrClass.dat registry hive,Registry,**10\UsrClass.dat,lazy_ntfs,
      678,UsrClass.dat registry transaction files,Registry,**10\UsrClass.dat.LOG*,lazy_ntfs,
      679,LNK Files,LNKFiles,**10\*.LNK,lazy_ntfs,
      680,Word Autosave Location,FileKnowledge,Users\*\AppData\Roaming\Microsoft\Word\*,lazy_ntfs,
      681,Excel Autosave Location,ApplicationCompatibility,Users\*\AppData\Roaming\Microsoft\Excel\*,lazy_ntfs,
      682,PowerPoint Autosave Location,FileKnowledge,Users\*\AppData\Roaming\Microsoft\PowerPoint\*,lazy_ntfs,
      683,Publisher Autosave Location,FileKnowledge,Users\*\AppData\Roaming\Microsoft\Publisher\*,lazy_ntfs,
      684,Publisher Autosave Location,FileKnowledge,Users\*\AppData\Roaming\Microsoft\Word\*,lazy_ntfs,
      685,Office Document Cache,FileKnowledge,Users\*\AppData\Local\Microsoft\Office\*\OfficeFileCache\*,lazy_ntfs,
      686,Office Document Cache,FileKnowledge,Users\*\AppData\Local\Microsoft\Office\*\OfficeFileCache\*,lazy_ntfs,
      687,Chrome bookmarks,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Bookmarks*,lazy_ntfs,
      688,Chrome bookmarks,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Bookmarks*,lazy_ntfs,
      689,Chrome Cookies,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\**10\Cookies*,lazy_ntfs,
      690,Chrome Cookies,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\**10\Cookies*,lazy_ntfs,
      691,Chrome Current Session,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Current Session,lazy_ntfs,
      692,Chrome Current Session,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Current Session,lazy_ntfs,
      693,Chrome Current Tabs,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Current Tabs,lazy_ntfs,
      694,Chrome Current Tabs,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Current Tabs,lazy_ntfs,
      695,Chrome Download Metadata,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Download Metadata,lazy_ntfs,
      696,Chrome Download Metadata,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Download Metadata,lazy_ntfs,
      697,Chrome Extension Cookies,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Extension Cookies,lazy_ntfs,
      698,Chrome Extension Cookies,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Extension Cookies,lazy_ntfs,
      699,Chrome Favicons,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Favicons*,lazy_ntfs,
      700,Chrome Favicons,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Favicons*,lazy_ntfs,
      701,Chrome History,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\History*,lazy_ntfs,
      702,Chrome History,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\History*,lazy_ntfs,
      703,Chrome Last Session,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Last Session,lazy_ntfs,
      704,Chrome Last Session,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Last Session,lazy_ntfs,
      705,Chrome Last Tabs,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Last Tabs,lazy_ntfs,
      706,Chrome Last Tabs,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Last Tabs,lazy_ntfs,
      707,Chrome Sessions Folder,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Sessions\*,lazy_ntfs,
      708,Chrome Sessions Folder,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Sessions\*,lazy_ntfs,
      709,Chrome Login Data,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Login Data,lazy_ntfs,
      710,Chrome Login Data,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Login Data,lazy_ntfs,
      711,Chrome Media History,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Media History*,lazy_ntfs,
      712,Chrome Media History,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Media History*,lazy_ntfs,
      713,Chrome Network Action Predictor,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Network Action Predictor,lazy_ntfs,
      714,Chrome Network Action Predictor,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Network Action Predictor,lazy_ntfs,
      715,Chrome Network Persistent State,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Network Persistent State,lazy_ntfs,
      716,Chrome Network Persistent State,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Network Persistent State,lazy_ntfs,
      717,Chrome Preferences,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Preferences,lazy_ntfs,
      718,Chrome Preferences,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Preferences,lazy_ntfs,
      719,Chrome Quota Manager,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\QuotaManager,lazy_ntfs,
      720,Chrome Quota Manager,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\QuotaManager,lazy_ntfs,
      721,Chrome Reporting and NEL,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Reporting and NEL,lazy_ntfs,
      722,Chrome Reporting and NEL,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Reporting and NEL,lazy_ntfs,
      723,Chrome Shortcuts,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Shortcuts*,lazy_ntfs,
      724,Chrome Shortcuts,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Shortcuts*,lazy_ntfs,
      725,Chrome Top Sites,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Top Sites*,lazy_ntfs,
      726,Chrome Top Sites,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Top Sites*,lazy_ntfs,
      727,Chrome Trust Tokens,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Trust Tokens*,lazy_ntfs,
      728,Chrome Trust Tokens,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Trust Tokens*,lazy_ntfs,
      729,Chrome SyncData Database,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Sync Data\SyncData.sqlite3,lazy_ntfs,
      730,Chrome SyncData Database,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Sync Data\SyncData.sqlite3,lazy_ntfs,
      731,Chrome Visited Links,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Visited Links,lazy_ntfs,
      732,Chrome Visited Links,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Visited Links,lazy_ntfs,
      733,Chrome Web Data,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Web Data*,lazy_ntfs,
      734,Chrome Web Data,Communications,Users\*\AppData\Local\Google\Chrome\User Data\*\Web Data*,lazy_ntfs,
      735,Windows Protect Folder,FileSystem,Users\*\AppData\Roaming\Microsoft\Protect\*\**10,lazy_ntfs,Required for offline decryption
      736,Windows Protect Folder,FileSystem,Users\*\AppData\Roaming\Microsoft\Protect\*\**10,lazy_ntfs,Required for offline decryption
      737,Edge folder,Communications,Users\*\AppData\Local\Packages\Microsoft.MicrosoftEdge_8wekyb3d8bbwe\**10,lazy_ntfs,
      738,Edge folder,Communications,Users\*\AppData\Local\Packages\Microsoft.MicrosoftEdge_8wekyb3d8bbwe\**10,lazy_ntfs,
      739,Amcache,ApplicationCompatibility,**10\Amcache.hve,lazy_ntfs,
      740,Amcache transaction files,ApplicationCompatibility,**10\Amcache.hve.LOG*,lazy_ntfs,
      741,LNK Files from Recent,LNKFiles,Users\*\AppData\Roaming\Microsoft\Windows\Recent\**10,lazy_ntfs,
      742,LNK Files from Recent,LNKFiles,Users\*\AppData\Roaming\Microsoft\Windows\Recent\**10,lazy_ntfs,
      743,LNK Files from Microsoft Office Recent,LNKFiles,Users\*\AppData\Roaming\Microsoft\Office\Recent\**10,lazy_ntfs,
      744,LNK Files from Microsoft Office Recent,LNKFiles,Users\*\AppData\Roaming\Microsoft\Office\Recent\**10,lazy_ntfs,
      745,Desktop LNK Files,LNKFiles,**10\*.LNK,lazy_ntfs,
      746,SDB Files,Executables,Windows\apppatch\Custom\*.sdb,lazy_ntfs,
      747,SDB Files,Executables,Windows.old\Windows\apppatch\Custom\*.sdb,lazy_ntfs,
      748,SDB Files x64,Executables,Windows\apppatch\Custom\Custom64\*.sdb,lazy_ntfs,
      749,SDB Files x64,Executables,Windows.old\Windows\apppatch\Custom\Custom64\*.sdb,lazy_ntfs,
      750,SRUM,Execution,Windows\System32\SRU\**10,lazy_ntfs,
      751,SRUM,Execution,Windows.old\Windows\System32\SRU\**10,lazy_ntfs,
      752,SOFTWARE registry hive,Registry,Windows\System32\config\SOFTWARE,lazy_ntfs,
      753,SOFTWARE registry hive,Registry,Windows.old\Windows\System32\config\SOFTWARE,lazy_ntfs,
      754,SOFTWARE registry transaction files,Registry,Windows\System32\config\SOFTWARE.LOG*,lazy_ntfs,
      755,SOFTWARE registry transaction files,Registry,Windows.old\Windows\System32\config\SOFTWARE.LOG*,lazy_ntfs,
      756,SUM Database (.mdb files),Logs,Windows\System32\LogFiles\SUM\*.mdb,lazy_ntfs,"Grabs Current.mdb, SystemIdentity.mdb, and [GUID].mdb"
      757,at .job,Persistence,Windows\Tasks\*.job,lazy_ntfs,
      758,at .job,Persistence,Windows.old\Windows\Tasks\*.job,lazy_ntfs,
      759,at SchedLgU.txt,Persistence,Windows\SchedLgU.txt,lazy_ntfs,
      760,at SchedLgU.txt,Persistence,Windows.old\Windows\SchedLgU.txt,lazy_ntfs,
      761,XML,Persistence,Windows\System32\Tasks\**10,lazy_ntfs,
      762,XML,Persistence,Windows.old\Windows\System32\Tasks\**10,lazy_ntfs,
      763,SignatureCatalog,FileMetadata,Windows\System32\CatRoot\**10,lazy_ntfs,
      764,SignatureCatalog,FileMetadata,Windows.old\Windows\System32\CatRoot\**10,lazy_ntfs,
      765,Snip & Sketch,FileKnowledge,Users\*\AppData\Local\Packages\Microsoft.ScreenSketch_8wekyb3d8bbwe\TempState\*.png,lazy_ntfs,Pulls all temporary .png images generated by the Snip & Sketch screen capture tool built into Windows
      766,User startup folders,Persistence,Users\*\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Startup,lazy_ntfs,
      767,System-wide startup folder,Persistence,ProgramData\Microsoft\Windows\Start Menu\Programs\StartUp,lazy_ntfs,
      768,StartupInfo XML Files,Persistence,Windows\System32\WDI\LogFiles\StartupInfo\*.xml,lazy_ntfs,
      769,StartupInfo XML Files,Persistence,Windows.old\Windows\System32\WDI\LogFiles\StartupInfo\*.xml,lazy_ntfs,
      770,Syscache,Program Execution,System Volume Information\Syscache.hve,lazy_ntfs,
      771,Syscache transaction files,Program Execution,System Volume Information\Syscache.hve.LOG*,lazy_ntfs,
      772,Thumbcache DB,FileKnowledge,Users\*\AppData\Local\Microsoft\Windows\Explorer\thumbcache_*.db,lazy_ntfs,
      773,Setupapi.log XP,USBDevices,Windows\setupapi.log,lazy_ntfs,
      774,Setupapi.log Win7+,USBDevices,Windows\inf\setupapi.dev.log,lazy_ntfs,
      775,Setupapi.log Win7+,USBDevices,Windows.old\Windows\inf\setupapi.dev.log,lazy_ntfs,
      776,VHD,Disk Images,**10\*.VHD,lazy_ntfs,
      777,VHDX,Disk Images,**10\*.VHDX,lazy_ntfs,
      778,VDI,Disk Images,**10\*.VDI,lazy_ntfs,
      779,VMDK,Disk Images,**10\*.VMDK,lazy_ntfs,
      780,WBEM,WBEM,Windows\System32\wbem\Repository\**10,lazy_ntfs,
      781,WBEM,WBEM,Windows.old\Windows\System32\wbem\Repository\**10,lazy_ntfs,
      782,WER Files,Executables,ProgramData\Microsoft\Windows\WER\**10,lazy_ntfs,
      783,Crash Dumps,SQL Exploitation,Users\*\AppData\Local\CrashDumps\*.dmp,lazy_ntfs,
      784,Crash Dumps,SQL Exploitation,Windows\*.dmp,lazy_ntfs,
      785,Crash Dumps,SQL Exploitation,Windows.old\Windows\*.dmp,lazy_ntfs,
      786,Windows Firewall Logs,WindowsFirewallLogs,Windows\System32\LogFiles\Firewall\pfirewall.*,lazy_ntfs,
      787,Windows Firewall Logs,WindowsFirewallLogs,Windows.old\Windows\System32\LogFiles\Firewall\pfirewall.*,lazy_ntfs,
      788,Cryptokeys,Windows Hello,Windows\ServiceProfiles\LocalService\AppData\Roaming\Microsoft\Crypto\Keys\**10,lazy_ntfs,
      789,Masterkey,Windows Hello,Windows\System32\Microsoft\Protect\S-1-5-18\User\**10,lazy_ntfs,
      790,NGC,Windows Hello,Windows\ServiceProfiles\LocalService\AppData\Local\Microsoft\Ngc\**10,lazy_ntfs,
      791,SECURITY registry transaction files,Registry,Windows\System32\config\SECURITY.LOG*,lazy_ntfs,
      792,SECURITY registry transaction files,Registry,Windows.old\Windows\System32\config\SECURITY.LOG*,lazy_ntfs,
      793,SOFTWARE registry transaction files,Registry,Windows\System32\config\SOFTWARE.LOG*,lazy_ntfs,
      794,SOFTWARE registry transaction files,Registry,Windows.old\Windows\System32\config\SOFTWARE.LOG*,lazy_ntfs,
      795,SYSTEM registry transaction files,Registry,Windows\System32\config\SYSTEM.LOG*,lazy_ntfs,
      796,SYSTEM registry transaction files,Registry,Windows.old\Windows\System32\config\SYSTEM.LOG*,lazy_ntfs,
      797,SECURITY registry hive,Registry,Windows\System32\config\SECURITY,lazy_ntfs,
      798,SECURITY registry hive,Registry,Windows.old\Windows\System32\config\SECURITY,lazy_ntfs,
      799,SOFTWARE registry hive,Registry,Windows\System32\config\SOFTWARE,lazy_ntfs,
      800,SOFTWARE registry hive,Registry,Windows.old\Windows\System32\config\SOFTWARE,lazy_ntfs,
      801,SYSTEM registry hive,Registry,Windows\System32\config\SYSTEM,lazy_ntfs,
      802,SYSTEM registry hive,Registry,Windows.old\Windows\System32\config\SYSTEM,lazy_ntfs,
      803,SECURITY registry hive (RegBack),Registry,Windows\System32\config\RegBack\SECURITY,lazy_ntfs,
      804,SECURITY registry hive (RegBack),Registry,Windows.old\Windows\System32\config\RegBack\SECURITY,lazy_ntfs,
      805,SOFTWARE registry hive (RegBack),Registry,Windows\System32\config\RegBack\SOFTWARE,lazy_ntfs,
      806,SOFTWARE registry hive (RegBack),Registry,Windows.old\Windows\System32\config\RegBack\SOFTWARE,lazy_ntfs,
      807,SYSTEM registry hive (RegBack),Registry,Windows\System32\config\RegBack\SYSTEM,lazy_ntfs,
      808,SYSTEM registry hive (RegBack),Registry,Windows.old\Windows\System32\config\RegBack\SYSTEM,lazy_ntfs,
      809,SYSTEM registry hive (RegBack),Registry,Windows\System32\config\RegBack\SYSTEM1,lazy_ntfs,
      810,SYSTEM registry hive (RegBack),Registry,Windows.old\Windows\System32\config\RegBack\SYSTEM1,lazy_ntfs,
      811,WindowsIndexSearch,FileKnowledge,programdata\microsoft\search\data\applications\windows\*,lazy_ntfs,
      812,GatherLogs,FileKnowledge,programdata\microsoft\search\data\applications\windows\GatherLogs\**10,lazy_ntfs,
      813,Windows 10 Notification DB,Notifications,Users\*\AppData\Local\Microsoft\Windows\Notifications\wpndatabase.db,lazy_ntfs,
      814,Windows 10 Notification DB,Notifications,Users\*\AppData\Local\Microsoft\Windows\Notifications\appdb.dat,lazy_ntfs,
      815,MigLog.xml,OS Upgrade,Windows\Panther\MigLog.xml,lazy_ntfs,
      816,Setupact.log,OS Upgrade,Windows\Panther\Setupact.log,lazy_ntfs,
      817,HumanReadable.xml,OS Upgrade,Windows\Panther\*HumanReadable.xml,lazy_ntfs,
      818,FolderMoveLog.txt,OS Upgrade,Windows\Panther\Rollback\FolderMoveLog.txt,lazy_ntfs,
      819,Update Store.db,OS Upgrade,ProgramData\USOPrivate\UpdateStore\store.db,lazy_ntfs,
      820,Windows Power Diagnostics,Diagnostics,ProgramData\Microsoft\Windows\Power Efficiency Diagnostics\**10,lazy_ntfs,
      821,Legacy .rbs files relating to Windows Telemetry and Diagnostics,SystemEvents,ProgramData\Microsoft\Diagnosis\events*.rbs,lazy_ntfs,
      822,Legacy .rbs files relating to Windows Telemetry and Diagnostics,SystemEvents,Windows.old\ProgramData\Microsoft\Diagnosis\events*.rbs,lazy_ntfs,
      823,ActivitiesCache.db,FileFolderAccess,Users\*\AppData\Local\ConnectedDevicesPlatform\*\ActivitiesCache.db*,lazy_ntfs,
      824,System Volume Information,Folder capture,System Volume Information\**10,lazy_ntfs,
      825,1Password Database,Apps,Users\*\AppData\Local\1password\data\1Password10.sqlite,lazy_ntfs,"Database which holds information about 1Password installation, such as accounts, categories, settings and more"
      826,1Password Backup Databases,Apps,Users\*\AppData\Local\1password\backups\1Password10.sqlite,lazy_ntfs,Backups of 1Password Database
      827,1Password Logs,Apps,Users\*\AppData\Local\1password\logs\*.log,lazy_ntfs,Log of usage of 1Password - can be useful for identifying periods of user activity
      828,4K Video Downloader,Apps,Users\*\AppData\Local\4kdownload.com\4K Video Downloader\4K Video Downloader\*.sqlite,lazy_ntfs,Grabs database(s) that stores user download history
      829,AceText - Clipboard History,Apps,Users\*\Documents\*.atc,lazy_ntfs,Locates the Clipboard history for AceText
      830,Acronis True Image - Logs,Apps,ProgramData\Acronis\TrueImageHome\Logs\ti_demon\*,lazy_ntfs,Copies out all log files
      831,Acronis True Image - Database Files,Apps,ProgramData\Acronis\TrueImageHome\Database\archives.db*,lazy_ntfs,Copies out the Database folder which appears to have important information
      832,Acronis True Image - Scripts Folder,Apps,ProgramData\Acronis\TrueImageHome\Scripts\*,lazy_ntfs,Copies out all scripts files
      833,Ammyy Program Data,ApplicationLogs,ProgramData\Ammyy\**10,lazy_ntfs,"May not contain traditional log files, but presence of this folder may indicate historical usage"
      834,AnyDesk Logs - User Profile - *.trace,Communications,Users\*\AppData\Roaming\AnyDesk\*.trace,lazy_ntfs,Collects the trace logs for AnyDesk from a user profile
      835,AnyDesk Logs - ProgramData - *.trace,Communications,ProgramData\AnyDesk\*.trace,lazy_ntfs,Collects the trace logs for AnyDesk from ProgramData
      836,AnyDesk Logs - User Profile - *.conf,Communications,Users\*\AppData\Roaming\AnyDesk\*.conf,lazy_ntfs,Collects the conf logs for AnyDesk from a user profile
      837,AnyDesk Logs - ProgramData - *.conf,Communications,ProgramData\AnyDesk\*.conf,lazy_ntfs,Collects the conf logs for AnyDesk from ProgramData
      838,AnyDesk Videos,Communications,Users\*\Videos\AnyDesk\*.anydesk,lazy_ntfs,Collects any session recordings made by the user while using AnyDesk
      839,AnyDesk Logs - User Profile - connection_trace.txt,Communications,Users\*\AppData\Roaming\AnyDesk\connection_trace.txt,lazy_ntfs,Collects the connection trace log from user profile
      840,AnyDesk Logs - ProgramData - connection_trace.txt,Communications,ProgramData\AnyDesk\connection_trace.txt,lazy_ntfs,Collects the connection trace log from ProgramData
      841,AnyDesk Logs - System User Account,Communications,Windows\SysWOW64\config\systemprofile\AppData\Roaming\AnyDesk\*,lazy_ntfs,Collects the logs associated with the System user account
      842,AnyDesk Chat Logs - User Profile,Communications,Users\*\AppData\Roaming\AnyDesk\chat\*.txt,lazy_ntfs,Collects chat logs associated with the user profile
      843,Aspera Client Logs,FileDownload,Users\*\AppData\Local\Aspera\Aspera Connect\var\log\**10\*.log,lazy_ntfs,
      844,Aspera Server Logs,FileDownload,Users\*\.aspera\connect\var\log\**10\*.log,lazy_ntfs,
      845,AteraAgent .ini files,Software,Program Files\ATERA Networks\AteraAgent\**10\*.ini,lazy_ntfs,Collects logs for AteraAgent
      846,AteraAgent Logs,Software,Program Files\ATERA Networks\AteraAgent\**10\*.txt,lazy_ntfs,Collects logs for AteraAgent
      847,AteraAgent Logs,Software,Program Files\ATERA Networks\AteraAgent\**10\*.db,lazy_ntfs,Collects logs for AteraAgent
      848,AteraAgent Logs,Software,Program Files\ATERA Networks\AteraAgent\**10\*.config,lazy_ntfs,Collects logs for AteraAgent
      849,AteraAgent Logs,Software,Program Files\ATERA Networks\AteraAgent\**10\*.cfg,lazy_ntfs,Collects logs for AteraAgent
      850,Box Drive Application Metadata,Apps,Users\*\AppData\Local\Box\Box\**10,lazy_ntfs,
      851,Box Sync Application Metadata,Apps,Users\*\AppData\Local\Box Sync\**10,lazy_ntfs,
      852,Box Drive User Files,Apps,Users\*\Box\**10,lazy_ntfs,Caution! This target will collect Box Drive contents from the local drive AND on-demand cloud files. Ensure your scope of authority permits cloud collections before use or isolate system from network
      853,Box Sync User Files,Apps,Users\*\Box Sync\**10,lazy_ntfs,
      854,Cisco Jabber Database,Communications,Users\*\AppData\Local\Cisco\Unified Communications\Jabber\CSF\History\*.db,lazy_ntfs,The Cisco Jabber process needs to be killed before database can be copied.
      855,ClipboardMaster - Clipboard History - Text,Apps,Users\*\AppData\Roaming\Jumping Bytes\ClipboardMaster\Clipboard.clm4,lazy_ntfs,Locates the user’s clipboard history (text) for ClipboardMaster
      856,ClipboardMaster - Clipboard History - Images,Apps,Users\*\AppData\Roaming\Jumping Bytes\ClipboardMaster\pics\**10,lazy_ntfs,Locates the user’s clipboard history (images) for ClipboardMaster
      857,ClipboardMaster - Clipboard History - Backups,Apps,Users\*\AppData\Roaming\Jumping Bytes\ClipboardMaster\Clipboard.clm4.ba*,lazy_ntfs,Locates the user’s clipboard history (backups) for ClipboardMaster
      858,Confluence Wiki Log Files,Logs,Atlassian\Application Data\Confluence\logs\*.log*,lazy_ntfs,
      859,Confluence Wiki Log Files,Logs,Program Files\Atlassian\Confluence\logs\*.log,lazy_ntfs,
      860,DWAgent Log Files,Logs,ProgramData\DWAgent*\*.log*,lazy_ntfs,
      861,Directory Opus,Apps,Users\*\AppData\Local\GPSoftware\Directory Opus\State Data\MRU\rename_folders.osd,lazy_ntfs,Locates .osd file which contains names of folders that have been renamed manually by the user.
      862,Directory Opus,Apps,Users\*\AppData\Local\GPSoftware\Directory Opus\State Data\MRU\rename_files.osd,lazy_ntfs,Locates .osd file which contains names of files that have been renamed manually by the user.
      863,Directory Opus,Apps,Users\*\AppData\Local\GPSoftware\Directory Opus\State Data\MRU\find_contains.osd,lazy_ntfs,Locates .osd file which contains search queries initiated by the user during a search for files with contents related to the search query.
      864,Directory Opus,Apps,Users\*\AppData\Local\GPSoftware\Directory Opus\State Data\MRU\find_name.osd,lazy_ntfs,Locates .osd file which contains search queries initiated by the user during a search for files with a filename related to the search query.
      865,Directory Opus,Apps,Users\*\AppData\Local\GPSoftware\Directory Opus\State Data\MRU\find_path.osd,lazy_ntfs,Locates .osd file which contains file paths related to user activity - not exactly sure how these are generated at this time.
      866,Directory Opus,Apps,Users\*\AppData\Local\GPSoftware\Directory Opus\State Data\recent.osd,lazy_ntfs,Locates .osd file which contains file paths related to recent user activity. Effectively the DOpus Shellbags-equivalent. Appears to be for last 10 folder visited within the Lister.
      867,Directory Opus,Apps,Users\*\AppData\Local\GPSoftware\Directory Opus\State Data\backupconfig.osd,lazy_ntfs,Locates .osd file which contains file paths related to the location of the backup settings files for Directory Opus.
      868,Directory Opus,Apps,Users\*\AppData\Local\GPSoftware\Directory Opus\Thumbnail Cache\*,lazy_ntfs,Locates .osd file which contains file paths related to the location of the backup settings files for Directory Opus.
      869,Directory Opus,Apps,Users\*\AppData\Roaming\GPSoftware\Directory Opus\Logs\*,lazy_ntfs,Locates .txt files that will be named with the IP address of the FTP server Directory Opus was used to connect to. All-activity.txt will simply be a combination of all other .txt files present in this directory.
      870,Discord Cache Files,Communications,Users\*\AppData\Roaming\discord\cache\**10,lazy_ntfs,Gets cached data from Discord app
      871,Discord Local Storage LevelDB Files,Communications,Users\*\AppData\Roaming\discord\local storage\leveldb\**10,lazy_ntfs,Gets LevelDB database from Discord app
      872,Double Commander - history.xml,Apps,Users\*\AppData\Roaming\doublecmd\history.xml,lazy_ntfs,Locates an .xml file that contains Shellbags-equivalent artifacts that are sorted in temporal order from bottom to top.
      873,Double Commander - doublecmd.xml,Apps,Users\*\AppData\Roaming\doublecmd\doublecmd.xml,lazy_ntfs,Locates an .xml file that contains Shellbags-equivalent artifacts that are sorted in temporal order from top to bottom.
      874,Double Commander - FTP Log,Apps,Users\*\AppData\Roaming\doublecmd\doublecmd*.log,lazy_ntfs,Locates log files that'll be named with the following naming convention: doublecmd_2021-04-03.log.
      875,Double Commander - multiarc.ini,Apps,Users\*\AppData\Roaming\doublecmd\multiarc.ini,lazy_ntfs,
      876,Double Commander - session.ini,Apps,Users\*\AppData\Roaming\doublecmd\session.ini,lazy_ntfs,
      877,Double Commander - pixmaps.txt,Apps,Users\*\AppData\Roaming\doublecmd\pixmaps.txt,lazy_ntfs,
      878,Double Commander - shortcuts.scf,Apps,Users\*\AppData\Roaming\doublecmd\shortcuts.scf,lazy_ntfs,
      879,Dropbox Metadata,Apps,Users\*\AppData\Local\Dropbox\info.json,lazy_ntfs,Getting individual files because folder may contain very large extraneous files. Info.json contains user's Dropbox folder location
      880,Dropbox Metadata,Apps,Users\*\AppData\Local\Dropbox\host.db,lazy_ntfs,SQLite database which contains the local path of the user's Dropbox folder encoded in BASE64.
      881,Dropbox Metadata,Apps,Users\*\AppData\Local\Dropbox\machine_storage\tray-thumbnails.db,lazy_ntfs,SQLite database containing references to image files at one time present in a user’s Dropbox instance.
      882,Dropbox Metadata,Apps,Users\*\AppData\Local\Dropbox\host.dbx,lazy_ntfs,"SQLite database which contains the local path of the user's Dropbox folder encoded in BASE64. Decode each line separately, not together."
      883,Windows Protect Folder,FileSystem,Users\*\AppData\Roaming\Microsoft\Protect\*\**10,lazy_ntfs,Required for offline decryption of Dropbox databases
      884,Dropbox Metadata,Apps,Users\*\AppData\Local\Dropbox\instance*\**10,lazy_ntfs,instance folder holds multiple SQLite databases related to Dropbox activity and contents
      885,Dropbox User Files,Apps,Users\*\Dropbox*\**10,lazy_ntfs,"Default storage location for Dropbox Personal and Business (when using wildcard), but can be user-defined. Check info.json file in user Dropbox metadata files to identify default folder."
      886,EF Commander - .ini File,Apps,Users\*\AppData\Roaming\EFSoftware\*,lazy_ntfs,Locates folder where all configuration files reside
      887,Evernote Accounts,App,Users\*\AppData\Local\Evernote\Evernote\Databases\**10\.accounts,lazy_ntfs,Holds username and email of accounts
      888,Evernote Notebooks,App,Users\*\AppData\Local\Evernote\Evernote\Databases\**10\*.exb,lazy_ntfs,SQLite Database of the notes
      889,Evernote Notebook Snippets,App,Users\*\AppData\Local\Evernote\Evernote\Databases\**10\*.exb.snippets,lazy_ntfs,Note 'Snippets'
      890,Everything (VoidTools),FileSystem,Users\*\AppData\Local\Everything\Everything.db,lazy_ntfs,Copies out Everything.db
      891,Everything (VoidTools) - Run History,FileSystem,Users\*\AppData\Roaming\Everything\Run History.csv,lazy_ntfs,Copies out a CSV containing the history of items ran from Everything's search results window
      892,Everything (VoidTools) - Search History,FileSystem,Users\*\AppData\Roaming\Everything\Search History.csv,lazy_ntfs,Copies out a CSV containing the history of items searched for within Everything with timestamps
      893,Everything (VoidTools) - .ini file,FileSystem,Users\*\AppData\Roaming\Everything\Everything.ini,lazy_ntfs,Copies out the .ini file for Everything
      894,Exchange TransportRoles log files,Logs,Program Files\Microsoft\Exchange Server\*\TransportRoles\Logs\**10\*.log,lazy_ntfs,Highly dependent on Exchange configuration
      895,Fences - Desktop Screenshots,Apps,Users\*\AppData\Roaming\Stardock\Fences\Backups,lazy_ntfs,Locates all screenshots taken automatically by the Fences application
      896,FileZilla XML Log Files,Logs,Users\*\AppData\Roaming\FileZilla\*.xml*,lazy_ntfs,
      897,FileZilla SQLite3 Log Files,Logs,Users\*\AppData\Roaming\FileZilla\*.sqlite3*,lazy_ntfs,
      898,FileZilla Server XML Log Files,Logs,Users\*\AppData\Roaming\FileZilla Server\*.xml*,lazy_ntfs,
      899,FileZilla Log Files,Logs,Program Files (x86)\FileZilla Server\Logs\*.log*,lazy_ntfs,
      900,Free Commander - FreeCommander.ini,Apps,Users\*\AppData\Local\FreeCommanderXE\Settings\FreeCommander.ini,lazy_ntfs,Locates an .ini file that contains Shellbags-equivalent artifacts.
      901,Free Commander - FreeCommander.ftp.ini,Apps,Users\*\AppData\Local\FreeCommanderXE\Settings\FreeCommander.ftp.ini,lazy_ntfs,Locates an .ini file that contains the file path to the FTP log for Free Commander.
      902,Free Commander - FreeCommander.hist.ini,Apps,Users\*\AppData\Local\FreeCommanderXE\Settings\FreeCommander.hist.ini,lazy_ntfs,Locates an .ini file that contains Shellbags-equivalent artifacts that are sorted in temporal order from top to bottom for both left and right directory browsers.
      903,Free Commander - FreeCommander.fav.xml,Apps,Users\*\AppData\Local\FreeCommanderXE\Settings\FreeCommander.fav.xml,lazy_ntfs,Locates an .xml file that contains favorited files/folder by the user.
      904,Free Commander - Backup Settings,Apps,Users\*\AppData\Local\FreeCommanderXE\Settings\Bkp_Settings*\**10,lazy_ntfs,"Locates an exact copy of the above files which will have a timestamped folder name, i.e. Bkp_Settings-YYYY-MM-DD HH-MM-SS."
      905,Free Commander - FTP Log,Apps,Users\*\AppData\Local\Temp\fc*.log,lazy_ntfs,Locates log file(s) that have a default naming convention of fc_ftplog_20210403 but can be modified by the user.
      906,Free Commander - FTP Related Information,Apps,Users\*\AppData\Local\Temp\FreeCommander*\**10,lazy_ntfs,Locates a folder that may be named randomly that contains more FTP related information as well as .tmp files that are created while the user is traversing folders during an active FTP session. These files are deleted upon program exit.
      907,FDM Database,App,Users\*\AppData\Local\Free Download Manager\**10\fdm.sqlite,lazy_ntfs,"fdm.sqlite shows Torrents, downloads, folder history, auth credentials and more. Will also pull fdm.sqlite in db_backup/"
      908,FDM Backup Info,App,Users\*\AppData\Local\Free Download Manager\backup\backup.info,lazy_ntfs,"Backup info file - can change backup name from userdata.zip, so could give indication of file name"
      909,FDM Database (userdata.zip),App,Users\*\AppData\Local\Free Download Manager\backup\userdata.zip,lazy_ntfs,fdm.sqlite can also appear in the backup folder in a compressed userdata.zip file
      910,FreeFileSync,Apps,Users\*\AppData\Roaming\FreeFileSync\Logs,lazy_ntfs,Copies out all log files
      911,Google Drive Backup and Sync User Files,Apps,Users\*\Google Drive*\**10,lazy_ntfs,Older Google Drive Backup and Sync application only
      912,Google Drive Backup and Sync Metadata,Apps,Users\*\AppData\Local\Google\Drive\**10,lazy_ntfs,Older version of Google Drive
      913,Google Drive for Desktop Metadata,Apps,Users\*\AppData\Local\Google\DriveFS\**10,lazy_ntfs,Metadata folder the same for both newer Google Drive for Desktop and older Google File Stream application
      914,Google Earth My Places file,Apps,Users\*\AppData\LocalLow\Google\GoogleEarth\myplaces.kml,lazy_ntfs,File which holds favorited locations
      915,Google Earth My Places Backup file,Apps,Users\*\AppData\LocalLow\Google\GoogleEarth\myplaces.backup.kml,lazy_ntfs,Backup file which holds favorited locations
      916,Google Earth My Places file (XP),Apps,Documents and Settings\*\Application Data\Google\GoogleEarth\myplaces.kml,lazy_ntfs,File which holds favorited locations
      917,Google Earth My Places Backup file (XP),Apps,Documents and Settings\*\Application Data\Google\GoogleEarth\myplaces.backup.kml,lazy_ntfs,Backup file which holds favorited locations
      918,HeidiSQL Backup files (*.sql),Apps,Users\*\AppData\Roaming\HeidiSQL\Backups\*,lazy_ntfs,
      919,HeidiSQL (tabs.ini),Apps,Users\*\AppData\Roaming\HeidiSQL\tabs.ini,lazy_ntfs,
      920,HexChat Chat Logs,Communications,Users\*\AppData\Roaming\HexChat\logs\**10,lazy_ntfs,
      921,IceChat Chat Logs,Communications,Users\*\AppData\Local\IceChat Networks\IceChat\Logs\**10,lazy_ntfs,
      922,IrfanView Configuration File,FileKnowledge,Users\*\AppData\Roaming\IrfanView\i_view32.ini,lazy_ntfs,
      923,JDownloader 2.0 Download Lists,App,Users\*\AppData\Local\JDownloader 2.0\cfg\**10\downloadList*.zip,lazy_ntfs,"Zip folder which contains several files (00,00_00 and extraInfo) which list the download folder, the time it was created, the name of the download, origin URL, referral URL and more"
      924,JDownloader 2.0 Link Collector,App,Users\*\AppData\Local\JDownloader 2.0\cfg\**10\linkcollector*.zip,lazy_ntfs,"Zip folder which contains several files (0X,0X_00 and extraInfo) which list the websites crawled for links, the referral URLs, timestamps and more"
      925,JDownloader 2.0 General Settings,App,Users\*\AppData\Local\JDownloader 2.0\cfg\**10\org.jdownloader.settings.GeneralSettings.json,lazy_ntfs,General user config for JDownloader 2.0. Holds default download folder.
      926,JDownloader 2.0 Link Grabber Settings,App,Users\*\AppData\Local\JDownloader 2.0\cfg\**10\org.jdownloader.gui.views.linkgrabber.addlinksdialog.LinkgrabberSettings.json,lazy_ntfs,Linkgrabber Settings for JDownloader 2.0. Holds latest download destination folder.
      927,JDownloader 2.0 Proxy Settings,App,Users\*\AppData\Local\JDownloader 2.0\cfg\**10\org.jdownloader.settings.InternetConnectionSettings.customproxylist.json,lazy_ntfs,Proxy configuration for JDownloader 2.0
      928,Java WebStart Cache User Level - Default,Communication,Users\*\AppData\Local\Sun\Java\Deployment\cache\*\*\*.idx,lazy_ntfs,
      929,Java WebStart Cache User Level - IE Protected Mode,Communication,Users\*\AppData\LocalLow\Sun\Java\Deployment\cache\*\*\*.idx,lazy_ntfs,
      930,Java WebStart Cache System level,Communication,Windows\System32\config\systemprofile\AppData\Local\Sun\Java\Deployment\cache\*\*\*.idx,lazy_ntfs,
      931,Java WebStart Cache System level,Communication,Windows.old\Windows\System32\config\systemprofile\AppData\Local\Sun\Java\Deployment\cache\*\*\*.idx,lazy_ntfs,
      932,Java WebStart Cache System level - IE Protected Mode,Communication,Windows\System32\config\systemprofile\AppData\LocalLow\Sun\Java\Deployment\cache\*\*\*.idx,lazy_ntfs,
      933,Java WebStart Cache System level - IE Protected Mode,Communication,Windows.old\Windows\System32\config\systemprofile\AppData\LocalLow\Sun\Java\Deployment\cache\*\*\*.idx,lazy_ntfs,
      934,Java WebStart Cache System level (SysWow64),Communication,Windows\SysWOW64\config\systemprofile\AppData\Local\Sun\Java\Deployment\cache\*\*\*.idx,lazy_ntfs,
      935,Java WebStart Cache System level (SysWow64),Communication,Windows.old\Windows\SysWOW64\config\systemprofile\AppData\Local\Sun\Java\Deployment\cache\*\*\*.idx,lazy_ntfs,
      936,Java WebStart Cache System level (SysWow64) - IE Protected Mode,Communication,Windows\SysWOW64\config\systemprofile\AppData\LocalLow\Sun\Java\Deployment\cache\*\*\*.idx,lazy_ntfs,
      937,Java WebStart Cache System level (SysWow64) - IE Protected Mode,Communication,Windows.old\Windows\SysWOW64\config\systemprofile\AppData\LocalLow\Sun\Java\Deployment\cache\*\*\*.idx,lazy_ntfs,
      938,Java WebStart Cache User Level - XP,Communications,Documents and Settings\*\Application Data\Sun\Java\Deployment\cache\*\*\*.idx,lazy_ntfs,
      939,Kaseya Live Connect Logs (XP),ApplicationLogs,Documents and Settings\*\Application Data\Kaseya\Log\**10,lazy_ntfs,https://helpdesk.kaseya.com/hc/en-gb/articles/229009708-Live-Connect-Log-File-Locations
      940,Kaseya Live Connect Logs,ApplicationLogs,Users\*\AppData\Local\Kaseya\Log\KaseyaLiveConnect\**10,lazy_ntfs,https://helpdesk.kaseya.com/hc/en-gb/articles/229009708-Live-Connect-Log-File-Locations
      941,Kaseya Agent Endpoint Service Logs (XP),ApplicationLogs,Documents and Settings\All Users\Application Data\Kaseya\Log\Endpoint\**10,lazy_ntfs,https://helpdesk.kaseya.com/hc/en-gb/articles/229009708-Live-Connect-Log-File-Locations
      942,Kaseya Agent Endpoint Service Logs,ApplicationLogs,ProgramData\Kaseya\Log\Endpoint\**10,lazy_ntfs,https://helpdesk.kaseya.com/hc/en-gb/articles/229009708-Live-Connect-Log-File-Locations
      943,Kaseya Agent Service Log,ApplicationLogs,Program Files*\Kaseya\*\agentmon.log*,lazy_ntfs,https://helpdesk.kaseya.com/hc/en-gb/articles/229009708-Live-Connect-Log-File-Locations
      944,Kaseya Setup Log,ApplicationLogs,Users\*\AppData\Local\Temp\KASetup.log,lazy_ntfs,https://helpdesk.kaseya.com/hc/en-gb/articles/229011448
      945,Kaseya Setup Log,ApplicationLogs,Windows\Temp\KASetup.log,lazy_ntfs,https://helpdesk.kaseya.com/hc/en-gb/articles/229011448
      946,Kaseya Setup Log,ApplicationLogs,Windows.old\Windows\Temp\KASetup.log,lazy_ntfs,https://helpdesk.kaseya.com/hc/en-gb/articles/229011448
      947,Kaseya Agent Edge Service Logs,ApplicationLogs,ProgramData\Kaseya\Log\KaseyaEdgeServices\**10,lazy_ntfs,https://www.huntress.com/blog/rapid-response-kaseya-vsa-mass-msp-ransomware-incident
      948,Keepass User Config,App,Users\*\AppData\Roaming\KeePass\*.xml,lazy_ntfs,Collecting Keepass User Configuration File
      949,Keepass Config Xml,App,Program Files\KeePass Password Safe*\*.xml,lazy_ntfs,Collecting Keepass Configuration File
      950,Keepass Application Details,App,Program Files\KeePass Password Safe*\*.config,lazy_ntfs,Collecting Keepass Application Details
      951,Keepass Local Ini,App,Users\*\AppData\Local\KeePassXC\*.ini,lazy_ntfs,
      952,Keepass Roaming Ini,App,Users\*\AppData\Roaming\KeePassXC\*.ini,lazy_ntfs,
      953,LogMeIn ProgramData Logs,ApplicationLogs,ProgramData\LogMeIn\Logs\**10,lazy_ntfs,
      954,LogMeIn Application Logs,ApplicationLogs,Users\*\AppData\Local\temp\LogMeInLogs\**10,lazy_ntfs,"Contains RemoteAssist (formerly GoToAssist), GoToMeeting, and other GoTo* logs"
      955,Macrium Reflect,Apps,ProgramData\Macrium\Macrium Service\*,lazy_ntfs,Copies out all log files
      956,Macrium Reflect,Apps,ProgramData\Macrium\Reflect\*,lazy_ntfs,Copies out the Reflect folder which contains many important logs
      957,Macrium Reflect,Apps,ProgramData\Macrium\Reflect Launcher,lazy_ntfs,Copies out the Reflect folder which contains many important logs
      958,Mattermost - Chat Logs,Apps,Users\*\AppData\Roaming\Mattermost\IndexedDB\**10,lazy_ntfs,Locates Mattermost logs and copies them
      959,MediaMonkey - Media SQLite Database,Apps,Users\*\AppData\Roaming\MediaMonkey\MM.DB,lazy_ntfs,Locates SQLite DB that contains a complete enumeration of the user's media collection within MediaMonkey
      960,MediaMonkey - MediaMonkey.ini,Apps,Users\*\AppData\Roaming\MediaMonkey\MediaMonkey.ini,lazy_ntfs,Locates .ini file which contains information about the user's MediaMonkey application instance
      961,Microsoft OneNote - FullTextSearchIndex,Apps,Users\*\AppData\Local\Packages\Microsoft.Office.OneNote_8wekyb3d8bbwe\LocalState\AppData\Local\OneNote\*\FullTextSearchIndex,lazy_ntfs,Grabs database(s) comprising of each OneNote notebook's text content
      962,Microsoft OneNote - RecentNotebooks_SeenURLs,Apps,Users\*\AppData\Local\Packages\Microsoft.Office.OneNote_8wekyb3d8bbwe\LocalState\AppData\Local\OneNote\Notifications\RecentNotebooks_SeenURLs,lazy_ntfs,Grabs a file that appears to record recently seen OneNote notebooks
      963,Microsoft OneNote - AccessibilityCheckerIndex,Apps,Users\*\AppData\Local\Packages\Microsoft.Office.OneNote_8wekyb3d8bbwe\LocalState\AppData\Local\OneNote\16.0\AccessibilityCheckerIndex,lazy_ntfs,Grabs database(s) comprising of each OneNote notebook's version sync error history
      964,Microsoft OneNote - User NoteTags,Apps,Users\*\AppData\Local\Packages\Microsoft.Office.OneNote_8wekyb3d8bbwe\LocalState\AppData\Local\OneNote\16.0\NoteTags\*LiveId.db,lazy_ntfs,Grabs a database that stores the user specified tags within OneNote to be used application-wide
      965,Microsoft OneNote - RecentSearches,Apps,Users\*\AppData\Local\Packages\Microsoft.Office.OneNote_8wekyb3d8bbwe\LocalState\AppData\Local\OneNote\16.0\RecentSearches\RecentSearches.db,lazy_ntfs,Grabs a database that stores the user's recent searches within OneNote
      966,"Microsoft Sticky Notes - Windows 7, 8, and 10 version 1511 and earlier",Apps,Users\*\AppData\Roaming\Microsoft\StickyNotes\StickyNotes.snt,lazy_ntfs,
      967,Microsoft Sticky Notes - 1607 and later,Apps,Users\*\AppData\Local\Packages\Microsoft.MicrosoftStickyNotes*\LocalState\plum.sqlite*,lazy_ntfs,
      968,Microsoft Teams IndexedDB Cache,Apps,Users\*\AppData\Roaming\Microsoft\Teams\IndexedDB\https_teams.microsoft.com_0.indexeddb.leveldb\**10,lazy_ntfs,"LevelDB database which can contain inbound/outbound chat messages, call history and more"
      969,Microsoft Teams Local Storage Cache,Apps,Users\*\AppData\Roaming\Microsoft\Teams\Local Storage\leveldb\**10,lazy_ntfs,"LevelDB database which can contain meeting history, file transfer logs and more"
      970,Microsoft Teams Cache,Apps,Users\*\AppData\Roaming\Microsoft\Teams\Cache\**10,lazy_ntfs,Chromium cache which can be viewed with Nirsoft's ChromeCacheView
      971,Microsoft Teams Config,Apps,Users\*\AppData\Roaming\Microsoft\Teams\desktop-config.json,lazy_ntfs,JSON config file for Teams
      972,Microsoft Teams Logs (Windows 11),Apps,Users\%User%\AppData\Local\Packages\MicrosoftTeams_8wekyb3d8bbwe\LocalCache\Microsoft\MSTeams\Logs,lazy_ntfs,Lots of log files for MS Teams
      973,Microsoft To Do - SQLite Database of To Do tasks,Apps,Users\*\AppData\Local\Packages\Microsoft.Todos_8wekyb3d8bbwe\LocalState\AccountsRoot\*\todosqlite.db*,lazy_ntfs,
      974,Microsoft To Do - User Avatar,Apps,Users\*\AppData\Local\Packages\Microsoft.Todos_8wekyb3d8bbwe\LocalState\AccountsRoot\4c444a17ebb042fb92df97d00d1c802a\avatars\UserAvatar.jpg,lazy_ntfs,
      975,Midnight Commander -- All Configuation Files,Apps,Users\*\Midnight Commander\*,lazy_ntfs,Locates folder where all configuration files reside
      976,Multi Commander - Application Folder,Apps,Users\*\AppData\Local\MultiCommander*\**10,lazy_ntfs,Locates the contents of the Application folder.
      977,Multi Commander - Config Folder,Apps,Users\*\AppData\Roaming\MultiCommander*\Config\**10,lazy_ntfs,Locates the contents of the Config folder.
      978,Multi Commander - Log Folder,Apps,Users\*\AppData\Roaming\MultiCommander*\Logs\**10,lazy_ntfs,Locates log file(s) related to user activity within Multi Commander.
      979,Multi Commander - UserData Folder,Apps,Users\*\AppData\Roaming\MultiCommander*\UserData\**10,lazy_ntfs,Locates the contents of the UserData folder.
      980,Multi Commander - Log File,Apps,Users\*\AppData\Roaming\MultiCommander*\**10\*MultiCommander.log,lazy_ntfs,Locates log file(s) associated with Milti Commander. Commonly in YYYY-MM-DD (numbers)-MultiCommander.log naming convention.
      981,Nessus Logs,Nessus,ProgramData\Tenable\Nessus\conf\**10,lazy_ntfs,
      982,Nessus Logs,Nessus Logs,ProgramData\Tenable\Nessus\nessus\logs\**10,lazy_ntfs,
      983,Notepad++ Unsaved Edits,Text Editor,Users\*\AppData\Roaming\Notepad++\backup\**10,lazy_ntfs,Locates non-saved Notepad++ files and copies them.
      984,Notepad++ Config,Text Editor,Users\*\AppData\Roaming\Notepad++\config.xml,lazy_ntfs,"Retrieves config.xml which contains recently searched terms, replaced terms and recently opened documents"
      985,Notepad++ Session,Text Editor,Users\*\AppData\Roaming\Notepad++\session.xml,lazy_ntfs,Retrieves session.xml which contains session date
      986,One Commander - All Configuration Files,Apps,Users\*\OneCommander\*,lazy_ntfs,Locates folder where all configuration files reside
      987,One Commander - Other Configuration Files,Apps,Users\*\AppData\Local\Apps\2.0\*\*\onec*\**10,lazy_ntfs,Locates folder where all configuration files reside
      988,OneDrive Metadata Logs,Apps,Users\*\AppData\Local\Microsoft\OneDrive\logs\**10,lazy_ntfs,
      989,OneDrive Metadata Settings,Apps,Users\*\AppData\Local\Microsoft\OneDrive\settings\**10,lazy_ntfs,
      990,OneDrive User Files,Apps,Users\*\OneDrive*\**10,lazy_ntfs,Caution -- This target will collect OneDrive contents from the local drive AND on-demand cloud files. Ensure your scope of authority permits cloud collections before use or isolate system from network.
      991,OpenSSH Config File,Apps,Users\*\.ssh\config,lazy_ntfs,"Config file can hold usernames, IP addresses and ports, key locations and configured shortcuts for servers e.g. ssh web-server"
      992,OpenSSH Known Hosts,Apps,Users\*\.ssh\known_hosts,lazy_ntfs,"Known hosts file can hold a list of connected FQDNs/IP Addresses and ports if they are non-default, as well as public key fingerprints"
      993,OpenSSH Public Keys,Apps,Users\*\.ssh\*.pub,lazy_ntfs,"Gets all public keys (*.pub). It is more difficult to find private keys as they typically do not have a file extension. However, the .pub files should be able to help find the private keys as they are typically named the same."
      994,OpenSSH Default RSA Private Key,Apps,Users\*\.ssh\id_rsa,lazy_ntfs,Default name for an auto-generated SSH RSA private key
      995,OpenSSH Default ECDSA Private Key,Apps,Users\*\.ssh\id_ecdsa,lazy_ntfs,Default name for an auto-generated SSH ECDSA private key
      996,OpenSSH Default ECDSA-SK Private Key,Apps,Users\*\.ssh\id_ecdsa_sk,lazy_ntfs,Default name for an auto-generated SSH ECDSA private key using a Security Key
      997,OpenSSH Default ED25519 Private Key,Apps,Users\*\.ssh\id_ed25519,lazy_ntfs,Default name for an auto-generated SSH ED25519 private key
      998,OpenSSH Default ED25519-SK Private Key,Apps,Users\*\.ssh\id_ed25519_sk,lazy_ntfs,Default name for an auto-generated SSH ED25519 private key using a Security Key
      999,OpenSSH Default DSA Private Key,Apps,Users\*\.ssh\id_dsa,lazy_ntfs,Default name for an auto-generated SSH DSA private key
      1000,OpenSSH Server Config File,Apps,ProgramData\ssh\sshd_config,lazy_ntfs,Config file can hold information on allowed/denied users
      1001,OpenSSH Server Logs,Apps,ProgramData\ssh\logs\*,lazy_ntfs,OpenSSH server logs
      1002,OpenSSH Host ECDSA Key,Apps,ProgramData\ssh\ssh_host_ecdsa_key,lazy_ntfs,Retrieves the host ECDSA key
      1003,OpenSSH Host ED25519 Key,Apps,ProgramData\ssh\ssh_host_ed25519_key,lazy_ntfs,Retrieves the host ED25519 key
      1004,OpenSSH Host DSA Key,Apps,ProgramData\ssh\ssh_host_dsa_key,lazy_ntfs,Retrieves the host DSA key
      1005,OpenSSH Host RSA Key,Apps,ProgramData\ssh\ssh_host_rsa_key,lazy_ntfs,Retrieves the host RSA key
      1006,OpenSSH User Authorized Keys,Apps,Users\*\.ssh\authorized_keys,lazy_ntfs,Retrieves the user's authorised public keys
      1007,OpenSSH User Authorized Keys 2,Apps,Users\*\.ssh\authorized_keys2,lazy_ntfs,Retrieves the user's authorised public keys from the second file
      1008,OpenSSH Authorized Administrator Keys,Apps,ProgramData\ssh\administrators_authorized_keys,lazy_ntfs,Retrieves the administrator group's authorised public keys
      1009,OpenVPN Client Config,ApplicationLogs,Users\*\OpenVPN\config\**10,lazy_ntfs,Contains OpenVPN Configs (Profiles)
      1010,OpenVPN Client Config,ApplicationLogs,Program Files*\OpenVPN\config\**10,lazy_ntfs,Contains OpenVPN Configs(Profiles)
      1011,OpenVPN Client Config,ApplicationLogs,Users\*\OpenVPN\log\*.log,lazy_ntfs,Contains OpenVPN Logs for each Config(Profile)
      1012,PST XP,Communications,Documents and Settings\*\Local Settings\Application Data\Microsoft\Outlook\*.pst,lazy_ntfs,
      1013,OST XP,Communications,Documents and Settings\*\Local Settings\Application Data\Microsoft\Outlook\*.ost,lazy_ntfs,
      1014,PST (2013 or 2016),Communications,Users\*\Documents\Outlook Files\*.pst,lazy_ntfs,
      1015,OST (2013 or 2016),Communications,Users\*\Documents\Outlook Files\*.ost,lazy_ntfs,
      1016,PST,Communications,Users\*\AppData\Local\Microsoft\Outlook\*.pst,lazy_ntfs,"Outlook Data File: POP accounts, archives, older installations"
      1017,OST,Communications,Users\*\AppData\Local\Microsoft\Outlook\*.ost,lazy_ntfs,"Offline Outlook Data File: M365, Exchange, IMAP"
      1018,NST,Communications,Users\*\AppData\Local\Microsoft\Outlook\*.nst,lazy_ntfs,Outlook Group Storage File: Group conversations and calendar
      1019,Outlook Attachment Temporary Storage,Communications,Users\*\AppData\Local\Microsoft\Windows\INetCache\Content.Outlook\**10,lazy_ntfs,Outlook temporary storage folder for user attachments
      1020,PeaZip Configuration Files,FileKnowledge,Users\*\AppData\Roaming\PeaZip\**10,lazy_ntfs,
      1021,ProtonVPN - Connection Logs,ApplicationLogs,Users\*\AppData\Local\ProtonVPN\Logs,lazy_ntfs,Locates ProtonVPN connection logs.
      1022,Q-Dir - .ini File,Apps,Users\*\AppData\Roaming\Q-Dir\Q-Dir.ini,lazy_ntfs,Locates .ini file associated with Q-Dir which stores useful user activity information.
      1023,Q-Dir - .qdr file,Apps,Users\*\AppData\Roaming\Q-Dir\start.qdr,lazy_ntfs,"Locates .qdr file associated with Q-Dir which stores useful user activity information, including the last 4 folders opened (encoded, unfortunately)."
      1024,QFinderPro,Apps,Users\*\AppData\Local\QNAP\QfinderPro,lazy_ntfs,Locates a JSON file that provides network location information for any QNAP connected devices.
      1025,Radmin Server 32bit Log,ApplicationLogs,Windows\SysWOW64\rserver30\Radm_log.htm,lazy_ntfs,Contains Application Log entries such as service start and incomming connections.
      1026,Radmin Server 64bit Log,ApplicationLogs,Windows\System32\rserver30\Radm_log.htm,lazy_ntfs,Contains Application Log entries such as service start and incomming connections.
      1027,Radmin Server 32bit Chats,ApplicationLogs,Windows\SysWOW64\rserver30\CHATLOGS\*\*.htm,lazy_ntfs,Previous chat logs
      1028,Radmin Server 64bit Chats,ApplicationLogs,Windows\System32\rserver30\CHATLOGS\*\*.htm,lazy_ntfs,Previous chat logs
      1029,Radmin Viewer Chats,ApplicationLogs,Users\*\Documents\ChatLogs\*\*.htm,lazy_ntfs,Previous chat logs
      1030,RemoteUtilities Connection Logs,Remote Access,Program Files*\Remote Utilities - Host\Logs\rut_log_*.html,lazy_ntfs,Includes connection log files
      1031,RemoteUtilities Install Log,Remote Access,ProgramData\Remote Utilities\install.log,lazy_ntfs,Includes Install log file
      1032,ScreenConnect Session Database,ApplicationLogs,Program Files*\ScreenConnect\App_Data\Session.db,lazy_ntfs,SQLite database with session information
      1033,ScreenConnect Session Database,ApplicationLogs,Program Files*\ScreenConnect\App_Data\User.xml,lazy_ntfs,Contains each user's last authenticated time
      1034,ScreenConnect User Config,ApplicationLogs,ProgramData\ScreenConnect Client*\user.config,lazy_ntfs,Contains server domain and IP info
      1035,ShareX,Apps,Users\*\Documents\ShareX\**10,lazy_ntfs,Locates and captures all files within the default ShareX folder path
      1036,Siemens TIA Settings,ICS,Users\*\AppData\Roaming\Siemens\Automation\Portal*\Settings\**10,lazy_ntfs,
      1037,Signal Attachments cache,Communications,Users\*\AppData\Roaming\Signal\attachments.noindex\**10,lazy_ntfs,Profile pictures (and possibly attachments) for users who this individual has as contacts or has communicated with
      1038,Signal Logs,Communications,Users\*\AppData\Roaming\Signal\logs\**10,lazy_ntfs,"Logs for Signal. Most recent has the extension .log while old ones will have extension .log.0, .log.1 etc."
      1039,Signal config.json,Communications,Users\*\AppData\Roaming\Signal\config.json,lazy_ntfs,config.json holds the db.sqlite SQLCipher raw key
      1040,Signal Database,Communications,Users\*\AppData\Roaming\Signal\sql\db.sqlite,lazy_ntfs,"Stores attachment details, conversations, messages, and more"
      1041,main.db (App <v12),Communications,Users\*\AppData\Local\Packages\Microsoft.SkypeApp_*\LocalState\*\main.db,lazy_ntfs,
      1042,skype.db (App +v12),Communications,Users\*\AppData\Local\Packages\Microsoft.SkypeApp_*\LocalState\*\skype.db,lazy_ntfs,
      1043,main.db XP,Communications,Documents and Settings\*\Application Data\Skype\*\main.db,lazy_ntfs,
      1044,main.db Win7+,Communications,Users\*\AppData\Roaming\Skype\*\main.db,lazy_ntfs,
      1045,s4l-[username].db (App +v8),Communications,Users\*\AppData\Local\Packages\Microsoft.SkypeApp_*\LocalState\s4l-*.db,lazy_ntfs,
      1046,leveldb (Skype for Desktop +v8),Communications,Users\*\AppData\Roaming\Microsoft\Skype for Desktop\IndexedDB\*.leveldb\**10,lazy_ntfs,
      1047,Skype for Destkop v8+ Chromium Cache,Communications,Users\*\AppData\Roaming\Microsoft\Skype for Desktop\Cache\**10,lazy_ntfs,Can be viewed with Nirsoft's ChromeCacheView
      1048,Slack - Chat Logs,Apps,Users\*\AppData\Roaming\Slack\IndexedDB\**10,lazy_ntfs,Locates Slack logs and copies them
      1049,Slack LevelDB Files,Apps,Users\*\AppData\Roaming\Slack\Local Storage\leveldb\**10,lazy_ntfs,
      1050,Slack Electron Logs,Apps,Users\*\AppData\Roaming\Slack\logs\**10,lazy_ntfs,Current Slack application is based on Electron and additional logging can be found here.
      1051,Slack Cache,Apps,Users\*\AppData\Roaming\Slack\Cache\**10,lazy_ntfs,Collects Slack cache files. This folder can be parsed like a Chrome Browser cache using a tool like Nirsoft ChromeCacheView
      1052,Slack Storage,Apps,Users\*\AppData\Roaming\Slack\storage\**10,lazy_ntfs,User activity logs can be present including slack-downloads log
      1053,Snagit - Captures,Apps,Users\*\AppData\Local\TechSmith\Snagit\DataStore,lazy_ntfs,Locates all Snagit captures
      1054,SpeedCommander - .ini File,Apps,Users\*\AppData\Roaming\SpeedProject\SpeedCommander 19\*,lazy_ntfs,Locates folder where all configuration files reside
      1055,Splashtop Log Files,Software,Program Files*\Splashtop\Splashtop Remote\Server\log\**10,lazy_ntfs,Collects logs for Splashtop
      1056,Splashtop Log Files in ProgramData,Software,ProgramData\Splashtop\Temp\log\**10,lazy_ntfs,Collects logs for Splashtop
      1057,SublimeText 2/3 Auto Save Session,Text Editor,Users\*\AppData\Roaming\Sublime Text*\Settings\Session.sublime_session,lazy_ntfs,Sublime Text 2/3 stores unsaved (temporary) files and its content in its Session.sublime_session file
      1058,SugarSync Log File,Apps,Users\*\AppData\Local\SugarSync\sc1.log,lazy_ntfs,Locates a log file the gives a play-by-play of what the user synced when.
      1059,SugarSync - Shared Folders (Default Location),Apps,Users\*\Documents\SugarSync Shared Folders\**10,lazy_ntfs,
      1060,SugarSync - My SugarSync (Default Location),Apps,Users\*\Documents\My SugarSync\**10,lazy_ntfs,
      1061,SumatraPDF Settings - SessionData,FileKnowledge,Users\*\AppData\Local\SumatraPDF\SumatraPDF-settings.txt,lazy_ntfs,Settings file which contains information about previous user session
      1062,SumatraPDF Cache,FileKnowledge,Users\*\AppData\Local\SumatraPDF\sumatrapdfcache,lazy_ntfs,Folder contains a PNG snapshot of each PDF file the user had open at the time of last application close
      1063,Supremo Connection Logs,Communications,ProgramData\SupremoRemoteDesktop\Log\*.log,lazy_ntfs,Includes Supremo.00.Client.log and Supremo.00.Incoming.log
      1064,Supremo File Transfer Inbox,Communications,ProgramData\SupremoRemoteDesktop\Inbox,lazy_ntfs,Includes all files transferred to the inbox folder during a remote session
      1065,Tablacus Explorer - remember.xml,Logs,Users\*\AppData\Local\Temp\*\config\**10\remember.xml,lazy_ntfs,
      1066,Tablacus Explorer - window.xml,Logs,Users\*\AppData\Local\Temp\*\config\**10\window.xml,lazy_ntfs,
      1067,Tablacus Explorer - window1.xml,Logs,Users\*\AppData\Local\Temp\*\config\**10\window1.xml,lazy_ntfs,
      1068,TeamViewer Connection Logs,Communications,Program Files*\TeamViewer\connections*.txt,lazy_ntfs,Includes connections_incoming.txt and connections.txt
      1069,TeamViewer Application Logs,ApplicationLogs,Program Files*\TeamViewer\TeamViewer*_Logfile*,lazy_ntfs,Includes TeamViewer<version>_Logfile.log and TeamViewer<version>_Logfile_OLD.log
      1070,TeamViewer Configuration Files,ApplicationLogs,Users\*\AppData\Roaming\TeamViewer\MRU\RemoteSupport\**10,lazy_ntfs,Includes miscellaneous config files
      1071,Telegram app folder,Apps,Users\*\AppData\Roaming\Telegram Desktop\**10,lazy_ntfs,Telegram app folder structure
      1072,Telegram downloaded files,Apps,Users\*\Downloads\Telegram Desktop\**10,lazy_ntfs,Chat Attachments
      1073,TeraCopy,TeraCopy,Users\*\AppData\Roaming\TeraCopy\**10,lazy_ntfs,
      1074,Mozilla Thunderbird Install Date,Apps,Users\*\AppData\Roaming\Thunderbird\Crash Reports\InstallTime*,lazy_ntfs,Holds install time in Unix Seconds timestamp
      1075,Mozilla Thunderbird Profiles.ini,Apps,Users\*\AppData\Roaming\Thunderbird\profiles.ini,lazy_ntfs,Profiles list - can hold references to other profiles held elsewhere on the device
      1076,Mozilla Thunderbird prefs.js,Apps,Users\*\AppData\Roaming\Thunderbird\Profiles\*\prefs.js,lazy_ntfs,User Preferences for that profile
      1077,Mozilla Thunderbird Global Messages Database,Apps,Users\*\AppData\Roaming\Thunderbird\Profiles\*\global-messages-db.sqlite,lazy_ntfs,"Holds list of contacts, emails, and other potentially useful artifacts"
      1078,Mozilla Thunderbird logins.json,Apps,Users\*\AppData\Roaming\Thunderbird\Profiles\*\logins.json,lazy_ntfs,"Holds last time online login used, last time password changed, hostname, HTTP(s) URL and more"
      1079,Mozilla Thunderbird places.sqlite,Apps,Users\*\AppData\Roaming\Thunderbird\Profiles\*\places.sqlite,lazy_ntfs,"Holds history for Thunderbird - as it contains portions of Firefox embedded, it can be used to visit websites too"
      1080,Mozilla Thunderbird ImapMail INBOX,Apps,Users\*\AppData\Roaming\Thunderbird\Profiles\*\ImapMail\**10\INBOX,lazy_ntfs,"Holds all email files with headers, content etc"
      1081,Mozilla Thunderbird Mail INBOX,Apps,Users\*\AppData\Roaming\Thunderbird\Profiles\*\Mail\**10\INBOX,lazy_ntfs,"Holds all email files with headers, content etc"
      1082,Mozilla Thunderbird Calendar Data,Apps,Users\*\AppData\Roaming\Thunderbird\Profiles\*\calendar-data\local.sqlite,lazy_ntfs,Holds local calendar data
      1083,Mozilla Thunderbird Attachments,Apps,Users\*\AppData\Roaming\Thunderbird\Profiles\*\Attachments\*,lazy_ntfs,Holds attachments
      1084,Mozilla Thunderbird Address Book,Apps,Users\*\AppData\Roaming\Thunderbird\Profiles\*\abook.sqlite,lazy_ntfs,Holds local address book
      1085,Total Commander - .ini File,Apps,Users\*\AppData\Roaming\GHISLER\wincmd.ini,lazy_ntfs,Locates .ini file associated with Total Commander which stores useful user activity information.
      1086,Total Commander - Log File,Apps,**10\totalcmd.log,lazy_ntfs,Locates log file associated with Total Commander. NOTE: this log file is NOT enabled by default and the filename can be modified.
      1087,Total Commander - Temp Files Created During Folder Traversal,Apps,Users\*\AppData\Local\Temp\FTP*.tmp,lazy_ntfs,Locates .tmp files which are created during the user's folder traversal and provide insight into contents of each folder traversed.
      1088,Total Commander - FTP .ini File,Apps,Users\*\AppData\Roaming\GHISLER\wcx_ftp.ini,lazy_ntfs,Locates .ini file associated with Total Commander which stores useful FTP information.
      1089,Total Commander - File Tree,Apps,Users\*\AppData\Local\GHISLER\treeinfo*.wc,lazy_ntfs,Locates a file that contains an exhaustive file tree of a user's file system.
      1090,Total Commander - FTP Logs,Apps,Users\*\AppData\Local\Temp\tcftp.log,lazy_ntfs,Locates a file that contains the Total Commander FTP logs.
      1091,TreeSize - ScanHistory.XML,Apps,Users\*\AppData\Roaming\JAM Software\TreeSize\scanhistory.xml,lazy_ntfs,Locates XML file that provides a list of previously scanned directories by the user.
      1092,UltraViewer Logs,Remote Access,Users\*\AppData\Roaming\UltraViewer\**10,lazy_ntfs,"Includes all files related to UltraViewer chat, connections, and recordings"
      1093,UltraViewer Logs,Remote Access,Program Files*\UltraViewer\UltraViewerService_log.txt,lazy_ntfs,UltraViewer Service log file
      1094,UltraViewer Logs,Remote Access,Program Files*\UltraViewer\ConnectionLog.Log,lazy_ntfs,UltraViewer Service level connection log
      1095,VLC Recently Opened Files,Apps,Users\*\AppData\Roaming\vlc\vlc-qt-interface.ini,lazy_ntfs,Configuration file for VLC. Holds [RecentsMRL] key which lists recently opened files as well as sometimes retaining timestamps for file opening
      1096,VLC Recorded Files,Apps,Users\*\Videos\vlc-*.avi,lazy_ntfs,"Recorded files in VLC. Sometimes the Record button may be pressed instead of Play by suspects, which can record them watching content with VLC"
      1097,VMware - Virtual Machine Inventory,Apps,Users\*\AppData\Roaming\VMware,lazy_ntfs,Locates an inventory of all Virtual Machines on disk.
      1098,VMware (Fusion/Workstation/Server/Player),Memory,**10\*.vmem,lazy_ntfs,Captures all raw memory from VMware virtual machines.
      1099,VMware (Fusion/Workstation/Server/Player),Memory,**10\*.vmss,lazy_ntfs,Captures all memory images from VMware virtual machines.
      1100,VMware (Fusion/Workstation/Server/Player),Memory,**10\*.vmsn,lazy_ntfs,Captures all memory images from VMware virtual machines.
      1101,RealVNC Log,ApplicationLogs,Users\*\AppData\Local\RealVNC\vncserver.log,lazy_ntfs,https://www.realvnc.com/en/connect/docs/logging.html#logging
      1102,Viber Config Database,Apps,Users\*\AppData\Roaming\ViberPC\config.db,lazy_ntfs,Configuration file for Viber
      1103,Viber Users Data Database,Apps,Users\*\AppData\Roaming\ViberPC\*\viber.db,lazy_ntfs,"Viber data for that user, containing Calls, Chat Messages, Contacts and more"
      1104,Viber Users Avatars Cache,Apps,Users\*\AppData\Roaming\ViberPC\*\Avatars,lazy_ntfs,Cache of the Avatars for other Viber users
      1105,Viber Users Backgrounds Cache,Apps,Users\*\AppData\Roaming\ViberPC\*\Backgrounds,lazy_ntfs,Store of the backgrounds
      1106,Viber Users Thumbnails Cache,Apps,Users\*\AppData\Roaming\ViberPC\*\Thumbnails,lazy_ntfs,Cache of the thumbnails for uploaded/downloaded images
      1107,VirtualBox VM configs,Apps,**10\*.vbox,lazy_ntfs,Locates all .vbox VM configuration files on disk
      1108,VirtualBox VM backup configs,Apps,**10\*.vbox-prev,lazy_ntfs,Locates all backup .vbox VM configuration files on disk
      1109,VirtualBox Logs,Apps,**10\VBox.log,lazy_ntfs,Locates all VBox.log files on disk
      1110,VirtualBox Backup Logs,Apps,**10\VBox.log.*,lazy_ntfs,Locates all backup VBox.log files on disk - these can show historic VM usage
      1111,VirtualBox Hardening Logs,Apps,**10\VBoxHardening.log,lazy_ntfs,Locates all VBoxHardening.log files on disk
      1112,VirtualBox,Memory,**10\*.sav,lazy_ntfs,Captures all partial memory images from VirtualBox.
      1113,WhatsApp Cache,Apps,Users\*\AppData\Roaming\WhatsApp\Cache,lazy_ntfs,"Copies the cache of WhatsApp. Can be opened with Chrome Cache Viewer for viewing embedded thumbnails and other image artefacts, as well as extracting .enc message files or other files"
      1114,WhatsApp Local Storage,Apps,Users\*\AppData\Roaming\WhatsApp\Local Storage\leveldb,lazy_ntfs,"Copies the Local Storage leveldb of WhatsApp. Contains phone model and name of user, plus encrypted base64 strings which can be viewed with LevelDBDumper"
      1115,WinSCP (.ini file),Logs,**10\WinSCP.ini,lazy_ntfs,
      1116,Windows Your Phone - All Databases,Apps,Users\*\AppData\Local\Packages\Microsoft.YourPhone_8wekyb3d8bbwe\LocalCache\Indexed\**10,lazy_ntfs,Locates all Your Phone database files
      1117,XYplorer - .ini file,Apps,Users\*\AppData\Roaming\XYplorer\XYplorer.ini,lazy_ntfs,Locates .ini file associated with Total Commander which stores useful user activity information.
      1118,XYplorer - .ini file for each respective pane,Apps,Users\*\AppData\Roaming\XYplorer\Panes\*\**10\pane.ini,lazy_ntfs,Locates the .ini file for the left and right pane.
      1119,XYplorer - AutoBackup folder,Apps,Users\*\AppData\Roaming\XYplorer\AutoBackup\**10,lazy_ntfs,Locates the AutoBackup folder and copies its contents.
      1120,XYplorer - .dat files,Apps,Users\*\AppData\Roaming\XYplorer\**10\*.dat,lazy_ntfs,"Locates the .dat files in the XYplorer's AppData folder, all of which are updated upon program's exit."
      1121,Zoho Assist log files in AppData\Local,Apps,Users\*\AppData\Local\ZohoMeeting\log\**10,lazy_ntfs,Zoho Assist log files in AppData
      ocal
      1122,Zoho Assist .conf files in AppData\Local,Apps,Users\*\AppData\Local\ZohoMeeting\*.conf,lazy_ntfs,Grabs all .conf files present in this folder (Connection/Settings)
      1123,Zoho Assist log files in ProgramData,Apps,ProgramData\ZohoMeeting\log\**10,lazy_ntfs,Zoho Assist log files in ProgramData
      1124,Zoho Assist .conf files,Apps,ProgramData\ZohoMeeting\**10\*.conf,lazy_ntfs,Grabs all .conf files present in this folder (Connection/Proxy/Settings)
      1125,Zoho Assist log files in Program Files*,Apps,Program Files*\ZohoMeeting\UnAttended\ZohoMeeting\logs\**10,lazy_ntfs,Zoho Assist log files in Program Files*
      1126,Zoho Assist .conf files in  Program Files*,Apps,Program Files*\ZohoMeeting\UnAttended\ZohoMeeting\*.conf,lazy_ntfs,Grabs all .conf files present in this folder (Service/Settings)
      1127,Zoho Assist .txt files in  Program Files*,Apps,Program Files*\ZohoMeeting\UnAttended\ZohoMeeting\*.txt,lazy_ntfs,Grabs all .txt files present in this folder (Service/Settings)
      1128,Zoom client logs,Apps,Users\*\AppData\Roaming\Zoom\logs\**10\*,lazy_ntfs,Zoom client artifacts
      1129,Zoom client logs (Windows XP),Apps,Documents and Settings\*\Application Data\Zoom\**10\*,lazy_ntfs,Zoom client artifacts (Windows XP)
      1130,Zoom client recordings,Apps,Users\*\Documents\Zoom\**10\*,lazy_ntfs,Zoom recording artifacts
      1131,Zoom plugin (Outlook),Apps,Users\*\AppData\Roaming\Zoom Plugin\*.json,lazy_ntfs,Zoom plugin artifacts
      1132,iTunes Backup Folder,Communications,Users\*\AppData\Roaming\Apple\Mobilesync\Backup\**10,lazy_ntfs,
      1133,iTunes Backup Folder,Communications,Users\*\AppData\Roaming\Apple Computer\Mobilesync\Backup\**10,lazy_ntfs,
      1134,iTunes Backup Folder - iOS13,Communications,Users\*\Apple\Mobilesync\Backup\**10,lazy_ntfs,
      1135,mIRC Chat Logs (Vista+),Communications,Users\*\AppData\Roaming\mIRC\logs\**10,lazy_ntfs,
      1136,mIRC Chat Logs (2000/XP),Communications,Documents and Settings\*\Application Data\mIRC\logs\**10,lazy_ntfs,
      1137,mRemoteNG Logs,Communications,Users\*\AppData\Roaming\mRemoteNG\mRemoteNG.log,lazy_ntfs,Contains log entries for remote connections
      1138,mRemoteNG Connection Configuration and Backups,Communications,Users\*\AppData\Roaming\mRemoteNG\confCons.xml*,lazy_ntfs,"Contains connection config, often with obfuscated credentials"
      1139,mRemoteNG Program Settings,Communications,Users\*\AppData\*\mRemoteNG\**10\user.config,lazy_ntfs,Contains user-specific program settings
      1140,pCloud Database,Apps,Users\*\AppData\Local\pCloud\*.db,lazy_ntfs,Database contains all files sync'd with pCloud account.
      1141,pCloud Database WAL File,Apps,Users\*\AppData\Local\pCloud\*.db-wal,lazy_ntfs,Write-Ahead Log for pCloud database file.
      1142,pCloud Database Shared Memory File,Apps,Users\*\AppData\Local\pCloud\*.db-shm,lazy_ntfs,Shared Memory for the pCloud database file.
  - name: KapeTargets
    type: hidden
    description: Each parameter above represents a group of rules to be triggered. This table specifies which rule IDs will be included when the parameter is checked.
    default: |
      Group,RuleIds
      _BasicCollection,"[88, 479, 480, 481, 482, 483, 484, 485, 487, 488, 489, 490, 491, 492, 493, 515, 516, 517, 546, 547, 548, 549, 550, 551, 552, 553, 575, 576, 588, 589, 593, 594, 623, 624, 625, 626, 627, 628, 629, 630, 631, 632, 633, 634, 635, 636, 637, 638, 639, 640, 641, 642, 643, 644, 645, 646, 647, 648, 649, 650, 651, 652, 653, 654, 655, 656, 657, 658, 659, 660, 661, 662, 663, 664, 665, 666, 667, 668, 669, 670, 671, 672, 750, 751, 752, 753, 754, 755, 757, 758, 759, 760, 761, 762, 770, 771, 772, 773, 774, 775, 811, 812]"
      _SANS_Triage,"[1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31, 32, 33, 34, 35, 36, 37, 38, 39, 40, 41, 42, 43, 44, 45, 46, 47, 48, 49, 50, 51, 52, 53, 54, 55, 56, 57, 58, 59, 60, 61, 62, 63, 64, 65, 66, 67, 68, 69, 71, 72, 73, 74, 75, 76, 88, 192, 193, 194, 195, 196, 197, 198, 199, 200, 201, 202, 203, 204, 205, 206, 207, 208, 209, 210, 211, 220, 221, 222, 223, 224, 225, 226, 227, 228, 229, 230, 231, 232, 233, 234, 235, 236, 237, 238, 239, 240, 241, 242, 243, 244, 245, 246, 247, 248, 249, 250, 251, 252, 253, 254, 255, 256, 257, 258, 262, 263, 264, 265, 266, 267, 268, 269, 270, 271, 272, 273, 274, 275, 276, 277, 278, 279, 280, 281, 282, 283, 284, 285, 286, 287, 288, 289, 290, 291, 292, 293, 294, 295, 296, 297, 298, 299, 300, 301, 302, 303, 304, 305, 306, 307, 308, 309, 310, 311, 312, 313, 314, 315, 316, 317, 318, 319, 320, 321, 322, 323, 324, 325, 326, 327, 328, 329, 330, 331, 332, 333, 334, 335, 336, 337, 338, 339, 340, 341, 479, 480, 481, 482, 483, 484, 485, 487, 488, 489, 490, 491, 492, 493, 494, 495, 496, 497, 515, 516, 517, 518, 519, 520, 521, 522, 523, 524, 525, 526, 527, 546, 547, 548, 549, 550, 551, 552, 553, 575, 576, 577, 578, 579, 580, 581, 582, 583, 584, 585, 586, 587, 588, 589, 593, 594, 623, 624, 625, 626, 627, 628, 629, 630, 631, 632, 633, 634, 635, 636, 637, 638, 639, 640, 641, 642, 643, 644, 645, 646, 647, 648, 649, 650, 651, 652, 653, 654, 655, 656, 657, 658, 659, 660, 661, 662, 663, 664, 665, 666, 667, 668, 669, 670, 671, 672, 750, 751, 752, 753, 754, 755, 756, 757, 758, 759, 760, 761, 762, 770, 771, 772, 773, 774, 775, 780, 781, 786, 787, 811, 812, 823, 833, 834, 835, 836, 837, 838, 839, 840, 841, 842, 850, 851, 854, 870, 871, 879, 880, 881, 882, 883, 884, 912, 913, 920, 921, 939, 940, 941, 942, 943, 944, 945, 946, 947, 953, 954, 958, 968, 969, 970, 971, 972, 988, 989, 1025, 1026, 1027, 1028, 1029, 1030, 1031, 1032, 1033, 1034, 1037, 1038, 1039, 1040, 1041, 1042, 1043, 1044, 1045, 1046, 1047, 1048, 1049, 1050, 1051, 1052, 1055, 1056, 1063, 1064, 1068, 1069, 1070, 1071, 1072, 1092, 1093, 1094, 1101, 1102, 1103, 1104, 1105, 1106, 1113, 1114, 1121, 1122, 1123, 1124, 1125, 1126, 1127, 1135, 1136, 1137, 1138, 1139]"
      _Boot,[479]
      _J,"[480, 481, 482, 483]"
      _LogFile,[484]
      _MFT,[485]
      _MFTMirr,[486]
      _T,"[487, 488]"
      1Password,"[825, 826, 827]"
      4KVideoDownloader,[828]
      AVG,"[1, 2, 3, 4, 5, 6, 7]"
      AceText,[829]
      AcronisTrueImage,"[830, 831, 832]"
      Amcache,"[489, 490, 491, 492]"
      Ammyy,[833]
      Antivirus,"[1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31, 32, 33, 34, 35, 36, 37, 38, 39, 40, 41, 42, 43, 44, 45, 46, 47, 48, 49, 50, 51, 52, 53, 54, 55, 56, 57, 58, 59, 60, 61, 62, 63, 64, 65, 66, 67, 68, 69, 71, 72, 73, 74, 75, 76, 494, 495, 496, 497]"
      AnyDesk,"[834, 835, 836, 837, 838, 839, 840, 841, 842]"
      ApacheAccessLog,[77]
      AppCompatPCA,[493]
      AppData,[342]
      ApplicationEvents,"[494, 495, 496, 497]"
      AsperaConnect,"[843, 844]"
      AssetAdvisorLog,[498]
      AteraAgent,"[845, 846, 847, 848, 849]"
      Avast,"[8, 9, 10, 11, 12, 13]"
      AviraAVLogs,"[14, 15, 16]"
      BCD,"[499, 500]"
      BITS,[501]
      BitTorrent,[355]
      Bitdefender,"[17, 18, 19]"
      BoxDrive_Metadata,"[850, 851]"
      BoxDrive_UserFiles,"[852, 853]"
      BraveBrowser,"[192, 193, 194, 195, 196, 197, 198, 199, 200, 201, 202, 203, 204, 205, 206, 207, 208, 209, 210, 211]"
      BrowserCache,"[212, 213, 214, 215, 216, 217, 218, 219]"
      CertUtil,"[502, 503, 504]"
      Chrome,"[220, 221, 222, 223, 224, 225, 226, 227, 228, 229, 230, 231, 232, 233, 234, 235, 236, 237, 238, 239, 240, 241, 242, 243, 244, 245, 246, 247, 248, 249, 250, 251, 252, 253, 254, 255, 256, 257, 258]"
      ChromeExtensions,"[259, 260]"
      ChromeFileSystem,[261]
      CiscoJabber,[854]
      ClipboardMaster,"[855, 856, 857]"
      CloudStorage_All,"[850, 851, 852, 853, 879, 880, 881, 882, 883, 884, 885, 911, 912, 913, 988, 989, 990, 1058, 1059, 1060, 1140, 1141, 1142]"
      CloudStorage_Metadata,"[850, 851, 879, 880, 881, 882, 883, 884, 912, 913, 988, 989]"
      CloudStorage_OneDriveExplorer,"[590, 591, 592, 593, 594, 664, 665, 666, 667, 668, 669, 670, 671, 672, 988, 989]"
      CombinedLogs,"[88, 515, 516, 517, 518, 519, 520, 521, 522, 523, 524, 525, 526, 527, 773, 774, 775, 786, 787]"
      Combofix,[20]
      ConfluenceLogs,"[858, 859]"
      Cybereason,"[21, 22, 23]"
      DC__,[356]
      DWAgent,[860]
      Debian,"[393, 394, 395, 396, 397, 398, 399, 400, 401, 402, 403, 404, 405, 406, 407, 408, 409, 410]"
      DirectoryOpus,"[861, 862, 863, 864, 865, 866, 867, 868, 869]"
      DirectoryTraversal_AudioFiles,[343]
      DirectoryTraversal_ExcelDocuments,[344]
      DirectoryTraversal_PDFDocuments,[345]
      DirectoryTraversal_PictureFiles,[346]
      DirectoryTraversal_SQLiteDatabases,[347]
      DirectoryTraversal_VideoFiles,[348]
      DirectoryTraversal_WildCardExample,[349]
      DirectoryTraversal_WordDocuments,[350]
      Discord,"[870, 871]"
      DoubleCommander,"[872, 873, 874, 875, 876, 877, 878]"
      Dropbox_Metadata,"[879, 880, 881, 882, 883, 884]"
      Dropbox_UserFiles,[885]
      EFCommander,[886]
      ESET,"[24, 25, 26, 27]"
      Edge,[262]
      EdgeChromium,"[263, 264, 265, 266, 267, 268, 269, 270, 271, 272, 273, 274, 275, 276, 277, 278, 279, 280, 281, 282, 283, 284]"
      Emsisoft,[28]
      EncapsulationLogging,"[505, 506, 507, 508]"
      EventLogs_RDP,"[509, 510, 511, 512, 513, 514]"
      EventLogs,"[515, 516, 517]"
      EventTraceLogs,"[518, 519, 520, 521, 522, 523, 524, 525, 526, 527]"
      EventTranscriptDB,"[528, 529, 530]"
      Evernote,"[887, 888, 889]"
      Everything__VoidTools_,"[890, 891, 892, 893]"
      EvidenceOfExecution,"[489, 490, 491, 492, 493, 575, 576, 588, 589, 770, 771]"
      Exchange,"[531, 894]"
      ExchangeClientAccess,[531]
      ExchangeCve_2021_26855,"[532, 533, 534, 535]"
      ExchangeTransport,[894]
      FSecure,"[29, 30, 31]"
      FTPClients,"[896, 897, 898, 899, 1115]"
      Fences,[895]
      FileExplorerReplacements,"[861, 862, 863, 864, 865, 866, 867, 868, 869, 872, 873, 874, 875, 876, 877, 878, 886, 900, 901, 902, 903, 904, 905, 906, 975, 976, 977, 978, 979, 980, 986, 987, 1022, 1023, 1054, 1065, 1066, 1067, 1085, 1086, 1087, 1088, 1089, 1090, 1117, 1118, 1119, 1120]"
      FileSystem,"[479, 480, 481, 482, 483, 484, 485, 487, 488]"
      FileZillaClient,"[896, 897]"
      FileZillaServer,"[898, 899]"
      Firefox,"[285, 286, 287, 288, 289, 290, 291, 292, 293, 294, 295, 296, 297, 298, 299, 300, 301, 302, 303, 304, 305, 306, 307, 308, 309, 310, 311, 312, 313, 314, 315, 316, 317, 318, 319]"
      FreeCommander,"[900, 901, 902, 903, 904, 905, 906]"
      FreeDownloadManager,"[907, 908, 909]"
      FreeFileSync,[910]
      Freenet,"[357, 358, 359, 360, 361]"
      FrostWire,"[362, 363, 364]"
      Gigatribe,"[365, 366, 367]"
      GoogleDriveBackupSync_UserFiles,[911]
      GoogleDrive_Metadata,"[912, 913]"
      GoogleEarth,"[914, 915, 916, 917]"
      GroupPolicy,"[536, 537, 538, 539, 540, 541]"
      HeidiSQL,"[918, 919]"
      HexChat,[920]
      HitmanPro,"[32, 33, 34]"
      IISConfiguration,"[542, 543, 544, 545]"
      IISLogFiles,"[78, 79, 80, 81, 82, 83]"
      IRCClients,"[920, 921, 1135, 1136]"
      IceChat,[921]
      InternetExplorer,"[320, 321, 322, 323, 324, 325, 326, 327, 328, 329, 330, 331, 332]"
      IrfanView,[922]
      JDownloader2,"[923, 924, 925, 926, 927]"
      JavaWebCache,"[928, 929, 930, 931, 932, 933, 934, 935, 936, 937, 938]"
      Kali,"[411, 412, 413, 414, 415, 416, 417, 418, 419, 420, 421, 422, 423, 424, 425, 426, 427, 428]"
      KapeTriage,"[1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31, 32, 33, 34, 35, 36, 37, 38, 39, 40, 41, 42, 43, 44, 45, 46, 47, 48, 49, 50, 51, 52, 53, 54, 55, 56, 57, 58, 59, 60, 61, 62, 63, 64, 65, 66, 67, 68, 69, 71, 72, 73, 74, 75, 76, 88, 192, 193, 194, 195, 196, 197, 198, 199, 200, 201, 202, 203, 204, 205, 206, 207, 208, 209, 210, 211, 220, 221, 222, 223, 224, 225, 226, 227, 228, 229, 230, 231, 232, 233, 234, 235, 236, 237, 238, 239, 240, 241, 242, 243, 244, 245, 246, 247, 248, 249, 250, 251, 252, 253, 254, 255, 256, 257, 258, 262, 263, 264, 265, 266, 267, 268, 269, 270, 271, 272, 273, 274, 275, 276, 277, 278, 279, 280, 281, 282, 283, 284, 285, 286, 287, 288, 289, 290, 291, 292, 293, 294, 295, 296, 297, 298, 299, 300, 301, 302, 303, 304, 305, 306, 307, 308, 309, 310, 311, 312, 313, 314, 315, 316, 317, 318, 319, 320, 321, 322, 323, 324, 325, 326, 327, 328, 329, 330, 331, 332, 333, 334, 335, 336, 337, 338, 339, 340, 341, 479, 480, 481, 482, 483, 484, 485, 487, 488, 489, 490, 491, 492, 493, 494, 495, 496, 497, 515, 516, 517, 546, 547, 548, 549, 550, 551, 552, 553, 575, 576, 577, 578, 579, 580, 581, 582, 583, 584, 585, 586, 587, 588, 589, 593, 594, 623, 624, 625, 626, 627, 628, 629, 630, 631, 632, 633, 634, 635, 636, 637, 638, 639, 640, 641, 642, 643, 644, 645, 646, 647, 648, 649, 650, 651, 652, 653, 654, 655, 656, 657, 658, 659, 660, 661, 662, 663, 664, 665, 666, 667, 668, 669, 670, 671, 672, 750, 751, 752, 753, 754, 755, 756, 757, 758, 759, 760, 761, 762, 770, 771, 823, 833, 834, 835, 836, 837, 838, 839, 840, 841, 842, 939, 940, 941, 942, 943, 944, 945, 946, 947, 953, 954, 1025, 1026, 1027, 1028, 1029, 1030, 1031, 1032, 1033, 1034, 1055, 1056, 1063, 1064, 1068, 1069, 1070, 1092, 1093, 1094, 1101, 1121, 1122, 1123, 1124, 1125, 1126, 1127, 1137, 1138, 1139]"
      Kaseya,"[939, 940, 941, 942, 943, 944, 945, 946, 947]"
      Keepass,"[948, 949, 950]"
      KeepassXC,"[951, 952]"
      LNKFilesAndJumpLists,"[546, 547, 548, 549, 550, 551, 552, 553]"
      LinuxOnWindowsProfileFiles,"[554, 555, 556, 557]"
      LiveUserFiles,"[351, 352, 353, 354]"
      LogFiles,"[558, 559]"
      LogMeIn,"[494, 495, 496, 497, 953, 954]"
      MOF,[560]
      MSSQLErrorLog,"[84, 85]"
      MacriumReflect,"[955, 956, 957]"
      Malwarebytes,"[35, 36, 37, 38]"
      ManageEngineLogs,[86]
      Mattermost,[958]
      McAfee,"[39, 40, 41, 42, 43]"
      McAfee_ePO,[44]
      MediaMonkey,"[959, 960]"
      MemoryFiles,"[561, 562, 563, 564, 565]"
      MessagingClients,"[854, 870, 871, 920, 921, 958, 968, 969, 970, 971, 972, 1037, 1038, 1039, 1040, 1041, 1042, 1043, 1044, 1045, 1046, 1047, 1048, 1049, 1050, 1051, 1052, 1071, 1072, 1102, 1103, 1104, 1105, 1106, 1113, 1114, 1135, 1136]"
      MicrosoftOfficeBackstage,[566]
      MicrosoftOneNote,"[961, 962, 963, 964, 965]"
      MicrosoftStickyNotes,"[966, 967]"
      MicrosoftTeams,"[968, 969, 970, 971, 972]"
      MicrosoftToDo,"[973, 974]"
      MidnightCommander,[975]
      MiniTimelineCollection,"[479, 480, 481, 482, 483, 484, 485, 487, 488, 515, 516, 517, 623, 624, 625, 626, 627, 628, 629, 630, 631, 632, 633, 634, 635, 636, 637, 638, 639, 640, 641, 642, 643, 644, 645, 646, 647, 648, 649, 650, 651, 652, 653, 654, 655, 656, 657, 658, 659, 660, 661, 662, 663, 664, 665, 666, 667, 668, 669, 670, 671, 672]"
      MultiCommander,"[976, 977, 978, 979, 980]"
      NETCLRUsageLogs,[567]
      NGINXLogs,[87]
      NZBGet,"[368, 369]"
      Nessus,"[981, 982]"
      NewsbinPro,[370]
      Newsleecher,[371]
      Nicotine__,"[372, 373, 374, 375, 376, 377, 378, 379, 380, 381, 382]"
      Notepad__,"[983, 984, 985]"
      OfficeAutosave,"[568, 569, 570, 571]"
      OfficeDiagnostics,"[572, 573]"
      OfficeDocumentCache,[574]
      OneCommander,"[986, 987]"
      OneDrive_Metadata,"[988, 989]"
      OneDrive_UserFiles,[990]
      OpenSSHClient,"[991, 992, 993, 994, 995, 996, 997, 998, 999]"
      OpenSSHServer,"[1000, 1001, 1002, 1003, 1004, 1005, 1006, 1007, 1008]"
      OpenVPNClient,"[1009, 1010, 1011]"
      Opera,"[333, 334]"
      OutlookPSTOST,"[1012, 1013, 1014, 1015, 1016, 1017, 1018, 1019]"
      P2PClients,"[356, 362, 363, 364, 365, 366, 367, 385, 386, 387]"
      PeaZip,[1020]
      PowerShellConsole,[88]
      Prefetch,"[575, 576]"
      ProtonVPN,[1021]
      PuffinSecureBrowser,"[335, 336, 337, 338, 339, 340, 341]"
      Q_Dir,"[1022, 1023]"
      QFinderPro__QNAP_,[1024]
      RDPCache,"[577, 578, 579]"
      RDPLogs,"[580, 581, 582, 583, 584, 585, 586, 587]"
      Radmin,"[1025, 1026, 1027, 1028, 1029]"
      RecentFileCache,"[588, 589]"
      RecycleBin,"[590, 591, 592, 593, 594]"
      RecycleBin_DataFiles,"[590, 591, 592]"
      RecycleBin_InfoFiles,"[593, 594]"
      RegistryHives,"[623, 624, 625, 626, 627, 628, 629, 630, 631, 632, 633, 634, 635, 636, 637, 638, 639, 640, 641, 642, 643, 644, 645, 646, 647, 648, 649, 650, 651, 652, 653, 654, 655, 656, 657, 658, 659, 660, 661, 662, 663, 664, 665, 666, 667, 668, 669, 670, 671, 672]"
      RegistryHivesOther,"[595, 596, 597, 598, 599, 600, 601, 602, 603, 604, 605, 606, 607, 608, 609, 610, 611, 612, 613, 614, 615, 616, 617, 618, 619, 620, 621, 622]"
      RegistryHivesSystem,"[623, 624, 625, 626, 627, 628, 629, 630, 631, 632, 633, 634, 635, 636, 637, 638, 639, 640, 641, 642, 643, 644, 645, 646, 647, 648, 649, 650, 651, 652, 653, 654, 655, 656, 657, 658, 659, 660, 661, 662, 663]"
      RegistryHivesUser,"[664, 665, 666, 667, 668, 669, 670, 671, 672]"
      RemoteAdmin,"[494, 495, 496, 497, 577, 578, 579, 580, 581, 582, 583, 584, 585, 586, 587, 833, 834, 835, 836, 837, 838, 839, 840, 841, 842, 939, 940, 941, 942, 943, 944, 945, 946, 947, 953, 954, 1025, 1026, 1027, 1028, 1029, 1030, 1031, 1032, 1033, 1034, 1055, 1056, 1063, 1064, 1068, 1069, 1070, 1092, 1093, 1094, 1101, 1121, 1122, 1123, 1124, 1125, 1126, 1127, 1137, 1138, 1139]"
      RemoteUtilities_app,"[1030, 1031]"
      RoamingProfile,"[673, 674, 675, 676, 677, 678, 679, 680, 681, 682, 683, 684, 685, 686, 687, 688, 689, 690, 691, 692, 693, 694, 695, 696, 697, 698, 699, 700, 701, 702, 703, 704, 705, 706, 707, 708, 709, 710, 711, 712, 713, 714, 715, 716, 717, 718, 719, 720, 721, 722, 723, 724, 725, 726, 727, 728, 729, 730, 731, 732, 733, 734, 735, 736, 737, 738, 739, 740, 741, 742, 743, 744, 745]"
      RogueKiller,[45]
      SABnbzd,"[383, 384]"
      SDB,"[746, 747, 748, 749]"
      SOFELK,"[479, 480, 481, 482, 483, 484, 485, 487, 488, 489, 490, 491, 492, 493, 515, 516, 517, 546, 547, 548, 549, 550, 551, 552, 553, 575, 576, 588, 589, 770, 771]"
      SQLiteDatabases,"[89, 90, 91, 92, 93, 94, 95, 96, 97, 98, 99, 100, 101, 102, 103, 104, 105, 106, 107, 108, 109, 110, 111, 112, 113, 114, 115, 116, 117, 118, 119, 120, 121, 122, 123, 124, 125, 126, 127, 128, 129, 130, 131, 132, 133, 134, 135, 136, 137, 138, 139, 140, 141, 142, 143, 144, 145, 146, 147, 148, 149, 150, 151, 152, 153, 154, 155, 156, 157, 158, 159, 160, 161, 162, 163, 164, 165, 166, 167, 168, 169, 170, 171, 172, 173, 174, 175, 176, 177, 178, 179, 180, 181, 182, 183, 184, 185, 186, 187, 188, 189, 190, 191]"
      SRUM,"[750, 751, 752, 753, 754, 755]"
      SUM,[756]
      SUPERAntiSpyware,[46]
      SUSELinuxEnterpriseServer,"[429, 430, 431, 432, 433, 434, 435, 436, 437, 438, 439, 440, 441, 442]"
      ScheduledTasks,"[757, 758, 759, 760, 761, 762]"
      ScreenConnect,"[494, 495, 496, 497, 1032, 1033, 1034]"
      SecureAge,[47]
      SentinelOne,[48]
      ServerTriage,"[77, 78, 79, 80, 81, 82, 83, 84, 85, 86, 87, 531, 858, 859, 894, 898, 899, 1000, 1001, 1002, 1003, 1004, 1005, 1006, 1007, 1008]"
      ShareX,[1035]
      Shareaza,[385]
      SiemensTIA,[1036]
      Signal,"[1037, 1038, 1039, 1040]"
      SignatureCatalog,"[763, 764]"
      Skype,"[1041, 1042, 1043, 1044, 1045, 1046, 1047]"
      Slack,"[1048, 1049, 1050, 1051, 1052]"
      Snagit,[1053]
      SnipAndSketch,[765]
      Sophos,"[49, 50, 494, 495, 496, 497]"
      Soulseek,"[386, 387]"
      SpeedCommander,[1054]
      Splashtop,"[1055, 1056]"
      StartupFolders,"[766, 767]"
      StartupInfo,"[768, 769]"
      SublimeText,[1057]
      SugarSync,"[1058, 1059, 1060]"
      SumatraPDF,"[1061, 1062]"
      SupremoRemoteDesktop,"[1063, 1064]"
      Symantec_AV_Logs,"[51, 52, 53, 54, 55, 56, 57, 58, 59, 494, 495, 496, 497]"
      Syscache,"[770, 771]"
      TablacusExplorer,"[1065, 1066, 1067]"
      TeamViewerLogs,"[1068, 1069, 1070]"
      Telegram,"[1071, 1072]"
      TeraCopy,[1073]
      ThumbCache,[772]
      Thunderbird,"[1074, 1075, 1076, 1077, 1078, 1079, 1080, 1081, 1082, 1083, 1084]"
      TorrentClients,"[355, 390, 391, 392]"
      Torrents,[388]
      TotalAV,"[60, 61]"
      TotalCommander,"[1085, 1086, 1087, 1088, 1089, 1090]"
      TreeSize,[1091]
      TrendMicro,"[62, 63, 64]"
      USBDetective,"[489, 490, 491, 492, 515, 516, 517, 546, 547, 548, 549, 550, 551, 552, 553, 623, 624, 625, 626, 627, 628, 629, 630, 631, 632, 633, 634, 635, 636, 637, 638, 639, 640, 641, 642, 643, 644, 645, 646, 647, 648, 649, 650, 651, 652, 653, 654, 655, 656, 657, 658, 659, 660, 661, 662, 663, 664, 665, 666, 667, 668, 669, 670, 671, 672, 773, 774, 775]"
      USBDevicesLogs,"[773, 774, 775]"
      Ubuntu,"[443, 444, 445, 446, 447, 448, 449, 450, 451, 452, 453, 454, 455, 456, 457, 458, 459]"
      Ultraviewer,"[1092, 1093, 1094]"
      Usenet,[389]
      UsenetClients,"[368, 369, 370, 371, 383, 384]"
      VIPRE,"[65, 66, 67, 68]"
      VLC_Media_Player,"[1095, 1096]"
      VMware,"[776, 777, 778, 779, 1097, 1098, 1099, 1100]"
      VMwareInventory,[1097]
      VMwareMemory,"[1098, 1099, 1100]"
      VNCLogs,"[494, 495, 496, 497, 1101]"
      Viber,"[1102, 1103, 1104, 1105, 1106]"
      VirtualBox,"[776, 777, 778, 779, 1107, 1108, 1109, 1110, 1111, 1112]"
      VirtualBoxConfig,"[1107, 1108]"
      VirtualBoxLogs,"[1109, 1110, 1111]"
      VirtualBoxMemory,[1112]
      VirtualDisks,"[776, 777, 778, 779]"
      WBEM,"[780, 781]"
      WER,"[782, 783, 784, 785]"
      WSL,"[393, 394, 395, 396, 397, 398, 399, 400, 401, 402, 403, 404, 405, 406, 407, 408, 409, 410, 411, 412, 413, 414, 415, 416, 417, 418, 419, 420, 421, 422, 423, 424, 425, 426, 427, 428, 429, 430, 431, 432, 433, 434, 435, 436, 437, 438, 439, 440, 441, 442, 443, 444, 445, 446, 447, 448, 449, 450, 451, 452, 453, 454, 455, 456, 457, 458, 459, 460, 461, 462, 463, 464, 465, 466, 467, 468, 469, 470, 471, 472, 473]"
      WebBrowsers,"[192, 193, 194, 195, 196, 197, 198, 199, 200, 201, 202, 203, 204, 205, 206, 207, 208, 209, 210, 211, 220, 221, 222, 223, 224, 225, 226, 227, 228, 229, 230, 231, 232, 233, 234, 235, 236, 237, 238, 239, 240, 241, 242, 243, 244, 245, 246, 247, 248, 249, 250, 251, 252, 253, 254, 255, 256, 257, 258, 262, 263, 264, 265, 266, 267, 268, 269, 270, 271, 272, 273, 274, 275, 276, 277, 278, 279, 280, 281, 282, 283, 284, 285, 286, 287, 288, 289, 290, 291, 292, 293, 294, 295, 296, 297, 298, 299, 300, 301, 302, 303, 304, 305, 306, 307, 308, 309, 310, 311, 312, 313, 314, 315, 316, 317, 318, 319, 320, 321, 322, 323, 324, 325, 326, 327, 328, 329, 330, 331, 332, 333, 334, 335, 336, 337, 338, 339, 340, 341]"
      WebServers,"[77, 78, 79, 80, 81, 82, 83, 84, 85, 87]"
      Webroot,[69]
      WhatsApp,"[1113, 1114]"
      WinDefendDetectionHist,[70]
      WinSCP,[1115]
      WindowsDefender,"[71, 72, 73, 74, 75, 76]"
      WindowsFirewall,"[786, 787]"
      WindowsHello,"[788, 789, 790, 791, 792, 793, 794, 795, 796, 797, 798, 799, 800, 801, 802, 803, 804, 805, 806, 807, 808, 809, 810]"
      WindowsIndexSearch,"[811, 812]"
      WindowsNotificationsDB,"[813, 814]"
      WindowsOSUpgradeArtifacts,"[815, 816, 817, 818, 819]"
      WindowsPowerDiagnostics,[820]
      WindowsSubsystemforAndroid,"[474, 475, 476, 477, 478]"
      WindowsTelemetryDiagnosticsLegacy,"[821, 822]"
      WindowsTimeline,[823]
      WindowsYourPhone,[1116]
      XPRestorePoints,[824]
      XYplorer,"[1117, 1118, 1119, 1120]"
      ZohoAssist,"[1121, 1122, 1123, 1124, 1125, 1126, 1127]"
      Zoom,"[1128, 1129, 1130, 1131]"
      iTunesBackup,"[1132, 1133, 1134]"
      mIRC,"[1135, 1136]"
      mRemoteNG,"[1137, 1138, 1139]"
      openSUSE,"[460, 461, 462, 463, 464, 465, 466, 467, 468, 469, 470, 471, 472, 473]"
      pCloudDatabase,"[1140, 1141, 1142]"
      qBittorrent,"[390, 391]"
      uTorrent,[392]
  - name: DontBeLazy
    description: Normally we prefer to use lazy_ntfs for speed. Sometimes this might miss stuff so setting this will fallback to the regular ntfs accessor.
    type: bool

  - name: NTFS_CACHE_TIME
    type: int
    description: How often to flush the NTFS cache. (Default is never).
    default: "1000000"

sources:
  - name: All File Metadata
    query: |
      -- Select all the rule Ids to be included depending on the group
      -- selection.
      LET targets <= SELECT * FROM parse_csv(
           filename=KapeTargets, accessor="data")
      WHERE get(member=Group) AND log(message="Selecting " + Group)

      -- Filter only the rules in the rule table that have an Id we
      -- want. Targets with $ in their name probably refer to ntfs
      -- special files and so they are designated as ntfs
      -- accessor. Other targets may need ntfs parsing but not
      -- necessary - they are designated with the lazy_ntfs accessor.
      LET rule_specs_ntfs <= SELECT Id, Glob
        FROM parse_csv(filename=KapeRules, accessor="data")
        WHERE Id in array(array=targets.RuleIds) AND Accessor='ntfs'
        AND log(message="ntfs: Selecting glob " + Glob)

      LET rule_specs_lazy_ntfs <= SELECT Id, Glob
        FROM parse_csv(filename=KapeRules, accessor="data")
        WHERE Id in array(array=targets.RuleIds) AND Accessor='lazy_ntfs'
        AND log(message="auto: Selecting glob " + Glob)

      -- Call the generic VSS file collector with the globs we want in
      -- a new CSV file.
      LET all_results <= SELECT * FROM if(
           condition=VSSAnalysis,
           then={
             SELECT * FROM chain(async=TRUE,
               a={
                   -- For VSS we always need to parse NTFS
                   SELECT * FROM Artifact.Windows.Collectors.VSS(
                      RootDevice=Device, Accessor="ntfs",
                      collectionSpec=rule_specs_ntfs)
               }, b={
                   SELECT * FROM Artifact.Windows.Collectors.VSS(
                      RootDevice=Device,
                      Accessor=if(condition=DontBeLazy,
                                  then="ntfs", else="lazy_ntfs"),
                      collectionSpec=rule_specs_lazy_ntfs)
               })
           }, else={
             SELECT * FROM chain(async=TRUE,
               a={

                   -- Special files we access with the ntfs parser.
                   SELECT * FROM Artifact.Generic.Collectors.File(
                      Root=Device,
                      Accessor="ntfs",
                      collectionSpec=rule_specs_ntfs)
               }, b={

                   -- Prefer the auto accessor if possible since it
                   -- will fall back to ntfs if required but otherwise
                   -- will be faster.
                   SELECT * FROM Artifact.Generic.Collectors.File(
                      Root=Device,
                      Accessor=if(condition=UseAutoAccessor,
                                  then="auto", else="lazy_ntfs"),
                      collectionSpec=rule_specs_lazy_ntfs)
               })
           })

      SELECT * FROM all_results WHERE _Source =~ "Metadata"

  - name: Uploads
    query: |
      SELECT * FROM all_results WHERE _Source =~ "Uploads"

reports:
  - type: CLIENT
    template: |
      {{ import "Reporting.Default" "Templates" }}

      <!-- Default report in case the artifact does not have one -->
      ## {{ .Name }}

      {{ $name := .Name }}

      {{ template "hidden_paragraph_start" dict "description" "View Artifact Description" }}

      {{ Markdown .Description }}

      ### References</h3>

      {{ range .Reference }}
      * [{{ . }}]({{.}})
      {{- end }}

      {{ template "hidden_paragraph_end" }}

      {{ $query := print "SELECT SourceFile, Size, Modified, LastAccessed, Created \
          FROM source(source='All File Metadata')" }}

      <!-- There could be a huge number of rows just to get the count, so we cap at 10000 -->
      {{ $count := Get ( Query (print "LET X = " $query " LIMIT 10000 " \
         " SELECT 1 AS ALL, count() AS Count FROM X Group BY ALL") | Expand ) \
         "0.Count" 0 }}

      <!-- If this is a flow show the parameters. -->
      {{ $flow := Query "LET X = SELECT Request.Parameters.env AS \
         Env FROM flows(client_id=ClientId, flow_id=FlowId)" \
         "SELECT * FROM foreach(row=X[0].Env, query={ \
             SELECT Key, Value FROM scope()})" | Expand }}

      {{ if $flow }}

      ### Selected Targets

      {{- range $flow -}}{{- if eq (Get . "Value") "Y" }}
      * {{ Get . "Key" }}
      {{- end -}}{{- end }}
      {{ end }}

      ## Files collected

      {{ if gt $count 9999 }}
      Collected more than {{ $count }} files.
      {{ else }}
      Collected a total of {{ $count }} files.
      {{ end }}

      {{ Query $query | Table }}


```
