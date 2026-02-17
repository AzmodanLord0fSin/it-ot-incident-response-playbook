# it-ot-incident-response-playbook
Incident Response Playbook bridging IT and OT/ICS security environments

# IT/OT Incident Response Playbook

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Contributions Welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg)](CONTRIBUTING.md)

**Bridging the gap between IT Security and Operational Technology (OT/ICS) incident response.**

---

## Overview

This playbook provides actionable guidance for security teams responding to incidents that span IT and OT/ICS environments. Based on real-world experience in industrial production and critical infrastructure security.

### Why This Playbook?

**The Challenge:**
- IT security teams lack OT/ICS operational knowledge
- OT engineers don't understand modern IT attack vectors
- Ransomware and cyber threats increasingly target production systems
- Traditional IR playbooks don't address OT safety and availability requirements

**This Playbook:**
- Bridges IT security expertise with OT operational reality
- Addresses unique challenges: safety systems, production continuity, air-gapped networks
- Provides decision trees for critical go/no-go moments
- Based on NIST Cybersecurity Framework + IEC 62443 considerations

---

## Target Audience

- **CISOs** in manufacturing and critical infrastructure
- **IT Security Teams** supporting OT environments
- **OT/ICS Engineers** dealing with cyber incidents
- **Incident Response Teams** expanding into industrial environments

---

## Covered Scenarios

### Current (v1.0)
1. **[Ransomware Spread (IT → OT)](03_Response/Scenario_1_Ransomware.md)** 🔴 Critical
   - Initial access via phishing/credential compromise
   - Lateral movement to engineering workstations
   - Impact on HMI/SCADA and production systems

### Planned (v1.1+)
2. **VPN Compromise** - Unauthorized remote access to OT networks
3. **Supply Chain Attack** - Malicious firmware or software updates
4. **Insider Threat** - Deliberate sabotage by authorized personnel

---

## Structure
```
00_Framework/       → IR lifecycle and IT/OT differences
01_Preparation/     → Network segmentation, asset inventory, team roles
02_Detection/       → Indicators of compromise, monitoring tools
03_Response/        → Step-by-step incident scenarios (MAIN CONTENT)
04_Recovery/        → OT system restoration procedures
05_Post_Incident/   → Lessons learned, RCA templates
99_Appendix/        → Quick references, protocols, contacts
```

---

## Quick Start

### For Practitioners

1. **Read the Framework**
   - Start with [IT/OT Differences](00_Framework/IT_OT_Differences.md) to understand unique challenges
   - Review [IR Lifecycle](00_Framework/IR_Lifecycle.md) for process overview

2. **Choose Your Scenario**
   - Jump to [Ransomware Response](03_Response/Scenario_1_Ransomware.md) for the most common threat
   - Follow step-by-step actions with decision trees

3. **Adapt to Your Environment**
   - Customize contact information, network layouts, and tools
   - Conduct tabletop exercises with your team

### For Organizations

1. **Gap Analysis**: Compare your current IR plan against these scenarios
2. **Training**: Use scenarios for security awareness and IR team drills
3. **Customization**: Fork this repo and adapt for your specific environment
4. **Testing**: Conduct tabletop exercises quarterly

---

## Key Principles

### IT vs. OT Response Differences

| Aspect | IT Response | OT Response |
|--------|-------------|-------------|
| **Priority** | Confidentiality → Integrity → Availability | Safety → Availability → Integrity |
| **Isolation** | Immediate shutdown acceptable | Only if SAFE - production continuity critical |
| **Forensics** | Comprehensive investigation | Limited - uptime prioritized |
| **Patching** | Deploy immediately | Test thoroughly, scheduled maintenance windows |
| **Recovery** | Hours to days | Minutes to hours for critical systems |

### Critical OT Considerations

⚠️ **Safety First**: Never compromise safety systems or cause physical hazards
⚠️ **Production Impact**: Understand criticality before isolating systems
⚠️ **Air-Gapped Systems**: IR procedures must work without network access
⚠️ **Legacy Systems**: Many OT devices cannot be updated or monitored with standard tools

