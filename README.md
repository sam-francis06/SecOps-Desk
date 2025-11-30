# SecOps Desk – Zoho Cliq SOC Assistant

SecOps Desk is a Zoho Cliq Security Operations Assistant designed to streamline security operations by providing threat scanning, cybersecurity news updates, CVE lookups, incident management, and SOC analytics inside Zoho Cliq.

This project was developed as part of the Zoho Cliqtrix competition, showcasing a complete SOC workflow built entirely using Zoho Cliq’s extension framework.

This extension integrates multiple industry-standard threat intelligence services including VirusTotal, AbuseIPDB, WhoisXML, MITRE CVE, and GNews.

<img width="1537" height="860" alt="image" src="https://github.com/user-attachments/assets/f6412c97-f6e7-4ad8-9d72-20505ea35bf0" />


## Features

### Threat Scanning (`/scan`)
Scan URLs, IP addresses, and domains. Returns:
- VirusTotal analysis results
- AbuseIPDB threat score
- Whois and geolocation information
- Direct intelligence links

### Cybersecurity News (`/cybernews`)
Retrieve recent cybersecurity headlines and summaries from trusted news sources.

### CVE Lookup (`/cve <id>`)
Fetch up-to-date vulnerability details from the MITRE CVE database, including:
- Vulnerability description
- Severity level
- CVSS score
- Reference links

### Incident Lookup (`/incident <id>`)
Access incident reports stored in the SecOps Desk internal database. Includes:
- Incident metadata
- Severity
- Description
- Assigned reporter
- Status and timestamps

### SOC Dashboard Widget
Provides real-time SOC analytics such as:
- Total number of incidents
- Severity distribution
- Recent incidents overview

---


## Project Structure

```
SecOpsDesk/
├── Bot/
│   └── SecOps Desk/
│       ├── Configuration.dg
│       ├── Message Handler.dg
│       └── Welcome handler.dg
│
├── Database/
│   └── SecOps Desk Incident Reports/
│       ├── fields.png
│       └── secopsdeskincidents.dg
│
├── Function/
│   └── report/
│       └── Form Submit Handler.dg
│
├── Slash Commands/
│   ├── cve/
│   │   └── Execution Handler.dg
│   ├── cybernews/
│   │   └── Execution Handler.dg
│   ├── incident/
│   │   └── Execution Handler.dg
│   └── scan/
│       └── Execution Handler.dg
│
├── Widget/
│   ├── All Reports Tab.png
│   ├── OverView Tab.png
│   └── SecOps Desk Incident.dg
│
└── README.md

```

---

## Installation

Install the extension using the installation link below:

**Installation Link:** [https://cliq.zoho.com/installapp.do?id=7592](https://cliq.zoho.com/installapp.do?id=7592)

### Required API Connections

Configure the following connections within the Zoho Cliq Developer Console after installation:
- VirusTotal
- AbuseIPDB
- WhoisXML
- GNews


---

## Usage Examples

```bash
/scan example.com
/cybernews
/cve CVE-2024-12345
/incident INC-20251114095722
```

---

## License

This project is licensed under the MIT License.

---

## Author

**Francis Samuvel**   
Developer of SecOps Desk
