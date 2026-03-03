# TEAM DELTA — Source Citation & Evidence Verification Register

**Document ID**: TD-00  
**Purpose**: Maps every factual claim used in Team Delta deliverables to its verifiable source.  
**Last Updated**: February 12, 2026  
**Classification**: CONFIDENTIAL — Capstone Reference Document  
**Verification Status**: Chat 2 (Facts) ✅ | Chat 3 (Code) ✅ | Chat 4 (Merge) ✅ — Pending Chat 5 (Dissemination) ✅

---

## Section 1: Primary Forensic Evidence (Original Incident Data)

All claims about the November 2022 Racami infostealer incident are derived from the following original evidence artifacts provided to Team Delta.

| Claim | Source Artifact | Notes |
|-------|----------------|-------|
| Date of compromise: November 5, 2022, 23:13:29 UTC | Racami_-_Infostealer.png (Hudson Rock/Cavalier platform screenshot) | "Date Compromised: 2022-11-05 23:13:29" visible in screenshot |
| Initial detection: November 12, 2022, 22:16:59 (Detected 14 times) | Racami_-_Infostealer.png | "Initial Detection: 2022-11-12 22:16:59 (Detected 14 times)" |
| Latest detection: November 12, 2022, 22:16:59 | Racami_-_Infostealer.png | Visible in screenshot metadata |
| Stealer family: RedLine | Racami_-_Infostealer.png | "Stealer Family: RedLine" visible in screenshot |
| Stealer Log ID: GH[984304A1DB022880654C9054CBD33F2D] | Racami_-_Infostealer.png; Browser_Artifacts.xlsx (sheet name) | Consistent across both sources |
| Operating System: Windows 10 Enterprise x64 | Racami_-_Infostealer.png | Visible in screenshot |
| Antivirus: Windows Defender | Racami_-_Infostealer.png | Visible in screenshot |
| Malware path: C:\Users\richa[redacted]\AppData\Local\Temp\1000001001\bre.exe | Racami_-_Infostealer.png | Partially redacted in screenshot; path visible |
| IP Address: 154.1[redacted] | Racami_-_Infostealer.png | Partially redacted |
| Employee password reuse identified | Racami_-_Infostealer.png | "Employee password reuse identified" notation visible |
| Applications found: git | Racami_-_Infostealer.png | "Applications found: git" visible |
| 13 corporate credentials found | Racami_-_Infostealer.png | "Corporate Credentials Found: 13" visible |
| Compromised browsers: Chrome, Edge, Firefox | Browser_Artifacts.xlsx | Google_[Chrome]_Default.txt, Microsoft_[Edge]_Default.txt, Firefox_o02coest.default-beta.txt |
| Telegram application data compromised | Browser_Artifacts.xlsx | "Telegram" listed as compromised directory |

### URL/Credential Mapping (All 13 Pairs)

Source: URL_Mapping_csv_-_Sheet1.csv and Racami_-_Infostealer.png

| # | URL | Login |
|---|-----|-------|
| 1 | https://cisstg01.racami.com/CIS/login/racami | superadmin |
| 2 | https://cisqa05.racami.com/CIS/login/racami | superadmin |
| 3 | https://cisqa04.racami.com/CIS/login/chen%20co | c****o_superadmin |
| 4 | https://cisqa04.racami.com/CIS/app | r***n*** |
| 5 | https://git.racami.com/users/sign_in | rn***@racami.com |
| 6 | https://cisqa02.racami.com/CIS/login/chen%20co | c****o_superadmin |
| 7 | https://cisqa04.racami.com/CIS/login/pay+ | superadmin |
| 8 | https://cisqa01.racami.com/CIS/login/racami | superadmin |
| 9 | https://cisprod01.racami.com/CIS/login/racami | superadmin |
| 10 | https://cisuat03.racami.com/CIS/login/racami | superadmin |
| 11 | https://cisqa03.racami.com/CIS/login/racami | superadmin |
| 12 | https://work.racami.com/secure/Dashboard.jspa | rn***@racami.com |
| 13 | https://cisqa02.racami.com/CIS/login/racami | superadmin |

