# Windows system calls

## What are Windows System Calls?

* **The Gateway to the Kernel:** System calls are the primary way user-mode programs interact with the Windows kernel to request system-level services. These services include:
  * File and process management (creation, reading, writing)
  * Memory allocation and manipulation
  * Network communication
  * Device interaction

## Why System Calls are Targets for Abuse

* **Beneath the Radar:** Malware often uses system calls to perform malicious activities in ways that might be difficult to detect or analyze. Examples:
  * Creating new processes to inject malicious code.
  * Opening files to steal or delete sensitive data.
  * Establishing network connections to send stolen data or receive commands.

## Key System Calls for Reverse Engineers

Understanding these system call families is crucial for unraveling how a piece of software or malware operates at the lower level:

* **Process and Thread Management:**
  * `NtCreateProcess`, `NtOpenProcess`: Process creation and manipulation.
  * `NtCreateThread`, `NtResumeThread`: For manipulating threads within processes.
* **File I/O:**
  * `NtCreateFile`, `NtOpenFile`: Opening and creating files.
  * `NtReadFile`, `NtWriteFile`: Reading and writing data to files.
* **Memory Management:**
  * `NtAllocateVirtualMemory`: Allocates virtual memory.
  * `NtProtectVirtualMemory`: Modifies memory access permissions.
* **Network Communication:**
  * `NtCreateSocket`, `NtConnect`: Creating and managing network sockets.
  * `NtSend`, `NtRecv`: Transmit and receive network data.
* **Windows Registry:**
  * `NtCreateKey`, `NtOpenKey`: Creates or opens registry keys.
  * `NtSetValueKey`, `NtQueryValueKey`: Sets or retrieves registry values.

## Reverse Engineering Methods

* **Static Analysis:** Examine the disassembled code of a binary to identify the system calls it uses, even if they are obfuscated. Tools like IDA Pro are helpful here.
* **Dynamic Analysis:** Monitor system call activity of a program as it runs, using tools like:
  * **Sysinternals Process Monitor:** Gives a detailed view of all system calls in real-time.
  * **API Monitor:** Helps trace function calls within Windows programs.

## Important Considerations

* **System calls change across Windows versions:** Be aware of API differences between Windows XP, Windows 7, Windows 10, etc.
* **Malware Obfuscation:** Malware can try to hide or disguise system call usage.
