<div align="center">
  <h1>Rosetta Launch Failure</h1>
  <p>How to fix a rather annoying Rosetta launch failure on Macintosh systems.</p>
  <div>
    <a href="#the-explanation">The Explanation</a>
    <span>&nbsp;&nbsp;&nbsp;-&nbsp;&nbsp;&nbsp;</span>
    <a href="#the-error">The Error</a>
    <span>&nbsp;&nbsp;&nbsp;-&nbsp;&nbsp;&nbsp;</span>
    <a href="#the-fix">The Fix</a>
  </div>
</div>

------

## The Explanation

Recently, I downgraded from the Mac OS Ventura Beta 6 to the stable production-release version of Mac OS Monteray by using Time Machine, which is Apple's built-in backup utility toolkit. Time Machine will try to pick out, identify, and lay out any software that doesn't successfully port over to the version of Mac OS now on the system, although Rosetta seems to have silently failed. 

As a result, all applications running using Rosetta would fail with an error such as what follows. 

## The Error

```
-------------------------------------
Translated Report (Full Report Below)
-------------------------------------

Incident Identifier: 88275FFA-FD1A-4B82-A475-67DE85775A03
CrashReporter Key:   398F4766-7DA0-6A4D-7127-B64C0B96C2CF
Hardware Model:      MacBookPro18,1
Process:             Installer [39234]
Path:                /System/Library/CoreServices/Installer.app/Contents/MacOS/Installer
Identifier:          com.apple.installer
Version:             6.2.0 (1118)
Code Type:           X86-64 (Native)
Role:                Foreground
Parent Process:      launchd [1]
Coalition:           com.apple.installer [64752]

Date/Time:           2022-09-06 12:08:38.4931 -0600
Launch Time:         2022-09-06 12:08:27.1270 -0600
OS Version:          macOS 12.5.1 (21G83)
Release Type:        User
Report Version:      104

Exception Type:  EXC_BREAKPOINT (SIGTRAP)
Exception Codes: 0x0000000000000001, 0x00007ff7fff719b0
Exception Note:  EXC_CORPSE_NOTIFY
Termination Reason: SIGNAL 5 Trace/BPT trap: 5
Terminating Process: exc handler [39234]

Triggered by Thread:  0

Thread 0 Crashed:
0   runtime                       	    0x7ff7fff719b0 0x7ff7fff54000 + 121264
1   runtime                       	    0x7ff7fff71394 0x7ff7fff54000 + 119700
2   runtime                       	    0x7ff7fff690c4 0x7ff7fff54000 + 86212
3   runtime                       	    0x7ff7fff57ae0 0x7ff7fff54000 + 15072
4   dyld                          	       0x200dd4000 ???


Thread 0 crashed with ARM Thread State (64-bit):
    x0: 0x0000000000000000   x1: 0x0000000000000003   x2: 0x000000000000003c   x3: 0x000000000000002c
    x4: 0x0000000000000303   x5: 0x0000000000000000   x6: 0x0000000000000000   x7: 0x00000000000003e0
    x8: 0x00007ff7fff8f000   x9: 0x0000000000000000  x10: 0x0000000000000000  x11: 0x00007ff7fff8f8f4
   x12: 0x0000000000000000  x13: 0x0000000000000039  x14: 0x00007ff7fff8f7a8  x15: 0x00007ff7fff77818
   x16: 0xffffffffffffffe1  x17: 0x00007ff7fff806e1  x18: 0x0000000305af7fbb  x19: 0x00007ff7fff852e1
   x20: 0x00007ff7fff7fba2  x21: 0x0000000000000063  x22: 0x00007ff7fff7fb96  x23: 0x0000000305af6f20
   x24: 0x0000000108ccf2e0  x25: 0x0000000000000248  x26: 0x0000000000000009  x27: 0x0000000200e541b8
   x28: 0x0000000000000001   fp: 0x0000000305af6ee0   lr: 0x00007ff7fff719a8
    sp: 0x0000000305af6ec0   pc: 0x00007ff7fff719b0 cpsr: 0x60001000
   far: 0x0000000305af6f18  esr: 0xf2000001 (Breakpoint) brk 1

Binary Images:
    0x7ff7fff54000 -     0x7ff7fff83fff runtime (*) <ef33add1-6b70-3cc9-8bbc-c8544b609d2b> /usr/libexec/rosetta/runtime
       0x200dd4000 -        0x200e3ffff dyld (*) <f71fb3ca-5fcc-3577-9457-b047888a46d1> /usr/lib/dyld

Error Formulating Crash Report:
dyld_process_snapshot_get_shared_cache failed

EOF

-----------
Full Report
-----------

{"app_name":"Installer","timestamp":"2022-09-06 12:08:38.00 -0600","app_version":"6.2.0","slice_uuid":"9383026d-bc76-33f2-b2cf-2d28a96aa3d3","build_version":"1118","platform":0,"bundleID":"com.apple.installer","share_with_app_devs":0,"is_first_party":1,"bug_type":"309","os_version":"macOS 12.5.1 (21G83)","incident_id":"88275FFA-FD1A-4B82-A475-67DE85775A03","name":"Installer"}
{
  "uptime" : 41000,
  "procLaunch" : "2022-09-06 12:08:27.1270 -0600",
  "procRole" : "Foreground",
  "version" : 2,
  "userID" : 501,
  "deployVersion" : 210,
  "modelCode" : "MacBookPro18,1",
  "procStartAbsTime" : 1005137341452,
  "coalitionID" : 64752,
  "osVersion" : {
    "train" : "macOS 12.5.1",
    "build" : "21G83",
    "releaseType" : "User"
  },
  "captureTime" : "2022-09-06 12:08:38.4931 -0600",
  "incident" : "88275FFA-FD1A-4B82-A475-67DE85775A03",
  "bug_type" : "309",
  "pid" : 39234,
  "procExitAbsTime" : 1005409294422,
  "translated" : true,
  "cpuType" : "X86-64",
  "procName" : "Installer",
  "procPath" : "\/System\/Library\/CoreServices\/Installer.app\/Contents\/MacOS\/Installer",
  "bundleInfo" : {"CFBundleShortVersionString":"6.2.0","CFBundleVersion":"1118","CFBundleIdentifier":"com.apple.installer"},
  "buildInfo" : {"ProjectName":"Installer","SourceVersion":"1118000000000000","BuildVersion":"292"},
  "storeInfo" : {"deviceIdentifierForVendor":"8C94DAB8-38C4-5002-925C-02693783F9CF"},
  "parentProc" : "launchd",
  "parentPid" : 1,
  "coalitionName" : "com.apple.installer",
  "crashReporterKey" : "398F4766-7DA0-6A4D-7127-B64C0B96C2CF",
  "sleepWakeUUID" : "599433FF-4EA9-4CAF-8B9A-8A4336A30439",
  "sip" : "enabled",
  "isCorpse" : 1,
  "exception" : {"codes":"0x0000000000000001, 0x00007ff7fff719b0","rawCodes":[1,140703128033712],"type":"EXC_BREAKPOINT","signal":"SIGTRAP"},
  "termination" : {"flags":0,"code":5,"namespace":"SIGNAL","indicator":"Trace\/BPT trap: 5","byProc":"exc handler","byPid":39234},
  "extMods" : {"caller":{"thread_create":0,"thread_set_state":0,"task_for_pid":0},"system":{"thread_create":0,"thread_set_state":0,"task_for_pid":0},"targeted":{"thread_create":0,"thread_set_state":0,"task_for_pid":0},"warnings":0},
  "faultingThread" : 0,
  "threads" : [{"triggered":true,"id":485913,"threadState":{"x":[{"value":0},{"value":3},{"value":60},{"value":44},{"value":771},{"value":0},{"value":0},{"value":992},{"value":140703128154112},{"value":0},{"value":0},{"value":140703128156404,"symbolLocation":140,"symbol":"__crashreporter_info__"},{"value":0},{"value":57},{"value":140703128156072},{"value":140703128057880},{"value":18446744073709551585},{"value":140703128094433},{"value":12980289467},{"value":140703128113889},{"value":140703128091554},{"value":99},{"value":140703128091542},{"value":12980285216},{"value":4442616544},{"value":584},{"value":9},{"value":8604959160,"symbolLocation":0,"symbol":"dyld_all_image_infos"},{"value":1}],"flavor":"ARM_THREAD_STATE64","lr":{"value":140703128033704},"cpsr":{"value":1610616832},"fp":{"value":12980285152},"sp":{"value":12980285120},"esr":{"value":4060086273,"description":"(Breakpoint) brk 1"},"pc":{"value":140703128033712,"matchesCrashFrame":1},"far":{"value":12980285208}},"frames":[{"imageOffset":121264,"imageIndex":0},{"imageOffset":119700,"imageIndex":0},{"imageOffset":86212,"imageIndex":0},{"imageOffset":15072,"imageIndex":0},{"imageOffset":0,"imageIndex":1}]}],
  "usedImages" : [
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 140703127912448,
    "size" : 196608,
    "uuid" : "ef33add1-6b70-3cc9-8bbc-c8544b609d2b",
    "path" : "\/usr\/libexec\/rosetta\/runtime",
    "name" : "runtime"
  },
  {
    "source" : "P",
    "arch" : "x86_64",
    "base" : 8604434432,
    "size" : 442368,
    "uuid" : "[REDACTED]",
    "path" : "\/usr\/lib\/dyld",
    "name" : "dyld"
  }
],
  "vmSummary" : "ReadOnly portion of Libraries: Total=840K resident=0K(0%) swapped_out_or_unallocated=840K(100%)\nWritable regions: Total=136.1M written=0K(0%) resident=0K(0%) swapped_out=0K(0%) unallocated=136.1M(100%)\n\n                                   VIRTUAL   REGION \nREGION TYPE                           SIZE    COUNT (non-coalesced) \n===========                        =======  ======= \nRosetta Generic                         8K        2 \nRosetta IndirectBranch (reserved)      32K        1         reserved VM address space (unallocated)\nRosetta JIT                         128.0M        1 \nSTACK GUARD                          56.0M        1 \nStack                                8176K        1 \nVM_ALLOCATE (reserved)                 24K        2         reserved VM address space (unallocated)\n__DATA                                 80K        3 \n__DATA_CONST                           80K        1 \n__LINKEDIT                            240K        4 \n__TEXT                                624K        2 \nmapped file                           696K        7 \n===========                        =======  ======= \nTOTAL                               193.7M       25 \nTOTAL, minus reserved VM space      193.7M       25 \n",
  "legacyInfo" : {
  "threadTriggered" : {

  }
},
  "trialInfo" : {
  "rollouts" : [
    {
      "rolloutId" : "61fd92db295c182621ececc3",
      "factorPackIds" : {
        "SIRI_DIALOG_ASSETS" : "62fee155c3d531115200431b"
      },
      "deploymentId" : 250000135
    },
    {
      "rolloutId" : "60f8ddccefea4203d95cbeef",
      "factorPackIds" : {

      },
      "deploymentId" : 250000018
    }
  ],
  "experiments" : [

  ]
},
  "reportNotes" : [
  "dyld_process_snapshot_get_shared_cache failed"
]
}
```

It's not the most helpful error message, and I see it cited multiple times all over the internet with no fixes available. The error message is enough to know that the issue is with Rosetta, and judging by the fact that this started once I rolled back Mac OS versions, it's likely due to a non-reverse compatible change pertaining to Rosetta in Mac OS Ventura.

## The Fix

You can re-install Rosetta as follows.

1. Turn off your Macintosh.
2. Press and hold the power button until booted into Recovery Mode.
3. Select `Options` > `Continue`.
4. On the top of the screen, click the "Utilities" and select "Terminal"
5. Type `csrutil disable` to disable SIP.
6. Enter your administrator password to complete disabling SIP.
7. Restart your device, and boot into Mac OS.
8. Launch the `Terminal` application.
9. Type in the following command.
  ```
  rm -rf /Library/Apple/usr/lib/libRosettaAot.dylib
  rm -rf /Library/Apple/usr/libexec
  rm -rf /Library/Apple/usr/share/rosetta
  ```
10. Boot back into Recovery Mode, and enter the Terminal once again.
  - See steps 1-4.
11. Re-enable SIP by typing into `csrutil enable`. 
12. Reboot into Mac OS. 
13. Launch any Rosetta Application.
14. Follow the prompts to install Rosetta. 
15. Profit!