### Stealer Log Artifact Directories

Source: Browser_Artifacts.xlsx

Passwords.txt, Autofills, ImportantAutofills.txt, DomainDetects.txt, InstalledBrowsers.txt, ProcessList.txt, Cookies (directory), UserInformation.txt, InstalledSoftware.txt, Telegram (directory), Profile_1 (directory with Telegram data including configs, maps, settings, key_data)

### Installed Software (Selected — Security/Development Relevant)

Source: Installed_Software.xlsx

| Software | Version | Significance |
|----------|---------|-------------|
| Visual Studio Community 2019 | 16.11.1 | Primary IDE — confirms developer role |
| IntelliJ IDEA Community Edition 2022.2.3 | 222.4345.14 | Secondary IDE — Java development |
| Microsoft SQL Server Management Studio 18.11.1 | 15.0.18410 | Database administration — customer data access |
| pgJDBC 42.2.18 | 42.2.18 | PostgreSQL driver — additional database access |
| TIBCO Jaspersoft Studio 6.17.0 | 6.17 | Enterprise BI/reporting — financial data access |
| Microsoft Azure Storage Emulator v5.10 | 5.10.19227.211 | Cloud infrastructure tool |
| AnyDesk | 7.0.1 | Remote access tool — potential persistence vector |
| Google Chrome | 107.0.5304.87 | Browser — credential store compromised |
| Microsoft Edge | 107.0.1418.35 | Browser — credential store compromised |
| Mozilla Firefox (x86 en-US) | 107.0 | Browser — credential store compromised |
| mRemoteNG | 1.76.20.24615 | Multi-protocol remote connection manager |
| Foxit Reader | 9.4.0.16811 | PDF reader — phishing delivery vector |
| OBS Studio | 27.1 | Screen recording software |
| Adobe Photoshop CC 2019 | 20.0 | Indicates media/design work |
| Python Launcher | 3.9.7427 | Scripting capability |
| Integration Services (SSIS) | 15.0.2000.168 | SQL Server ETL tool |
| Browser for SQL Server 2019 | 15.0.2000 | SQL Server component |

---

## Section 2: Racami Company Information (OSINT)

| Claim | Source | Verification (Chat 2) |
|-------|--------|-----------------------|
| Racami, LLC is a private IT/software services provider headquartered in Norcross, Georgia | OSINT_Analysis.pdf (Gemini report, p.1) | ✅ A5-01: Confirmed — 3145 Northwoods Pkwy Suite 300, Norcross, GA 30071 (RocketReach, LeadIQ) |
| Founded 2008 | OSINT_Analysis.pdf (Gemini report, p.1) | ✅ A5-02: Confirmed — founded 2008 by Hani Khalaf (racami.com/about-racami-company-overview/) |
| Flagship platform: Alchem-e (modules: Pay, Proof, Doc Creator, Batch, Edge) | OSINT_Analysis.pdf (Gemini report, p.1) | ✅ A5-03: Confirmed (racami.com) |
| Specializes in Customer Communications Management (CCM), workflow automation, SaaS | OSINT_Analysis.pdf (Gemini report, p.1) | ✅ A5-04: Confirmed (racami.com) |
| Serves financial services, healthcare, and insurance sectors | OSINT_Analysis.pdf (Gemini report, p.1) | ✅ A5-05: Confirmed — also includes book publishing and marketing sectors |

---

## Section 3: HellCat Ransomware / 2025 Exploitation (Verified Web Sources)

These sources document the proven consequence of the 2022 infostealer infection.

### Source 3A: Hudson Rock / Infostealers.com
**Title**: "HELLCAT Ransomware Group Strikes Again: Four New Victims Breached via Jira Credentials from Infostealer Logs"  
**Author**: Alon Gal  
**Published**: April 5, 2025  
**URL**: https://www.infostealers.com/article/hellcat-ransomware-group-strikes-again-four-new-victims-breached-via-jira-credentials-from-infostealer-logs/  
**Verification**: ✅ A1-01, A1-02, A1-05 confirmed

