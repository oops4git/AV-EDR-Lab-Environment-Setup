# AV/EDR Lab Environment Setup
| Initially taken from Maldev Academy Discord and added more resources.
| Notion Notes : https://an0nud4y.notion.site/AV-EDR-Lab-Env-Setup-130bc870022d8071935cc682d3eb34b9?pvs=4


- An example of things that can be used to emulate certain features that paid edrs have:
    - SACL - sysmon
        - https://detect.fyi/sysmon-a-viable-alternative-to-edr-44d4fbe5735a?gi=eb4475ea6b3d
        - https://techcommunity.microsoft.com/t5/windows-server-for-it-pro/active-directory-hunting-set-up-advanced-monitoring-with-sysmon/m-p/3977120
        - Sysmon Config : https://github.com/SwiftOnSecurity/sysmon-config
    - hooks - bitdefender free : [https://otterhacker.github.io/Malware/Function hooking.html](https://otterhacker.github.io/Malware/Function%20hooking.html)
        - HookDetector (Detect all hooked APIs) : https://github.com/matterpreter/OffensiveCSharp/tree/master/HookDetector
    - Detecting manual syscalls from usermode
        - https://github.com/jackullrich/syscall-detect
        - hook the current process to identify the manual syscall executions on windows : https://github.com/paranoidninja/Process-Instrumentation-Syscall-Hook
    - process/pescans - yapscan/hoard as many yara rules as you can
    - etw  providers/Consumers -
        - silketw : https://otterhacker.github.io/Malware/ETW.html
        - ETWInspector : https://github.com/jsecurity101/ETWInspector
        - List ETW Providers for a process : https://github.com/whokilleddb/ETWListicle
    - kernel - elastic or sysmon
    - Capa - Capabilities Scanning
    - Trace API calls - TinyTracer
        - https://github.com/hasherezade/tiny_tracer
- Collect Windows Telemetry for Maldev
    - Collects telemetry like , ETW, ETW-TI, Kernel Callbacks, Hooks, Callstacks, Loaded DLLs, PEB) : https://github.com/dobin/RedEdr (Check other projects by author)
- **Free Trials EDR/AV**
    - Microsoft Defender For Endpoint
        - https://medium.com/@hackenbacker/creating-a-defender-for-endpoint-lab-for-free-695044b75bd6
        - https://learn.microsoft.com/en-us/defender-endpoint/defender-endpoint-trial-user-guide
    - Sophos XDR (trial)
    - Elastic EDR
        - https://github.com/sherifabdlnaby/elastdocker
        - [https://otterhacker.github.io/Malware/Elastic EDR.html](https://otterhacker.github.io/Malware/Elastic%20EDR.html)
        - https://github.com/peasead/elastic-container
        - https://www.youtube.com/watch?v=1luhjL7TN9U
    - TrendMicro
    - McAfee MVISION
    - Avast
    - openEDR - Comodo Free EDR
- Open Source EDRs
    - SimpleEDR - Manual DLL Hooking to find Detection Opportunity : https://github.com/Helixo32/SimpleEDR
    - CrimsonEDR : [https://github.com/Helixo32/CrimsonEDR](https://github.com/Helixo32/CrimsonEDR/tree/main)
    - https://sensepost.com/blog/2024/sensecon-23-from-windows-drivers-to-an-almost-fully-working-edr/
    - Write your own EDR
        - https://blog.whiteflag.io/blog/from-windows-drivers-to-a-almost-fully-working-edr/
        - https://youtube.com/playlist?list=PLc2_LEyTNutFkUliQMTZ_FHl8kNx3f5-E&si=8kHcC_FIxccHBR5H

- Process Memory Scanners
    - PE-sieve : https://github.com/hasherezade/pe-sieve
    - Moneta : https://github.com/forrest-orr/moneta
    - YapScan : https://github.com/fkie-cad/yapscan
    - MalMemDetect : https://github.com/waldo-irc/MalMemDetect
    - Patriot : https://github.com/joe-desimone/patriot
    - Hunt-Sleeping-Beacons : https://github.com/thefLink/Hunt-Sleeping-Beacons
    - YaraMemoryScanner : https://github.com/BinaryDefense/YaraMemoryScanner
    - Cobalt Strike Beacon Detection Specific Scanners
        - BeaconEye : https://github.com/CCob/BeaconEye
        - BeaconHunter : https://github.com/3lp4tr0n/BeaconHunter
    - EtwTi-FluctuationMonitor - Doing VirtualAlloc(RWX) changes CFG bitmap accordingly and then after VirtualAlloc(RW) CFG stays the same :  https://github.com/jdu2600/EtwTi-FluctuationMonitor

- Signature Detection Bypass
    - ThreatCheck : [https://github.com/PACHAKUTlQ/ThreatCheck](https://github.com/PACHAKUTlQ/ThreatCheck?tab=readme-ov-file)
    - AvRed : https://github.com/dobin/avred
