# Open-XDR-Lab
Plateforme XDR open-source déployée sur VirtualBox simulant un environnement SOC réaliste avec détection multi-couches (endpoint + réseau) de 4 attaques APT.

## Architecture prévue
| VM | IP | OS | Rôle |
|----|----|----|------|
| Kali Linux | 192.168.100.10 | Kali 2024 | Attaquant |
| Windows 10 (x2) | .20 / .21 | Win10 Pro | Victimes |
| Ubuntu Zeek | .40 | Ubuntu 22 | Sonde réseau |
| Ubuntu Wazuh+ELK | .50 | Ubuntu 22 | SOC Central |

## Attaques prévues (MITRE ATT&CK)
- [ ] T1550.002 — Pass-the-Hash Lateral Movement
- [ ] T1071 — C2 Beaconing (Sliver)
- [ ] T1048.003 — DNS Tunneling (dnscat2)
- [ ] T1486 — Ransomware Simulation (Python)

## Stack technique
- Wazuh (SIEM/EDR)
- Zeek (analyse réseau)
- osquery (endpoint queries)
- ELK Stack (visualisation)

## Structure
```
open-xdr-lab/
├── setup/       (configs Wazuh, Zeek, osquery)
├── attacks/     (guides et scripts)
├── hunting/     (requêtes Threat Hunting)
└── metrics/     (résultats mesurés)
```
## Disclaimer
Environnement isolé VirtualBox — usage éducatif uniquement.