Claims supported:
- HellCat ransomware group targeted Racami, LLC (USA) among four victims
- ✅ Four victims confirmed: HighWire Press, Asseco Poland, Racami, LeoVegas (A1-01)
- Attack exploited Jira credentials harvested by infostealer malware
- HellCat claimed to have stolen internal files, communications, and financial records
- Attack followed established HellCat playbook: compromised Jira credentials → data exfiltration → extortion
- Breach announcement included countdown timer and "Jiraware <<3!!" signature
- ⚠️ A1-03: Exact formatting may vary — verify spacing from primary screenshot
- Hudson Rock confirmed all four breaches stemmed from compromised Jira credentials harvested by infostealers
- Racami described as "a technology firm specializing in customer communications management"
- Stolen data "might include client communications, financial records, or proprietary software"

### Source 3B: SC Media
**Title**: "Pilfered Jira credentials leveraged in HellCat ransomware attacks"  
**Published**: April 9, 2025  
**URL**: https://www.scworld.com/brief/pilfered-jira-credentials-leveraged-in-hellcat-ransomware-attacks  
**Verification**: ✅ A1-06, A1-07 confirmed

Claims supported:
- Four U.S. and European companies compromised by HellCat ransomware-as-a-service
- Attacks exploited "information-stealing malware-harvested Atlassian Jira credentials"
- Infostealers involved included Lumma Stealer, Raccoon, Redline, and StealC
- Racami specifically named as a victim
- Same technique previously used against Ascom, Jaguar Land Rover, Schneider Electric, Telefonica, and Orange Group

### Source 3C: BleepingComputer (referenced in Source 3A)
**Title**: HellCat hackers go on a "worldwide Jira hacking spree"  
**URL**: https://www.bleepingcomputer.com/news/security/hellcat-hackers-go-on-a-worldwide-jira-hacking-spree/  
**Verification**: ✅ A1-09 confirmed (URL verified)

Claims supported:
- HellCat conducting systematic campaign targeting Jira instances globally
- Stolen credentials from infostealers used as primary attack vector

### Source 3D: Ransomware.live
**URL**: https://www.ransomware.live/group/hellcat  
**Verification**: ✅ A1-04 confirmed

Claims supported:
- HellCat leak site included: "Jiraware <<3 !! We have breached Racami's internal systems. The data in our possession poses a serio[us]..."

### Source 3E: OSINT_Analysis.pdf (Gemini Report)
Claims supported (cross-referenced with above web sources):
- November 2022 RedLine infection served as origin point for 2025 ransomware attack
- Stolen Jira credentials (work.racami.com) remained in dark web log shops for over two years
- HellCat began "Jira hacking spree" in April 2025 using old infostealer logs
- Credentials never rotated or protected by MFA, enabling 2025 exploitation
- Hudson Rock identified the forensic link between 2022 infostealer and 2025 breach

### Source 3F: KELA Cyber
**Title**: "Hellcat Hacking Group Unmasked: Investigating Rey and Pryx"  
**Published**: March 27, 2025 (updated November 27, 2025)  
**URL**: https://www.kelacyber.com/blog/hellcat-hacking-group-unmasked-rey-and-pryx/  
**Verification**: ✅ A2-01 through A2-03 confirmed

Claims supported:
- HellCat key operators identified as "Rey" (Saif Khader, Amman, Jordan) and "Pryx"
- Group originally known as "ICA Group"
- Rey involved in Telefonica breach and multiple high-profile incidents

---

## Section 4: Infostealer Threat Landscape Context

### Source 4A: Sekoia.io
**Title**: "Overview of the Russian-speaking infostealer ecosystem: the logs"  
**Published**: January 16, 2025  
**URL**: https://blog.sekoia.io/overview-of-the-russian-speaking-infostealer-ecosystem-the-logs/  
**Verification**: ✅ A4-01 confirmed

Claims supported:
- Logs sold on Russian Market/Genesis Market between $5 and $100 depending on volume, associated accounts, victim location, and log accuracy
- Infostealer logs are commonly text files containing account passwords, session cookies, credit card data, cryptocurrency wallet data, and system profiling data

