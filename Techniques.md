# Comprehensive List of AV / EDR Evasion Techniques

---

## Execution & Initial Access Evasion

1. Executing payloads exclusively in memory
2. Avoiding disk writes entirely
3. Staging payloads in small memory chunks
4. Delayed execution using timers or sleep loops
5. Environment-aware execution (sandbox evasion)
6. Execution conditioned on user interaction
7. Time-based execution gating
8. Hardware fingerprint checks before execution
9. Execution only after system uptime threshold
10. Execution only when specific processes are running

---

## AppLocker & Application Control Evasion

11. DLL sideloading via trusted executables  
12. DLL search order hijacking  
13. Abuse of trusted installation directories  
14. Execution from allowed AppLocker paths  
15. Binary planting in writable trusted paths  
16. MSI execution abuse  
17. Script execution via trusted interpreters  
18. LOLBins executing code indirectly  
19. COM object execution bypass  
20. .NET assembly execution via trusted host  

---

## Trusted Path & Signed Binary Abuse

21. Abuse of signed Microsoft binaries  
22. Abuse of third-party signed binaries  
23. Proxy execution through trusted processes  
24. Parent process spoofing  
25. Masquerading executable names  
26. Execution from Program Files subdirectories  
27. Abuse of Windows Update directories  
28. Abuse of system maintenance folders  
29. Execution under trusted service context  
30. DLL loading via signed service binaries  

---

## In-Memory Loader Techniques

31. Reflective DLL injection  
32. Manual PE mapping  
33. Shellcode execution via function pointers  
34. Threadless execution techniques  
35. APC-based execution  
36. Fiber-based execution  
37. Callback-based execution  
38. Heap spraying with staged payloads  
39. Memory permission staging (RW → RX)  
40. Stack-based execution techniques  

---

## Process Injection & Manipulation

41. Classic remote process injection  
42. Process hollowing  
43. Process ghosting  
44. Process doppelgänging  
45. Transacted hollowing  
46. Early-bird APC injection  
47. Parent-child process abuse  
48. Injection into trusted system processes  
49. Section mapping injection  
50. Shared memory injection  

---

## AMSI & Script-Based Evasion

51. Script content obfuscation  
52. String fragmentation and reconstruction  
53. Runtime string decoding  
54. AMSI trigger avoidance  
55. Use of custom PowerShell runspaces  
56. Avoiding PowerShell.exe entirely  
57. Use of unmanaged code to bypass AMSI  
58. Inline execution without script files  
59. Scriptless .NET execution  
60. Abuse of alternate scripting engines  

---

## LOLBins (Living Off The Land Binaries)

61. Indirect execution via msbuild  
62. Code execution via installutil  
63. Execution via rundll32 with benign exports  
64. Execution via regsvr32  
65. WMI-based execution  
66. Scheduled task abuse  
67. Service-based execution  
68. Execution via COM hijacking  
69. Use of lesser-known LOLBins  
70. LOLBins chained with in-memory payloads  

---

## EDR Behavioral Evasion

71. Avoiding suspicious API call sequences  
72. Reducing API call frequency  
73. Introducing random execution jitter  
74. Avoiding common injection APIs  
75. Using uncommon execution primitives  
76. Mimicking legitimate application behavior  
77. Throttling malicious logic execution  
78. Splitting execution across threads  
79. Avoiding high-risk syscall patterns  
80. Adaptive execution based on telemetry  

---

## .NET & Managed Code Tradecraft

81. Assembly.Load from byte arrays  
82. Reflection-based method invocation  
83. Dynamic delegate creation  
84. Avoiding static entry points  
85. Runtime compilation of code  
86. Dynamic invocation via interfaces  
87. Managed-to-unmanaged transitions  
88. Mixed-mode execution techniques  
89. Avoiding known .NET loader patterns  
90. Memory-only managed payload execution  

---

## Syscalls & Low-Level Evasion

91. Direct syscalls to bypass hooks  
92. Indirect syscalls via unhooked stubs  
93. Syscall number resolution at runtime  
94. Avoiding static syscall tables  
95. Randomized syscall invocation order  
96. Unhooking user-mode APIs  
97. Bypassing EDR inline hooks  
98. Kernel transition minimization  
99. Leveraging native APIs directly  
100. Reducing overall kernel interaction footprint  
