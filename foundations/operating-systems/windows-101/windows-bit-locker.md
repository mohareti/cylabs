# Windows Bit Locker

## What is BitLocker?

* **Full Disk Encryption:** BitLocker is a built-in Windows feature (available in Pro, Enterprise, and Education editions) designed to protect data on lost, stolen, or improperly decommissioned devices, using robust encryption.
* **Transparent Operation:** When BitLocker is enabled, data is encrypted as it's written to the disk and decrypted on-the-fly for authorized users – without a noticeable performance impact.
* **TPM Integration:** BitLocker works best in conjunction with a Trusted Platform Module (TPM) – a hardware chip on many computers that provides secure storage for encryption keys.

## How to Configure BitLocker

1. **Enable BitLocker:**
   * **Search:** Search for "Manage BitLocker” and open the Control Panel tool.
   * **Selection:** Choose the drive you want to encrypt.
   * **Turn on BitLocker:** Follow the on-screen instructions.
2. **Choose an Unlock Method:**
   * **TPM Only:** The most common, storing the key in the TPM.
   * **Password:** Requires a password each time you boot.
   * **USB Drive:** Requires inserting a USB flash drive with the stored key.
   * **Combination:** A combination of the methods above for higher security.
3. **Backup Recovery Key:**
   * **Crucial Step:** Store your recovery key securely (print, save on a separate flash drive, etc.). This key allows you to access your data if you lose your password or the TPM malfunctions.

## Additional Configuration Settings

* **Encryption Algorithm:** Choose between AES-128 or AES-256 (Manage BitLocker -> "Change encryption method and cipher strength").
* **Fixed Data Drive Encryption:** Enable encryption for non-removable drives.
* **Pre-boot Authentication:** (Advanced) Requires a PIN or other authentication before the operating system boots.

## BitLocker and Threat Hunting

* **Data at Rest Protection:** BitLocker makes it much harder for unauthorized individuals to access sensitive data, even if the physical drive is obtained. This is invaluable during forensic investigations.
* **Incident Response:** In the case of a lost or stolen device, BitLocker helps protect data from unauthorized access.
* **Compliance:** BitLocker can help with complying with data security regulations that require encryption.

## Considerations

* **Performance impact:** Minimal on modern systems.
* **TPM Requirement:** BitLocker's strongest security mode usually requires a TPM.
* **Data recovery:** Failing to back up your recovery key can lead to permanent data loss.

## Let's Go Deeper

* How to manage BitLocker via PowerShell or command line
* How BitLocker works at a technical level (encryption modes, etc.)
* Threat hunting scenarios where BitLocker's presence or absence plays a role