### Source 4B: BleepingComputer / ReliaQuest
**Title**: "'Russian Market' emerges as a go-to shop for stolen credentials"  
**Published**: June 2, 2025  
**URL**: https://www.bleepingcomputer.com/news/security/russian-market-emerges-as-a-go-to-shop-for-stolen-credentials/  
**Verification**: ✅ A4-02 through A4-05 confirmed

Claims supported:
- Russian Market logs available at prices as low as $2
- Russian Market grew significantly after Genesis Market takedown (April 2023)
- ✅ A4-06: Exact date confirmed — April 4–5, 2023 (Operation Cookie Monster), FBI-led with Dutch National Police and 17 countries
- 85% of credentials on Russian Market are recycled from existing sources
- Lumma dominated the market after Raccoon Stealer law enforcement action

### Source 4B-Supplemental: Genesis Market Takedown
**Source**: BleepingComputer + TechCrunch (new sources from Chat 2 verification)  
**URLs**:
- https://www.bleepingcomputer.com/news/security/fbi-seizes-stolen-credentials-market-genesis-in-operation-cookie-monster/
- https://techcrunch.com/2023/04/05/fbi-genesis-market-seized-stolen-logins/

Claims supported:
- Genesis Market takedown: April 4–5, 2023 (Operation Cookie Monster)
- FBI-led operation with Dutch National Police and 17 countries

### Source 4C: Rapid7
**Title**: "Inside Russian Market: Uncovering the Botnet Empire"  
**URL**: https://www.rapid7.com/blog/post/tr-inside-russian-market-uncovering-the-botnet-empire/  
**Verification**: ✅ A4-07 confirmed

Claims supported:
- Russian Market launched credential/bot log sales in late 2021
- Top vendors use multiple infostealers (Lumma, Rhadamanthys, Acreed, Vidar, Stealc, RedLine)
- Logs are data packages exfiltrated from compromised machines using infostealer malware

### Source 4D: OSINT_Analysis.pdf (Gemini Report)

Claims supported:
- Known RedLine C2 IP active in late 2022: 95.179.163.157 — ❌ A3-06: UNVERIFIABLE. Specific IP could not be confirmed in open sources. Recommend flagging as "per Gemini OSINT report — not independently verified"
- RedLine used api.ipify.org for victim IP fingerprinting — ⚠️ A3-03: CORRECTED. RedLine uses various services (api.ip.sb/ip, api.ipify.org, ip-api.com), not exclusively api.ipify.org
- Common process hollowing target: Regsvcs.exe — ✅ A3-07 confirmed (CloudSEK, Cyber Florida)
- Hardcoded user agent: Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1; SV1) — ❌ A3-04: UNVERIFIABLE. Not confirmed in RedLine-specific literature. Recommend removing or marking as approximate

### Source 4E: RedLine Technical Profile (New — discovered during Chat 2 verification)

| Source | URL | Claims Supported |
|--------|-----|------------------|
| CloudSEK | https://www.cloudsek.com/blog/technical-analysis-of-the-redline-stealer | TEMP folder staging, process hollowing into Regsvcs.exe |
| Splunk | https://www.splunk.com/en_us/blog/security/do-not-cross-the-redline-stealer-detections-and-analysis.html | TEMP directory deployment patterns |
| GridInSoft | https://gridinsoft.com/spyware/redline | File staging in Users/Temp directory |
| Triskele Labs | https://www.triskelelabs.com/blog/redline-stealer | Full ransomware within 35 minutes of initial RedLine infection |
| ANY.RUN | https://any.run/malware-trends/redline/ | Rapid execution, pricing ($100–$200) |
| ThreatSpike | https://www.threatspike.com/blog/redline-infostealer-analysis-part-2/ | Uses api.ip.sb/ip for IP fingerprinting |
| McAfee | https://www.mcafee.com/blogs/other-blogs/mcafee-labs/redline-stealer-a-novel-approach/ | Uses ip-api.com for IP fingerprinting |
| Flare | https://flare.io/learn/resources/blog/redline-stealer-malware | First appeared March 2020, COVID-themed phishing |
| NordVPN | https://nordvpn.com/blog/redline-stealer-malware/ | Origin and distribution history |
| InfoSec Institute | https://www.infosecinstitute.com/resources/malware-analysis/redline-stealer-malware-full-analysis/ | Pricing: $150 lite / $200 pro |
| SpyCloud | https://spycloud.com/blog/why-credential-stealing-malware-is-giving-soc-teams-the-blues/ | Pricing: $100/month or $800 lifetime |
| MITRE ATT&CK S1240 | https://attack.mitre.org/software/S1240/ | Official RedLine ATT&CK entry; first tracked March 2020 (Proofpoint) |
| Cyber Florida | https://cyberflorida.org/redline-stealer-malware-analysis/ | Process hollowing into Regsvcs.exe confirmed |

