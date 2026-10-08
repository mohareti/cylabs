# Ransomware: An Overview

**Definition:** Ransomware is a type of malicious software designed to block access to a computer system or data, typically by encrypting it, until a sum of money (ransom) is paid. It has become one of the most prevalent and dangerous cyber threats to both individuals and organizations worldwide.

## History of Ransomware

* **1989:** The first known ransomware, the AIDS Trojan, spread via floppy disks.
* **Early 2000s:** Ransomware gained traction with Gpcode, Cryzip, and MayArchive.
* **2013:** CryptoLocker emerged, a game-changer that used Bitcoin for payments.
* **2017:** WannaCry and NotPetya caused global disruptions, targeting vulnerabilities in Microsoft Windows.
* **Present:** Ransomware continues to evolve with advanced encryption algorithms and techniques to avoid detection.

## Types of Ransomware

* **Locker Ransomware:** Locks users out of their operating system, making it impossible to access their desktop and files.
* **Crypto Ransomware:** Encrypts valuable data like documents and photos without interfering with the basic computer functions.
* **Scareware:** Fake software that acts like an antivirus or a cleaning tool and claims to have found issues on your computer.
* **Doxware/Leakware:** Threatens to publish stolen information from your computer unless a ransom is paid.

## Crime Statistics

* **Ransom Payments:** The average payment has surged, with some demands in the millions.
* **Frequency:** An organization falls victim to ransomware every 14 seconds.
* **Costs:** Global damages from ransomware attacks are predicted to reach $20 billion.

**Programming Languages Used for Development:** Ransomware can be written in various programming languages, with some like C and C++ being traditional choices due to their power and control over system resources. Modern ransomware also uses languages like Go, Rust, and Python for their ease of use, efficiency, and ability to bypass security controls.

* **Go:** Preferred for its simplicity and efficient concurrency handling.
* **Rust:** Offers memory safety guarantees and is emerging in malware development.
* **Dlang, .NET, C#, Java, Objective-C:** These languages offer various features that can be exploited for malicious use.
* **Python, Perl, JavaScript, PowerShell:** Scripting languages that are often used for quick and effective ransomware development.
* **WebAssembly, Delphi:** Less common but are used for specific purposes in ransomware attacks.

## Stages and Techniques to Bypass Security Controls

1. **Infection:** The malware infects the system through phishing emails, exploit kits, or other vulnerabilities.
2. **Secure Communication:** Establishes communication with the command-and-control server, often using TOR or other anonymizing services.
3. **Encryption:** Files are encrypted using asymmetric encryption methods. Advanced ransomware employs techniques like encryption layering and intermittent encryption.
4. **Persistence:** Ensures that the ransomware survives reboots and remains undetected, often by modifying registry keys or scheduled tasks.
5. **Payment Demand:** A ransom note is displayed, demanding payment in cryptocurrencies.
6. **Data Exfiltration:** Some ransomware variants exfiltrate data to the attackers, threatening to release it if the ransom is not paid.

## Techniques to Bypass Security Controls

* **Polymorphic Code:** Changes its signature every time it runs to avoid signature-based detection.
* **Fileless Ransomware:** Operates in memory without writing files to the disk, evading traditional file scanning.
* **Encryption of Backup:** Targets and encrypts backup files to prevent recovery.
* **Use of Legitimate Tools:** Utilizes tools like PowerShell, WMI, and PsExec for lateral movement and to remain under the radar.
* **Exploiting Zero-day Vulnerabilities:** Uses unpatched vulnerabilities in software to gain access to systems.

**Reverse Engineering Challenges:** Languages like C++, Rust, and Go can create binary executables that are difficult to reverse-engineer due to optimizations and lack of metadata. Analyzing ELF files (Unix/Linux) and PE files (Windows) requires expertise in understanding low-level code and the Win32 API, which provides a large number of functions for Windows applications.

The continued evolution of ransomware necessitates strong cybersecurity measures, including regular backups, employee education, and robust security solutions. It's crucial to have an incident response plan in place to mitigate the impact of ransomware attacks.
