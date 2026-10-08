---
description: "Enhancing security on Azure is a critical task that requires the right set of tools."
---

# Azure Security Assessment Tools: Installation and Usage

Enhancing security on Azure is a critical task that requires the right set of tools. This blog post provides a comprehensive guide on installing and using some of the most effective Azure security tools available.

**1. MicroBurst** *Installation:*

```shell
git clone https://github.com/NetSPI/MicroBurst.git
Import-Module ./MicroBurst/MicroBurst.psd1
```

*Usage:* Navigate to the MicroBurst directory and execute scripts based on your requirements.

**2. Lava** *Installation:*

```shell
# Assuming Lava is a Python-based tool
pip install lava-tool
```

*Usage:*

```shell
lava --scan --target azure_subscription_id
```

**3. Koboko** *Installation:*

```shell
# If Koboko is hosted on a Git repository
git clone https://github.com/company/koboko.git
cd koboko
./install.sh
```

*Usage:*

```shell
koboko --target-url <target azure service>
```

**4. PowerZure** *Installation:*

```shell
git clone https://github.com/hausec/PowerZure.git
Import-Module ./PowerZure/PowerZure.ps1
```

*Usage:*

```powershell
Invoke-PowerZureFunction -FunctionName
```

**5. Stormspotter** *Installation:*

```shell
git clone https://github.com/Azure/Stormspotter.git
cd Stormspotter
python setup.py install
```

*Usage:*

```shell
stormspotter --collect
```

**6. BloodHound** *Installation:*

```shell
# For Neo4j
wget -O - https://debian.neo4j.com/neotechnology.gpg.key | sudo apt-key add -
sudo add-apt-repository "deb https://debian.neo4j.com stable 4.0"
sudo apt-get update
sudo apt-get install neo4j
# For BloodHound
git clone https://github.com/BloodHoundAD/BloodHound.git
cd BloodHound
npm install
npm run linuxbuild
```

*Usage:*

```shell
neo4j console
# Open BloodHound with the interface
```

**7. cloud\_enum** *Installation:*

```shell
git clone https://github.com/initstring/cloud_enum.git
cd cloud_enum
pip install -r requirements.txt
```

*Usage:*

```shell
python cloud_enum.py --keyword companyname
```

**8. AADInternals** *Installation:*

```powershell
Install-Module -Name AADInternals
```

*Usage:*

```powershell
Connect-AADInt
```

**9. ScoutSuite** *Installation:*

```shell
pip install scoutsuite
```

*Usage:*

```shell
scout azure --cli
```

**10. Prowler** *Installation:*

```shell
git clone https://github.com/toniblyx/prowler.git
cd prowler
```

*Usage:*

```shell
./prowler -g group_name
```

**11. Roadtools** *Installation:*

```shell
pip install roadtools roadrecon
```

*Usage:*

```shell
roadrecon
```

*Conclusion:* Following the installation and usage instructions for each tool will help enhance your Azure environment's security. Remember, it's crucial to keep these tools up to date and run them regularly to maintain a strong security posture.

.