---

## Section 5: MITRE ATT&CK Technique References

All MITRE ATT&CK technique IDs reference the official MITRE ATT&CK knowledge base at https://attack.mitre.org/  
**Verification**: All 18 technique IDs verified against live ATT&CK database (Chat 2, Part B). Two name corrections noted.

| Technique ID | Name | Source for Mapping | Verification |
|-------------|------|-------------------|--------------|
| T1204.002 | User Execution: Malicious File | Malware path in %TEMP% directory (forensic evidence) | ✅ B-01 |
| T1566 | Phishing | Inferred from execution path + Foxit Reader presence | ✅ B-02 |
| T1059 | Command and Scripting Interpreter | Developer tools present (Python, PowerShell, Visual Studio) | ✅ B-03 |
| T1547.001 | Boot or Logon Autostart Execution: Registry Run Keys / Startup Folder | Staged directory structure (1000001001) | ⚠️ B-04: Add "/ Startup Folder" to name |
| T1562.001 | Impair Defenses: Disable or Modify Tools | Windows Defender present but failed to detect | ✅ B-05 |
| T1036 | Masquerading | Generic filename "bre.exe" designed to avoid suspicion | ✅ B-06 |
| T1555.003 | Credentials from Password Stores: Credentials from Web Browsers | Passwords.txt, all 3 browser credential stores compromised | ✅ B-07 |
| T1539 | Steal Web Session Cookie | Cookie directories in stealer log artifacts | ✅ B-08 |
| T1552.001 | Unsecured Credentials: Credentials in Files | Plaintext password storage in browsers | ✅ B-09 |
| T1518 | Software Discovery | InstalledSoftware.txt in stealer artifacts | ✅ B-10 |
| T1082 | System Information Discovery | UserInformation.txt, DomainDetects.txt | ✅ B-11 |
| T1087 | Account Discovery | Multiple user accounts enumerated | ✅ B-12 |
| T1078 | Valid Accounts | Superadmin credentials + AnyDesk/mRemoteNG present | ✅ B-13 |
| T1005 | Data from Local System | All browser data, Telegram data, system profiles | ✅ B-14 |
| T1119 | Automated Collection | Full harvest completed in under 60 seconds (RedLine behavior) | ✅ B-15 |
| T1041 | Exfiltration Over C2 Channel | Data appeared on detection platform Nov 12 | ✅ B-16 |
| T1195.002 | Supply Chain Compromise: Compromise Software Supply Chain | (if referenced in deliverables) | ✅ B-17 |
| T1219 | Remote Access Tools | AnyDesk/mRemoteNG presence | ⚠️ B-18: Name updated from "Remote Access Software" to "Remote Access Tools" (current ATT&CK) |

---

## Section 6: Standards and Framework References

