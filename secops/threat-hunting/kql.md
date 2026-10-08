# KQL

\#chinese

DeviceEvents

\| where ActionType == "ProcessCreate"

\| where (ProcessCommandLine contains "certutil" or ProcessCommandLine contains "ntdsutil" or ProcessCommandLine contains "xcopy")

\| project Timestamp, DeviceName, InitiatingProcessFileName, InitiatingProcessCommandLine, InitiatingProcessParentFileName, ProcessCommandLine, AccountDomain

\# WMI spawning

DeviceProcessEvents

\| where InitiatingProcessFileName in\~ ("winword.exe", "excel.exe", "outlook.exe")

and FileName =\~"wmic.exe"

\#deleteing shadow copies

DeviceProcessEvents

\| where FileName =\~ "wmic.exe"

\| where ProcessCommandLine has "shadowcopy" and ProcessCommandLine has "delete"

\| project DeviceId, Timestamp, InitiatingProcessFileName, FileName,

ProcessCommandLine, InitiatingProcessIntegrityLevel, InitiatingProcessParentFileName

DeviceProcessEvents

\| where SHA256 has\_any ('d4f545691c8441b5bcb86535b1d0fd16dc06786eb4080087588cd4d0f388d5ca',

'882d95bdbca75ab9d13486e477ab76b3978e14d6fca30c11ec368f7e5fa1d0cb',

'8ac52ca0792baf2a4075fe7c68e5cbe2262da604e2fcdfb9b39656430925c168',

'3771846f010fcad26d593ea3771bee7cf3dec4d7604a8c719cef500fbf491820',

'3033913c51e0bf9a13c7ad2d5a481e174a1a3f19041c339e6ac900824793a1c6',

'095fbb7685f5ad054bab28346d744e137564beabc33c13a25818936ddc739f5b',

)

DeviceNetworkEvents

\| where RemoteUrl contains "amazonaws.com/package/update.js"

DeviceNetworkEvents

\| summarize Port= count() by RemotePort

\| sort by Port

\| where RemotePort <1024

DeviceNetworkEvents

\| summarize Port= count() by RemotePort

\| where RemotePort <10000

\| sort by Port desc

DeviceNetworkEvents

\| summarize Rurl= count() by RemoteUrl

\| sort by Rurl desc

DeviceNetworkEvents

\| summarize ProcessName = count() by InitiatingProcessFileName

\| sort by ProcessName desc

DeviceNetworkEvents

\| summarize ProcessName = count() by InitiatingProcessCommandLine

\| sort by ProcessName asc

DeviceNetworkEvents

\| summarize ProcessName = count() by InitiatingProcessFolderPath

\| sort by ProcessName desc

DeviceLogonEvents

\| where IsLocalAdmin == true and LogonType != 'RemoteInteractive'

\| extend IsLocalLogon = tobool(todynamic(AdditionalFields).IsLocalLogon)

\| where IsLocalLogon==false

DeviceProcessEvents

\| where InitiatingProcessFileName == "ONENOTE.EXE" and not( FileName in\~ ('protocolhandler.exe','notepad.exe','Teams.exe','powerpnt.exe','ai.exe','msedge.exe','msedgewebview2.exe','chrome.exe','firefox.exe','opera.exe','acrobat.exe','brave.exe','iexplore.exe','winword.exe','excel.exe'  ,'AcroRd32.exe','ONENOTEM.EXE','OUTLOOK.EXE','ONENOTE.EXE','splwow64.exe'))

DeviceProcessEvents

\| where Timestamp  >= ago(10d)

\| where InitiatingProcessFileName in\~ ("sqlservr.exe", "sqlagent.exe",

"sqlps.exe", "launchpad.exe")

\| summarize tostring(makeset(ProcessCommandLine))

by DeviceId, bin(Timestamp, 2m)

\| where

set\_ProcessCommandLine has "certutil" or

set\_ProcessCommandLine has "netstat" or

set\_ProcessCommandLine has "ping" or

set\_ProcessCommandLine has "sysinfo" or

set\_ProcessCommandLine has "systeminfo" or

set\_ProcessCommandLine has "taskkill" or

set\_ProcessCommandLine has "wget" or

