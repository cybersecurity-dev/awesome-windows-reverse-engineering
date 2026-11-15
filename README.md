<img width="4032" height="547" alt="image" src="https://github.com/user-attachments/assets/6bb7aaa8-43de-4f3b-ab38-ddfb4bca043b" /><div align="center">
    <p align="center">
        <a href="">
          <img width="25%" src="https://github.com/cybersecurity-dev/cybersecurity-dev/blob/main/assets/Windows.svg" />
        </a>
    </p>

```mermaid
flowchart LR
    ROOT["Windows Reverse Engineering Tools"]

    ROOT --> TRIAGE
    ROOT --> CODE
    ROOT --> RUNTIME
    ROOT --> INSTR
    ROOT --> PATCH

    subgraph TRIAGE_G["1. PE and File Inspection"]
        direction TB
        TRIAGE["File Identification<br/>Detect It Easy, PEStudio, TrID<br/>strings, sigcheck, Get-FileHash"]
        TRIAGE --> PE["PE Structure<br/>PE-bear, CFF Explorer, PEview<br/>dumpbin, Dependencies, pestudio"]
        PE --> HEX["Resources and Hex<br/>Resource Hacker, HxD<br/>ImHex, 010 Editor"]
    end

    subgraph CODE_G["2. Disassembly and Decompilation"]
        direction TB
        CODE["Disassemblers<br/>Ghidra, IDA Free, Binary Ninja<br/>radare2, Cutter, REDasm"]
        CODE --> DECOMP["Decompilers<br/>Ghidra, Hex-Rays, Binary Ninja<br/>RetDec, Snowman, dnSpyEx"]
        DECOMP --> MANAGED["Managed Code<br/>dnSpyEx, ILSpy, dotPeek<br/>de4dot, ildasm"]
    end

    subgraph RUNTIME_G["3. Debugging and Monitoring"]
        direction TB
        RUNTIME["Debuggers<br/>x64dbg, WinDbg, WinDbg Preview<br/>IDA debugger, Visual Studio"]
        RUNTIME --> MONITOR["Process and API Monitoring<br/>Process Monitor, Process Explorer<br/>API Monitor, WinAPIOverride"]
        MONITOR --> TRACE["Tracing and Profiling<br/>ETW, WPA, WPR<br/>TTD, Frida, Intel VTune"]
    end

    subgraph INSTR_G["4. Instrumentation and Memory"]
        direction TB
        INSTR["Dynamic Instrumentation<br/>Frida, DynamoRIO, Intel Pin<br/>Qiling, Unicorn, Speakeasy"]
        INSTR --> MEMORY["Memory Analysis<br/>Volatility 3, WinDbg<br/>PE-sieve, Moneta, HollowsHunter"]
        MEMORY --> SANDBOX["Sandbox and Behavior<br/>Windows Sandbox, FLARE-VM<br/>CAPE Sandbox, FakeNet-NG"]
    end

    subgraph PATCH_G["5. Editing and Patching"]
        direction TB
        PATCH["Binary Patching<br/>x64dbg, Ghidra, IDA<br/>Binary Ninja, Cutter"]
        PATCH --> PEEDIT["PE Modification<br/>CFF Explorer, PE-bear<br/>LIEF, Resource Hacker"]
        PEEDIT --> REPORT["Graphing and Documentation<br/>Ghidra graphs, IDA graphs<br/>Graphviz, Mermaid, Markdown"]
    end

    TRIAGE -.-> CODE
    TRIAGE -.-> RUNTIME
    CODE -.-> RUNTIME
    RUNTIME -.-> INSTR
    CODE -.-> PATCH
    INSTR -.-> PATCH

    classDef root fill:#102a43,stroke:#32d5ff,color:#ffffff,stroke-width:3px
    classDef triage fill:#25364a,stroke:#75a7d8,color:#ffffff,stroke-width:2px
    classDef code fill:#10334a,stroke:#32d5ff,color:#ffffff,stroke-width:2px
    classDef runtime fill:#261d4d,stroke:#9a72ff,color:#ffffff,stroke-width:2px
    classDef instr fill:#153b35,stroke:#45e0b7,color:#ffffff,stroke-width:2px
    classDef patch fill:#493218,stroke:#ffb454,color:#ffffff,stroke-width:2px

    class ROOT root
    class TRIAGE,PE,HEX triage
    class CODE,DECOMP,MANAGED code
    class RUNTIME,MONITOR,TRACE runtime
    class INSTR,MEMORY,SANDBOX instr
    class PATCH,PEEDIT,REPORT patch
```
# **`Awesome`** [Windows](https://wikipedia.org/wiki/Machine_code) [Reverse](https://www.apriorit.com/dev-blog/366-software-reverse-engineering-tools) [Engineering](https://wiki.installgentoo.com/wiki/Reverse_Engineering) [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
</div>