| Standard | Citation | Verification |
|----------|----------|--------------|
| NIST SP 800-61 Rev. 2 | Computer Security Incident Handling Guide (August 2012) | ✅ A6-01, A6-02: Confirmed. Four-phase lifecycle verified. **⚠️ A6-03 CRITICAL: Rev. 3 published April 3, 2025, supersedes Rev. 2. Rev. 2 formally withdrawn. See Section 7 for details. Chat 5 will handle reference updates.** |
| CIS Controls v8 | Center for Internet Security Controls, Version 8 (May 2021) | ✅ A7-01: Confirmed — released May 18, 2021 at RSA Conference. Note: v8.1 update released June 2024. |
| MITRE ATT&CK Framework | https://attack.mitre.org/ (Enterprise Matrix) | ✅ All 18 technique IDs verified (Part B) |

### Source 6A: NIST SP 800-61 Rev. 3 (New — discovered during Chat 2 verification)
**Title**: "Incident Response Recommendations and Considerations for Cybersecurity Risk Management"  
**Published**: April 3, 2025  
**URLs**:
- https://csrc.nist.gov/pubs/sp/800/61/r3/final
- https://csrc.nist.gov/news/2025/nist-revises-sp-800-61

Key changes from Rev. 2:
- Completely restructured to align with NIST CSF 2.0 Functions (Govern, Identify, Protect, Detect, Respond, Recover)
- Replaces the four-phase lifecycle model
- Rev. 2 formally withdrawn

**Action for Chat 5**: All deliverables currently reference Rev. 2. Add a footnote acknowledging Rev. 3 supersession. Do NOT wholesale-replace Rev. 2 references, as the deliverables' analysis is based on the Rev. 2 framework and remains valid in context.

### Source 6B: CIS Controls v8.1 (New — noted during Chat 2 verification)
**Published**: June 2024  
**Source**: https://www.cisecurity.org/  
Note: Iterative update to v8. Current deliverables reference v8, which remains valid. Consider adding a footnote in future revisions.

---

## Section 7: Claims Removed or Corrected

| Previous Claim | Issue | Resolution | Source |
|---------------|-------|------------|--------|
| "~$10 per Flashpoint/KELA threat intelligence, 2023-2024" | No verifiable Flashpoint/KELA source for this specific price point; professor flagged as inaccurate for superadmin access to enterprise infrastructure | Removed entirely. No specific pricing cited in any deliverable. | Original review |
| Delta Group report analyzed 5 URLs | Original evidence contains 13 URL/credential pairs | Corrected to full 13-pair dataset in all deliverables | Original review |
| HellCat/2025 outcome not mentioned in any deliverable | Professor identified this as a critical gap — the proven consequence of the unrotated credentials | Added as significant note in Risk Assessment, Executive Brief, and IR Plan | Original review |
| Stealer family listed as "Redacted (likely RedLine/Vidar)" | Screenshot clearly shows "Stealer Family: RedLine" | Corrected to confirmed RedLine in all deliverables | Original review |
| RedLine uses exclusively api.ipify.org for IP fingerprinting | Multiple sources show RedLine variants use different services | ⚠️ Broaden to: "RedLine queries external IP lookup services (e.g., api.ip.sb/ip, api.ipify.org, ip-api.com)" | Chat 2: A3-03 (ThreatSpike, McAfee) |
| Hardcoded user-agent "Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1; SV1)" | Not confirmed in any RedLine-specific technical analysis | ❌ Flag as unverified or remove. Source was Gemini OSINT report only. | Chat 2: A3-04 |
| RedLine C2 IP 95.179.163.157 | Specific IP not confirmed in open sources | ❌ Flag as unverified. Source was Gemini OSINT report only — cannot be independently corroborated. | Chat 2: A3-06 |
| T1547.001 named "Registry Run Keys" | Official MITRE name includes "/ Startup Folder" | ⚠️ Update to "Registry Run Keys / Startup Folder" in TD_02 and any ATT&CK mapping tables | Chat 2: B-04 |
| T1219 named "Remote Access Software" | MITRE ATT&CK updated the technique name | ⚠️ Update to "Remote Access Tools" in TD_02 and any ATT&CK mapping tables | Chat 2: B-18 |
| AppLocker code uses `New-AppLockerPolicy -Action Deny` | `-Action` is not a valid parameter; `-RuleType Deny` also invalid | ❌ CRITICAL: Replace with XML-based policy approach in Containment_Artifacts and TD_08 | Chat 3: C2 |
| Jira session invalidation via `DELETE /rest/auth/1/session/{user}` | Endpoint only logs out the currently authenticated user, not arbitrary users | ❌ CRITICAL: Replace with password-change or account-disable approach in TD_08 | Chat 3: C9 |
| NIST SP 800-61 Rev. 2 cited as current standard | Rev. 3 published April 3, 2025; Rev. 2 formally withdrawn | ⚠️ Add supersession footnote to all deliverables. Do not remove Rev. 2 analysis — it remains valid in historical context. Chat 5 will handle. | Chat 2: A6-03 |