set\_ProcessCommandLine has "whoami" or

set\_ProcessCommandLine has "Invoke-WebRequest" or

set\_ProcessCommandLine has "Copy-Item" or

set\_ProcessCommandLine has "WebClient" or

set\_ProcessCommandLine has "advpack.dll" or

set\_ProcessCommandLine has "appvlp.exe" or

set\_ProcessCommandLine has "atbroker.exe" or

set\_ProcessCommandLine has "bash.exe" or

set\_ProcessCommandLine has "bginfo.exe" or

set\_ProcessCommandLine has "bitsadmin.exe" or

set\_ProcessCommandLine has "cdb.exe" or

set\_ProcessCommandLine has "certutil.exe" or

set\_ProcessCommandLine has "cl\_invocation.ps1" or

set\_ProcessCommandLine has "cl\_mutexverifiers.ps1" or

set\_ProcessCommandLine has "cmstp.exe" or

set\_ProcessCommandLine has "csi.exe" or

set\_ProcessCommandLine has "diskshadow\.exe" or

set\_ProcessCommandLine has "dnscmd.exe" or

set\_ProcessCommandLine has "dnx.exe" or

set\_ProcessCommandLine has "dxcap.exe" or

set\_ProcessCommandLine has "esentutl.exe" or

set\_ProcessCommandLine has "expand.exe" or

set\_ProcessCommandLine has "extexport.exe" or

set\_ProcessCommandLine has "extrac32.exe" or

set\_ProcessCommandLine has "findstr.exe" or

set\_ProcessCommandLine has "forfiles.exe" or

set\_ProcessCommandLine has "[ftp.exe](ftp://ftp.exe)" or

set\_ProcessCommandLine has "gpscript.exe" or

set\_ProcessCommandLine has "hh.exe" or

set\_ProcessCommandLine has "ie4uinit.exe" or

set\_ProcessCommandLine has "ieadvpack.dll" or

set\_ProcessCommandLine has "ieaframe.dll" or

set\_ProcessCommandLine has "ieexec.exe" or

set\_ProcessCommandLine has "infdefaultinstall.exe" or

set\_ProcessCommandLine has "installutil.exe" or

set\_ProcessCommandLine has "makecab.exe" or

set\_ProcessCommandLine has "manage-bde.wsf" or

set\_ProcessCommandLine has "mavinject.exe" or

set\_ProcessCommandLine has "mftrace.exe" or

set\_ProcessCommandLine has "microsoft.workflow\.compiler.exe" or

set\_ProcessCommandLine has "mmc.exe" or

set\_ProcessCommandLine has "msbuild.exe" or

set\_ProcessCommandLine has "msconfig.exe" or

set\_ProcessCommandLine has "msdeploy.exe" or

set\_ProcessCommandLine has "msdt.exe" or

set\_ProcessCommandLine has "mshta.exe" or

set\_ProcessCommandLine has "mshtml.dll" or

set\_ProcessCommandLine has "msiexec.exe" or

set\_ProcessCommandLine has "msxsl.exe" or

set\_ProcessCommandLine has "odbcconf.exe" or

set\_ProcessCommandLine has "pcalua.exe" or

set\_ProcessCommandLine has "pcwrun.exe" or

set\_ProcessCommandLine has "pcwutl.dll" or

set\_ProcessCommandLine has "pester.bat" or

set\_ProcessCommandLine has "presentationhost.exe" or

set\_ProcessCommandLine has "pubprn.vbs" or

set\_ProcessCommandLine has "rcsi.exe" or

set\_ProcessCommandLine has "regasm.exe" or

set\_ProcessCommandLine has "register-cimprovider.exe" or

set\_ProcessCommandLine has "regsvcs.exe" or

set\_ProcessCommandLine has "regsvr32.exe" or

set\_ProcessCommandLine has "replace.exe" or

set\_ProcessCommandLine has "rundll32.exe" or

set\_ProcessCommandLine has "runonce.exe" or

set\_ProcessCommandLine has "runscripthelper.exe" or

set\_ProcessCommandLine has "schtasks.exe" or

set\_ProcessCommandLine has "scriptrunner.exe" or

set\_ProcessCommandLine has "setupapi.dll" or

