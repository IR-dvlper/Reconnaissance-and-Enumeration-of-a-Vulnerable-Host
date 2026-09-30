# Reconnaissance-and-Enumeration-of-a-Vulnerable-Host
A black-box reconnaissance and vulnerability assessment exercise against Metasploitable 2, an intentionally vulnerable VM, conducted from Kali Linux in an isolated VirtualBox lab. Demonstrates the early stages of the Penetration Testing Execution Standard (PTES) — intelligence gathering, enumeration, and vulnerability analysis.

---

## Objective
To simulate the reconnaissance and enumeration stages and a vulnerability assessment on a deliberately vulnerable host, identify and analyse real CVEs affecting the discovered services, highlighting the potential consequences they present and document how organisations could mitigate the risks found. This demonstrates the process a cyber security risk analyst might follow when assessing an organisation's systems.

## Tools Used

| Tool | Purpose |
|---|---|
| VirtualBox | Isolated lab environment |
| Metasploitable 2 | Target host |
| Kali Linux | Attacking machine |
| Nmap | Port scanning, service version detection, NSE vulnerability scripts |
| Netcat | Manual protocol interaction |
| Enum4linux / smbclient | SMB enumeration |
| Nikto | Web vulnerability scanning |

## Key Findings

- 23 open ports with 7 services enumerated in depth
- 8 CVEs identified, with CVSS ranging from low to critical
- Critical vulnerability found - vsFTPd 2.3.4 backdoor grants unauthenticated root-level shell access. Requires immediate mitigation
- SMB null-session access confirmed independently across three tools (smbclient, Nmap NSE, enum4linux), exposing the password policy and enabling a remote command execution vulnerability (CVE-2007-2447).
- Common vulnerabilities across services: outdated/unsupported software, plaintext protocols and weak or absent authentication controls

## Skills Demonstrated

- Network reconnaissance and service enumeration
- Use of analysis and enumeration tools: Nmap, Netcat, Enum4Linux, smbclient, Nikto
- Cyber Security risk analysis
- Vulnerability analysis
- Linux command line navigation and interaction
- Executive and technical document writing
- Framework application (PTES)
- Attention to detail
- Problem solving
- Written communication

## Lessons Learned

- How reconnaissance and enumeration is conducted by cyber security analysts and penetration testers during their early stages.
- Understanding the strengths and limitations of black box enumeration against white box enumeration
- Exclusively using tools to investigate services is not sufficient, investigation should be supplemented with research across a variety of legitimate resources to boost credbility and enhance your learning.
- Inferred findings are not the same as confirmed findings (as noted as a limitation of black box enumeration)
- Misconfiguration of a service is proved to be detrimental to an organisation, highlighting the importance of carefully establishing and monitoring server settings.
- With every service available, there are specific vulnerabilities which can be exploited through different attack methods.

---

*This project was conducted in an isolated virtual lab against a machine for which permission was explicitly granted.*