[![Windows](https://custom-icon-badges.demolab.com/badge/Windows-0078D6?style=for-the-badge&logo=windows11&logoColor=white)]()
[![YouTube](https://img.shields.io/badge/YouTube-%23FF0000.svg?style=for-the-badge&logo=YouTube&logoColor=white)](https://youtube.com/playlist?list=PL9V4Zu3RroiX0PgH9Ahf1wueyGiGprAz7&si=JDxNLcyRYyALGU7B)
[![Reddit](https://img.shields.io/badge/Reddit-FF4500?style=for-the-badge&logo=reddit&logoColor=white)](https://www.reddit.com/r/ReverseEngineering/new/)

<p align="center">
    <a href="https://github.com/cybersecurity-dev/"><img height="25" src="https://github.com/cybersecurity-dev/cybersecurity-dev/blob/main/assets/github.svg" alt="GitHub"></a>
    &nbsp;
    <a href="https://www.youtube.com/@CyberThreatDefense"><img height="25" src="https://github.com/cybersecurity-dev/cybersecurity-dev/blob/main/assets/youtube.svg" alt="YouTube"></a>
    &nbsp;
    <a href="https://cyberthreatdefence.com/my_awesome_lists"><img height="20" src="https://github.com/cybersecurity-dev/cybersecurity-dev/blob/main/assets/blog.svg" alt="My Awesome Lists"></a>
    <img src="https://github.com/cybersecurity-dev/cybersecurity-dev/blob/main/assets/bar.gif">
</p>

```mermaid
flowchart TB
    ROOT["Windows Reverse Engineering Tool Types"]

    ROOT --> INSPECT["PE and File Inspection<br/>PE-bear, CFF Explorer, PEStudio<br/>Detect It Easy, strings, sigcheck"]
    ROOT --> DISASM["Disassemblers<br/>Ghidra, IDA Free, Binary Ninja<br/>radare2, Cutter, Capstone"]
    ROOT --> DECOMP["Decompilers<br/>Ghidra, Hex-Rays, Binary Ninja<br/>RetDec, Snowman, dnSpyEx"]
    ROOT --> DEBUG["Debuggers<br/>x64dbg, WinDbg, GDB<br/>IDA debugger, Immunity Debugger"]
    ROOT --> TRACE["Tracing and Monitoring<br/>Process Monitor, Process Explorer<br/>API Monitor, ETW, WPA"]
    ROOT --> MEMORY["Memory and Forensics<br/>Volatility 3, WinDbg<br/>PE-sieve, Moneta, HollowsHunter"]
    ROOT --> INSTR["Instrumentation and Emulation<br/>Frida, DynamoRIO, Intel Pin<br/>Qiling, Unicorn, Speakeasy"]
    ROOT --> EDIT["Hex Editing and Patching<br/>HxD, ImHex, 010 Editor<br/>CFF Explorer, PE-bear, LIEF"]

    classDef root fill:#102a43,stroke:#32d5ff,color:#ffffff,stroke-width:3px
    classDef blue fill:#10334a,stroke:#32d5ff,color:#ffffff,stroke-width:2px
    classDef green fill:#123b3c,stroke:#45e0b7,color:#ffffff,stroke-width:2px
    classDef purple fill:#261d4d,stroke:#9a72ff,color:#ffffff,stroke-width:2px
    classDef orange fill:#493218,stroke:#ffb454,color:#ffffff,stroke-width:2px

    class ROOT root
    class INSPECT,DISASM blue
    class DECOMP,INSTR green
    class DEBUG,TRACE purple
    class MEMORY,EDIT orange
```

## 📖 Contents
- [Datasets](#datasets)
- [Scientific Research](#scientific-research)
- [My Other Awesome Lists](#my-other-awesome-lists)
- [Contributing](#contributing)
- [Contributors](#contributors)

## Tools

### [Disassembler](https://wikipedia.org/wiki/Disassembler) Tools
A disassembler is a computer program that translates machine language into assembly language

### [Decompiler](https://wikipedia.org/wiki/Decompiler) Tools
A decompiler is a computer program that translates an executable file back into high-level source code. 

### [Debugging](https://wikipedia.org/wiki/Debugger) Tools
A debugger is a computer program used to test and debug other programs (the "target" programs).

## Training
* [Reverse Engineering 101](https://malwareunicorn.org/workshops/re101.html)
* [Reverse Engineering 102](https://malwareunicorn.org/workshops/re102.html)
* [Malware Reverse Engineering for Beginners](https://intezer.com/blog/malware-reverse-engineering-beginners/)

##

### Datasets
You can access the datasets [here](https://github.com/cybersecurity-dev/awesome-malware-datasets?tab=readme-ov-file#windows).

### Scientific Research
You can access the Scientific Research [here](https://github.com/cybersecurity-dev/awesome-static-windows-malware-analysis-scientific-research).

### My Other Awesome Lists
You can access the my other awesome lists [here](https://cyberthreatdefence.com/my_awesome_lists)

### Contributing
[Contributions of any kind welcome, just follow the guidelines](contributing.md)!

### Contributors
[Thanks goes to these contributors](https://github.com/cybersecurity-dev/awesome-windows-reverse-engineering/graphs/contributors)!

### License
[![CC0](http://mirrors.creativecommons.org/presskit/buttons/88x31/svg/cc-zero.svg)](http://creativecommons.org/publicdomain/zero/1.0)

[🔼 Back to top](#awesome-windows-reverse-engineering-)

