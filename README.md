# WRT54GL-cves

Security research on the **Linksys WRT54GL** Wireless-G Broadband Router, firmware **v4.30.18 build 006** (the latest and final firmware release for this end-of-life product).

Two authenticated OS command injection vulnerabilities in the web management interface (`apply.cgi` diagnostic functions). Both were discovered by static analysis of the stock firmware `httpd` and `rc` binaries and **dynamically verified** against the real firmware code running in an emulated environment. As of 2026-10-11 neither issue has any public record for this model (checked: NVD full-text and CPE matching, Exploit-DB full index, Metasploit source tree, public PoC repositories, vendor research blogs).

| # | Directory | Title | CVE |
|---|-----------|-------|-----|
| 1 | [CVE-TBD-ping-ip-command-injection](CVE-TBD-ping-ip-command-injection/) | Ping diagnostic `ping_ip` authenticated OS command injection | requested |
| 2 | [CVE-TBD-traceroute-ip-command-injection](CVE-TBD-traceroute-ip-command-injection/) | Traceroute diagnostic `traceroute_ip` authenticated OS command injection | requested |

- Researcher: **Zimo-666**
- Discovery: 2026-10-10
- Vendor notified: 2026-10-11

All proof-of-concept steps are non-destructive: they create empty marker files only, change no configuration, and do not modify the device firmware.