---

## Tools & Technologies

### IT Security Tools
- Microsoft Defender XDR
- Sysmon / Windows Event Logs
- EDR Platforms (CrowdStrike, SentinelOne, etc.)

### OT Security Tools
- **Network Monitoring**: Nozomi Networks, Claroty, Dragos
- **Asset Discovery**: Claroty, Armis
- **Protocol Analysis**: Wireshark, Zeek

### Forensics
- FTK Imager (disk imaging)
- Magnet RAM Capture (memory acquisition)
- Volatility (memory analysis)

---

## Framework & Standards

This playbook aligns with:

- **NIST Cybersecurity Framework** (Identify, Protect, Detect, Respond, Recover)
- **IEC 62443** (Industrial Automation and Control Systems Security)
- **ISO 27001/27002** (Information Security Management)
- **MITRE ATT&CK for ICS** (Threat tactics and techniques)

---

## Contributing

Contributions are welcome! This playbook improves through community input.

**How to contribute:**
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/new-scenario`)
3. Commit your changes (`git commit -m 'Add new scenario: XYZ'`)
4. Push to branch (`git push origin feature/new-scenario`)
5. Open a Pull Request

See [CONTRIBUTING.md](CONTRIBUTING.md) for detailed guidelines.

---

## Usage & License

This playbook is released under the **MIT License** - free for educational and commercial use.

**Attribution appreciated but not required.** If you find this useful, consider:
- Starring the repository
- Sharing with your network
- Providing feedback via Issues

---

## Author

**Tobias K**

- Chief Information Security Officer
- Background: OT Security in Automotive Production (24/7 Manufacturing)
- IEC 62443 Certified (Industrial Cybersecurity Professional)
- Experience: ISO 27001 ISMS, Microsoft Defender XDR, Incident Response

**Connect:**
- LinkedIn: [https://www.linkedin.com/in/tobias-k-2b3733162/]
- GitHub: [AzmodanLord0fSin](https://github.com/AzmodanLord0fSin)

---

## Acknowledgments

Inspired by real-world incidents and lessons learned from:
- Industrial production environments (automotive, manufacturing)
- IT/OT convergence challenges
- Community resources: SANS ICS, Dragos, ICS-CERT/CISA

Special thanks to the industrial cybersecurity community for sharing knowledge and experiences.

---

## 📞 Feedback & Support

- **Questions?** Open an [Issue](https://github.com/[username]/it-ot-incident-response-playbook/issues)
- **Suggestions?** Submit a [Pull Request](https://github.com/[username]/it-ot-incident-response-playbook/pulls)
- **Discussion?** Use [Discussions](https://github.com/[username]/it-ot-incident-response-playbook/discussions)

---

## ⚠️ Disclaimer

This playbook provides general guidance based on industry best practices. Every organization's OT environment is unique. **Always:**
- Consult with your safety officers and plant managers
- Test procedures in non-production environments first
- Adapt guidance to your specific systems, regulations, and risk profile
- Maintain compliance with local laws and industry standards

The authors assume no liability for outcomes resulting from use of this playbook.

---

## 🗺️ Roadmap

**v1.0** (Current)
- [x] Ransomware scenario (IT → OT spread)
- [x] Framework documentation
- [x] Decision trees and checklists

**v1.1** (Planned)
- [ ] VPN Compromise scenario
- [ ] Supply Chain Attack scenario
- [ ] Insider Threat scenario
- [ ] Additional detection techniques
- [ ] Recovery validation procedures

**v2.0** (Future)
- [ ] Industry-specific adaptations (Energy, Water, Manufacturing)
- [ ] Integration with SIEM/SOAR platforms
- [ ] Automated detection rules (Sigma, Suricata)
- [ ] Video walkthroughs and training materials

---

**Last Updated:** February 2025 | **Version:** 1.0.0