set\_ProcessCommandLine has "shdocvw\.dll" or

set\_ProcessCommandLine has "shell32.dll" or

set\_ProcessCommandLine has "slmgr.vbs" or

set\_ProcessCommandLine has "sqltoolsps.exe" or

set\_ProcessCommandLine has "syncappvpublishingserver.exe" or

set\_ProcessCommandLine has "syncappvpublishingserver.vbs" or

set\_ProcessCommandLine has "syssetup.dll" or

set\_ProcessCommandLine has "te.exe" or

set\_ProcessCommandLine has "tracker.exe" or

set\_ProcessCommandLine has "url.dll" or

set\_ProcessCommandLine has "verclsid.exe" or

set\_ProcessCommandLine has "vsjitdebugger.exe" or

set\_ProcessCommandLine has "wab.exe" or

set\_ProcessCommandLine has "winrm.vbs" or

set\_ProcessCommandLine has "wmic.exe" or

set\_ProcessCommandLine has "xwizard.exe" or

set\_ProcessCommandLine has "zipfldr.dll"

\| sort by DeviceId  , Timestamp asc

DeviceProcessEvents

\| where InitiatingProcessFileName == InitiatingProcessCommandLine

\| where ProcessCommandLine has\_any (

"whoami /all","cmd /c set","arp -a","ipconfig /all","net view /all","nslookup -querytype=ALL -timeout=10",

"net share","route print","netstat -nao","net localgroup")

\| summarize dcount(FileName), make\_set(ProcessCommandLine) by DeviceId,bin(Timestamp, 1d), InitiatingProcessFileName, InitiatingProcessCommandLine

\| where dcount\_FileName >= 8

// The query finds attempts to list users or groups using Net commands

DeviceProcessEvents

\| where Timestamp > ago(30d)

\| where FileName == 'net.exe' and AccountName != "" and ProcessCommandLine !contains '\\\\'  and ProcessCommandLine !contains '/add'

\| where (ProcessCommandLine contains ' user ' or ProcessCommandLine contains ' group ') and (ProcessCommandLine contains ' /do' or ProcessCommandLine contains ' /domain')

\| extend Target = extract("(?i)\[user|group] (\\"\*\[a-zA-Z0-9-\_ ]+\\"\*)", 1, ProcessCommandLine) | filter Target  != ''

\| project AccountName, Target, ProcessCommandLine, DeviceName, Timestamp

\| sort by AccountName, Target

// Find attempts to stop processes using net stop

DeviceProcessEvents

\| where Timestamp > ago(30d)

\| where FileName =\~ "net.exe" and ProcessCommandLine has "stop"

\| summarize netStopCount = dcount(ProcessCommandLine), NetStopList = make\_set(ProcessCommandLine) by DeviceId, bin(Timestamp, 2m)

\| where netStopCount > 10

DeviceProcessEvents

\| where FileName == "batloader.exe"

\| extend InitiatingProcessFileName = InitiatingProcessFileName

\| where InitiatingProcessFileName in ("cmd.exe", "powershell.exe", "regsvr32.exe")

\| summarize  DeviceId = DeviceId, InitiatingProcessFileName = InitiatingProcessFileName by FileName

DeviceProcessEvents

\| where ProcessCommandLine contains "route -p ADD"

DeviceNetworkEvents

\| where RemoteUrl contains "edex-beta.unidata.ucar.edu"

DeviceNetworkEvents

\| where RemoteUrl contains "api."

\| where not(RemoteUrl contains "microsoft" or RemoteUrl contains "azure"or RemoteUrl contains "amazon")

\| summarize Count = count() by RemoteUrl

\| sort by Count desc

DeviceNetworkEvents

\| where RemoteUrl contains "api.dfwairport"

\| summarize Count = count() by RemoteUrl

\| sort by Count desc

DeviceEvents

\| where DeviceId == "28bacf007232ea3f8ba2e8459307f76526d42071"

\| where ActionType contains "ScheduledTask"

let EncodedList = dynamic(\['-encodedcommand', '-enc']); // -e and -en can also be added, be aware of FPs

