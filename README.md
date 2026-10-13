# WRT54GL-cves

Security research on the **Linksys WRT54GL** Wireless-G Broadband Router, firmware **v4.30.18 build 006** (the latest and final firmware release for this end-of-life product).

Five vulnerabilities in the web management interface (`apply.cgi`) and its backend service handlers (`httpd` / `rc`). All were discovered by static analysis of the stock firmware binaries and verified against the real firmware code running in an emulated environment — the strength of dynamic evidence varies per issue and is stated honestly in each document. As of 2026-10-11 none of the five issues has any public record for this model (checked: NVD full-text and CPE matching, Exploit-DB full index, Metasploit source tree, public PoC repositories, vendor research blogs).

| # | Directory | Title | CVE |
|---|-----------|-------|-----|
| 1 | [CVE-TBD-ping-ip-command-injection](CVE-TBD-ping-ip-command-injection/) | Ping diagnostic `ping_ip` authenticated OS command injection (CWE-78) | requested |
| 2 | [CVE-TBD-traceroute-ip-command-injection](CVE-TBD-traceroute-ip-command-injection/) | Traceroute diagnostic `traceroute_ip` authenticated OS command injection (CWE-78) | requested |
| 3 | [CVE-TBD-ntp-server-stack-overflow](CVE-TBD-ntp-server-stack-overflow/) | `ntp_server` stack-based buffer overflow in the rc NTP service handler (CWE-121) | pending submission |
| 4 | [CVE-TBD-heartbeat-config-injection](CVE-TBD-heartbeat-config-injection/) | heartbeat WAN `hb_server_ip`/`ppp_username` newline injection into bpalogin.conf (CWE-93) | pending submission |
| 5 | [CVE-TBD-ddns-config-injection](CVE-TBD-ddns-config-injection/) | DDNS `ddns_username`/`ddns_passwd` newline injection into the ez-ipupdate config (CWE-93) | pending submission |

- Researcher: **Zimo-666**
- Discovery: 2026-10-10 (issues 1–2), 2026-10-11 (issues 3–5)
- Vendor notified: 2026-10-11 (issues 1–2); pending for issues 3–5 (as of 2026-10-13)

All proof-of-concept steps are non-destructive: they create empty marker files or crash a single service handler only, install no persistence, and do not modify the device firmware.
