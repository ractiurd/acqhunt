# 🇵🇸 Stand With Palestine

![Palestinian Flag](https://img.freepik.com/premium-photo/child-holding-palestinian-flag-front-destroyed-building_988987-10735.jpg)

The situation in Palestine remains critical, with countless innocent lives affected by ongoing violence and oppression. As global citizens, it's our responsibility to speak up, spread awareness, and support justice and human rights.

Let us pray (make dua) for the people of Palestine and commit ourselves to advocating for peace and dignity for all.

---

# AcqHunt - Domain Acquisition Discovery Tool

**AcqHunt** is a powerful command-line reconnaissance tool for discovering domains and related assets tied to organizations, IP ranges, ASN numbers, and more. Built for cybersecurity professionals, researchers, and digital investigators, AcqHunt aggregates intelligence from multiple sources to provide deep acquisition visibility.

## 🔍 Key Features

- **Domain Lookup**: `-d` – Search by domain name.
- **Organization Lookup**: `-org` – Discover domains associated with a specific organization.
- **IP Range Scan**: `-ip` – Query CIDR-based IP ranges for domain associations.
- **ASN Scan**: `-a` – Retrieve domains tied to a specific Autonomous System Number.

### 🧠 Data Source Integrations

- `-c` – Pull certificate data from **crt.sh** (by domain).
- `-oc` – Pull organization-wide certificate data from **crt.sh**.
- `-i` – Query **website.informer.com** for related domain info.
- `-w` – Run **reverse WHOIS** lookup for domain ownership links.
- `-b` – Query the **BigDomainData API** for additional acquisition data.

### 💾 Output Options

- `-o` – Save output to a file of your choice for future analysis.

## ⚙️ Usage Examples

```bash
acqhunt -d example.com -c -w -b        # Full domain investigation
acqhunt -org "Google LLC" -oc          # Organization certificate discovery
acqhunt -ip 192.168.1.0/24             # Domain enumeration by IP range
acqhunt -a AS15169                     # Domain discovery via ASN
```
## 📦 Installation

### Option 1: Install via Go

To install AcqHunt using Go, run the following command:

```bash
go install github.com/ractiurd/acqhunt@latest
```
This will install the latest version and place the binary in your $GOPATH/bin directory. Make sure that directory is in your system’s PATH.

### Option 2: Manual Installation

If you prefer to install AcqHunt manually, follow these steps:

```bash
# Clone the repository
git clone https://github.com/ractiurd/acqhunt.git

# Navigate into the project directory
cd acqhunt

# Build the binary
go build

# Move the binary to a location in your system PATH
sudo mv acqhunt /usr/bin/
```
After installation, verify it's working:
```bash
acqhunt -h
```


## 🧰 Prerequisites

Before using AcqHunt, ensure the following tools and API keys are set up:

- **Whois Utility**
  - Required for domain and registrant lookups.
  - Install it with:
    ```bash
    sudo apt install whois -y
    ```

- **Reverse WHOIS API Key**
  - Needed for using the `-w` flag (Reverse WHOIS lookup).
  - You can get a key from: [WhoisXML API - Reverse WHOIS](https://reverse-whois.whoisxmlapi.com/)

- **BigDomainData API Key**
  - Required for the `-b` flag to query domain acquisition data.
  - Grab your API key from: [BigDomainData](https://www.bigdomaindata.com/)
 
## 🔐 Licensing

AcqHunt is completely **free to use** with no trial limitations.

You are welcome to use, share, and contribute to the project under the terms of its open usage model.

For questions, contributions, or support, feel free to contact the author:

- Twitter/X: https://x.com/ractiurd
- Facebook: https://facebook.com/ractiurd
## ⚠️ Disclaimer

AcqHunt is intended for ethical and educational use only. 

Please ensure you have proper authorization before scanning, querying, or collecting data on any domains, organizations, IP addresses, or ASNs.

The author is not responsible for any misuse of this tool.