---

## Section 8: Code Verification Register

**Verified**: February 12, 2026 (Chat 3)  
**Scope**: All code snippets and tool references in Team Delta deliverables  
**Method**: Each item verified against official vendor documentation via web search

### 8.1 Script/Query Verification Summary

| ID | Script/Query | Language | Document(s) | Verdict | Official Documentation | Notes |
|----|-------------|----------|-------------|---------|----------------------|-------|
| C1 | AD Credential Rotation | PowerShell | Containment_Artifacts, TD_08 | ✅ CORRECT | https://learn.microsoft.com/en-us/powershell/module/activedirectory/set-adaccountpassword | All cmdlets and parameters verified |
| C2 | AppLocker TEMP Execution Block | PowerShell | Containment_Artifacts, TD_08 | ❌ INCORRECT | https://learn.microsoft.com/en-us/powershell/module/applocker/new-applockerpolicy | **CRITICAL**: Both versions use invalid parameters. Replace with XML-based policy + `Set-AppLockerPolicy -Merge` |
| C3 | IIS Session Invalidation | PowerShell | Containment_Artifacts, TD_08 | ⚠️ PARTIAL | https://learn.microsoft.com/en-us/aspnet/core/security/data-protection/configuration/default-settings | DataProtection key path is environment-specific; add clarifying comment |
| C4 | AnyDesk Removal | PowerShell | Containment_Artifacts, TD_08 | ✅ CORRECT | https://support.anydesk.com/docs/command-line-interface | Both CLI and WMI approaches are valid |
| C5 | Network Adapter Isolation | PowerShell | Containment_Artifacts | ✅ CORRECT | https://learn.microsoft.com/en-us/powershell/module/netadapter/disable-netadapter | — |
| C6 | Impossible Travel Detection | KQL | TD_08 | ✅ CORRECT | https://learn.microsoft.com/en-us/kusto/query/prev-function | `serialize` + `prev()` pattern is valid |
| C7 | Session Without Authentication | Splunk SPL | TD_08 | ✅ CORRECT | https://docs.splunk.com/Documentation/SplunkCloud/latest/SearchReference/Aggregatefunctions | All functions verified |
| C8 | Git History Audit & Secret Scanning | Bash | Containment_Artifacts, TD_05R | ⚠️ PARTIAL | https://github.com/gitleaks/gitleaks | `gitleaks detect` deprecated in v8.19.0+; use `gitleaks git` |
| C9 | Jira Session Invalidation | Bash (curl) | TD_08 | ❌ INCORRECT | https://developer.atlassian.com/server/jira/platform/cookie-based-authentication/ | **CRITICAL**: API cannot target other users' sessions. Replace with password-change or account-disable approach |
| C10 | pfSense/pf Firewall Rules | pf.conf | TD_08 | ✅ CORRECT | https://man.openbsd.org/pf.conf | Hostname resolution is static (at rule load time only) |
| C11 | HIBP API Query | PowerShell | TD_05R, TD_08 | ⚠️ PARTIAL | https://haveibeenpwned.com/API/v3 | Add `ZeroFreeBSTR()` cleanup; clarify `/breaches` returns all breaches globally |
| C12 | Chrome Password Storage Check | PowerShell | TD_05R | ✅ CORRECT | Chromium source / community docs | `credentials_enable_service` key verified |
| C13 | TEMP Directory Executable Sweep | PowerShell | TD_05R, TD_08 | ✅ CORRECT | https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.management/get-childitem | — |
| C14 | Sigma Rule: Suspicious TEMP Execution | Sigma YAML | TD_08 | ✅ CORRECT | https://sigmahq.io/docs/basics/rules.html | Optional: remove unnecessary `*` wildcard from `contains` pattern |
| C15 | Remote Access Tool Audit | PowerShell | TD_05R | ⚠️ PARTIAL | AnyDesk support docs; Microsoft Learn | `'Logged in from'` log pattern unverified against AnyDesk docs; add clarifying comment |