let ReconVariables = dynamic(\['Get-ADGroupMember', 'Get-ADComputer', 'Get-ADUser', 'Get-NetGPOGroup', 'net user', 'whoami', 'net group', 'hostname', 'netsh firewall', 'tasklist', 'arp', 'systeminfo']);

let TimeFrame = 48d; //Customizable h = hours, d = days

DeviceProcessEvents

\| where Timestamp > ago(TimeFrame)

\| where ProcessCommandLine contains "powershell" or InitiatingProcessCommandLine contains "powershell"

\| where ProcessCommandLine has\_any (EncodedList) or InitiatingProcessCommandLine has\_any (EncodedList)

\| extend base64String = extract(@'\s+(\[A-Za-z0-9+/]{20}\S+$)', 1, ProcessCommandLine)

\| extend DecodedCommandLine = base64\_decode\_tostring(base64String)

\| extend DecodedCommandLineReplaceEmptyPlaces = replace\_string(DecodedCommandLine, '\u0000', '')

\| where isnotempty(base64String) and isnotempty(DecodedCommandLineReplaceEmptyPlaces)

\| where DecodedCommandLineReplaceEmptyPlaces has\_any (ReconVariables)

\| project

     Timestamp,

     ActionType,

     DecodedCommandLineReplaceEmptyPlaces,

     ProcessCommandLine,

     InitiatingProcessCommandLine,

     DeviceName,

     AccountName,

     AccountDomain

DeviceEvents

\| where ActionType == 'AsrVulnerableSignedDriverBlocked'

\| distinct FolderPath, FileName, DeviceId

\| summarize deviceCount = count() by FolderPath, FileName

\| join (DeviceEvents| where ActionType == "AsrVulnerableSignedDriverBlocked"| summarize ruleCount = count() by FolderPath, FileName) on $left.FolderPath == $right.FolderPath and $left.FileName == $right.FileName

\| project FolderPath, FileName, deviceCount, ruleCount

\| order by ruleCount desc

DeviceEvents

\| where ActionType startswith 'asr'

\| distinct ActionType, DeviceId

\| summarize deviceCount = count() by ActionType

\| join (DeviceEvents | where ActionType startswith 'Asr' | summarize ruleCount = count() by ActionType) on $left.ActionType == $right.ActionType

\| project ActionType, deviceCount, ruleCount

DeviceNetworkEvents

\| where RemoteIP in ("37.220.87.69", "94.142.138.4", "99.230.89.236", "144.76.173.247", "3.142.81.166", "3.141.177.1", "94.142.138.61", "37.221.93.196", "2.57.122.154", "146.70.45.213", "146.70.45.212", "51.81.155.128", "45.14.227.137", "47.89.189.43", "138.199.63.93", "103.172.41.208", "47.90.254.4", "192.145.124.4", "164.92.205.166", "103.165.168.142", "163.172.83.95", "172.98.87.184", "173.231.16.77")

DeviceProcessEvents

\| where ActionType == "ProcessCreate" and FileName == "rundll32.exe"

\| extend CommandLine = extract(".\*\\"(.\*)\\".\*", 1, ProcessCommandLine)

\| where CommandLine contains "RestartManager" or CommandLine contains "RegisterApplicationRestart"

\| project Timestamp, DeviceName, FileName, ProcessCommandLine

\| order by Timestamp desc

EmailEvents

\| where NetworkMessageId in ("8f71c3b4-d18b-49ba-4a9f-08db5596bf99","72725b7e-9a3f-4bf6-9031-08db5593d7f4","04ed6e5d-1cb4-48dc-c889-08db559437d7","a52ce6f6-6d3a-42ab-2dde-08db55b49601","37ffb799-b873-4469-c53e-08db55aaee96","9312d239-7dc0-411e-06f6-08db55ac4e25","7f0e0a93-50ef-4713-8fb2-08db55b558cd","c02d8af0-f778-4098-7ec9-08db55ace635","f1ebc63f-279b-4b34-d392-08db55ab47e0","b028bc08-d720-4084-b8ed-08db55abd090","7caef4cf-f820-4a2a-8f3c-08db55b4f033","f3737190-321b-410b-1d8a-08db55abb435","a9606500-11fa-4522-6a16-08db55b481c2","198ad17e-b67c-4161-1278-08db55b4a310")

\| take 100
