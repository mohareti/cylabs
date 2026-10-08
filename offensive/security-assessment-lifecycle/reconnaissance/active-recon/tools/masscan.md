# Masscan

## Asset Scanning with Masscan

[Masscan](https://github.com/robertdavidgraham/masscan) is an ultra-fast, open-source TCP and UDP port scanner.

* **Basic TCP Scan:**

  ```text
  masscan -p1-65535 <target>
  ```
* **Basic UDP Scan:**

  ```text
  masscan -pU:1-65535 <target>
  ```
* **Rate-Limited Scan (e.g., 10 packets per second):**

  ```text
  masscan -p1-65535 --rate 10 <target>
  ```

For more options and configurations, consult the [Masscan documentation](https://github.com/robertdavidgraham/masscan#usage).