### 8.2 Tool Reference Verification

| ID | Tool | Verdict | Official Source | Notes |
|----|------|---------|----------------|-------|
| D-01 | gitleaks | ✅ CORRECT | https://github.com/gitleaks/gitleaks | Note: `detect` subcommand deprecated v8.19.0+; use `git` subcommand |
| D-02 | trufflehog | ⚠️ CASING | https://github.com/trufflesecurity/trufflehog | Use `trufflehog` (lowercase) for CLI/repo; "TruffleHog" in prose |
| D-03 | FTK Imager | ✅ CORRECT | https://www.exterro.com/ftk-product-downloads/ftk-imager-version-4-7-1 | By Exterro (formerly AccessData); supports E01, MD5/SHA-1 |
| D-04 | CAINE | ✅ CORRECT | https://www.caine-live.net/ | Computer Aided INvestigative Environment; Ubuntu-based; v13.0 current |
| D-05 | Hudson Rock / Cavalier | ✅ CORRECT | https://www.hudsonrock.com/ | Platform: cavalier.hudsonrock.com; publication: infostealers.com |
| D-06 | Have I Been Pwned (HIBP) | ✅ CORRECT | https://haveibeenpwned.com/API/v3 | API v3; auth header: `hibp-api-key`; created by Troy Hunt |

### 8.3 Cross-Document Consistency Issues

| ID | Issue | Documents Affected | Severity | Resolution |
|----|-------|--------------------|----------|------------|
| E-01 | AppLocker `New-AppLockerPolicy` uses invalid parameters — different invalid syntax in each doc | Containment_Artifacts (Artifact 7.4), TD_08 (Section 4.2) | **CRITICAL** | Replace both with XML-based deny policy approach (see Chat 3: C2 corrected code) |
| E-02 | AnyDesk removal uses different methods across docs | Containment_Artifacts, TD_08 | Low | Both methods are valid. Optionally consolidate into single script with CLI + WMI fallback |
| E-03 | Git/gitleaks commands identical across docs | Containment_Artifacts, TD_05R | None | Good consistency — no action needed |

### 8.4 Code Verification Statistics

| Category | Total | Correct | Partially Correct | Incorrect |
|----------|-------|---------|--------------------|-----------|
| Code Snippets (C1–C15) | 15 | 9 (60%) | 4 (27%) | 2 (13%) |
| Tool References (D-01–D-06) | 6 | 5 (83%) | 1 (17%) | 0 (0%) |
| **Total** | **21** | **14 (67%)** | **5 (24%)** | **2 (10%)** |

**Critical fixes required**: 2 (C2: AppLocker, C9: Jira API)  
**Minor improvements recommended**: 5 (C3, C8, C11, C15, D-02)

---

## Appendix: Verification Pipeline Status

| Chat | Scope | Status | Key Findings |
|------|-------|--------|-------------|
| Chat 1 | Checklist Generation | ✅ Complete | 48 factual claims + 21 code items extracted |
| Chat 2 | Factual Claim Verification | ✅ Complete | 40/48 verified, 6 corrected, 2 unverifiable (83.3% clean rate) |
| Chat 3 | Code Verification | ✅ Complete | 14/21 correct, 5 partial, 2 critical errors (67% clean rate) |
| Chat 4 | Citation Register Merge | ✅ Complete | This document |
| Chat 5 | Dissemination to Deliverables | ✅ Complete | All corrections disseminated to deliverables |

---

*End of Citation Register*
