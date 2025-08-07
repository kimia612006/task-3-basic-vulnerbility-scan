Task 3 – Basic Vulnerability Scan on My PC

 
Objective
Use opensource tools to identify common vulnerabilities on a local machine.

 Tools Used
 Nmap v7.94SVN
 Script: `script vuln`
 Command used:
  bash
  sudo nmap sV script vuln 10.49.85.113
  
 Scan Results Summary

 Target IP: `10.49.85.113`
 Open Port: `53/tcp`
 Service Detected: `dnsmasq v2.51`
 Total CVEs Found: 20+
 Highest CVSS Score: `10.0`

 Critical Vulnerabilities Identified

 CVE ID  CVSS Score  Description  Link 

 [CVE201714493](https://vulners.com/cve/CVE201714493)  9.8  Remote code execution via crafted DNS requests 
 [CVE201714492](https://vulners.com/cve/CVE201714492)  9.8  Stackbased buffer overflow 
 [CVE201714491](https://vulners.com/cve/CVE201714491)  9.8  Heapbased buffer overflow 
 [EDBID:42943](https://vulners.com/exploitdb/EDBID:42943)  9.8  Public exploit available 
 [CVE202025682](https://vulners.com/cve/CVE202025682)  8.3  Information disclosure 
 [CVE202350387](https://vulners.com/cve/CVE202350387)  7.5  Exploitable with DoS attack 
 [CVE20220934](https://vulners.com/cve/CVE20220934)  7.5  Denial of Service issue 


 Risk Assessment

 Impact: Remote Code Execution (RCE), Denial of Service (DoS), Memory Corruption
 Severity: Critical
 Affected Service: `dnsmasq 2.51`
 Status: Service is running on a vulnerable version with multiple public exploits available

 Suggested Remediation

 Update `dnsmasq` to the latest stable version (recommended: 2.89+).
 Apply security patches as recommended in each CVE.
 If not required, disable port `53` externally (only allow internal DNS resolution).
 Regularly monitor for CVE updates and patch vulnerable services.


 Key Learnings

 Performed a realworld vulnerability assessment.
 Understood CVSS and how to interpret vulnerability scores.
 Identified critical remote exploits in commonly used DNS software.
