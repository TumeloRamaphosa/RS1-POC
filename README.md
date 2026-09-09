# RS1-POC: Rwanda Studex 1 Proof of Concept

**Mission:** Deploy a pre-POC virtual machine stack in Rwanda as a dry-run for the PwC Middle East engagement.

**Timeline:** September 2026 (Rwanda Trip) → October 2026 (PwC Pitch)

**Strategic Purpose:**
1. Test the Portable Agents deployment engine in a real emerging market
2. Validate the VM + Agent OS + WhatsApp interface model
3. Generate case study data for PwC pitch ("67% L1 deflection in Rwanda")
4. Partner with Russian tech (ART Engineering, NtechLab, Pharmasyntez) for Africa entry
5. Build the Agentic Rise cohort in Rwanda (5+ startups)

---

## Architecture Overview

```
┌─────────────────────────────────────────────────────────────────┐
│                    RS1-POC Stack                                 │
├─────────────────────────────────────────────────────────────────┤
│                                                                  │
│  ┌──────────────────────────────────────────────────────────┐   │
│  │  Rwanda VM (Orgo.ai or Local Server)                     │   │
│  │  ┌────────────────────────────────────────────────────┐  │   │
│  │  │  Agent OS (Control Hub - port 42069)              │  │   │
│  │  │  ├── CEO Agent (morning/evening briefs)           │  │   │
│  │  │  ├── Support Agent (L1 ticket deflection)         │  │   │
│  │  │  ├── Tech Agent (data ingestion)                  │  │   │
│  │  │  ├── Research Agent (deep investigation)          │  │   │
│  │  │  └── Ops Agent (Boltic orchestration)             │  │   │
│  │  └────────────────────────────────────────────────────┘  │   │
│  │                                                            │   │
│  │  ┌────────────────────────────────────────────────────┐  │   │
│  │  │  Integrations                                      │  │   │
│  │  │  ├── WhatsApp Gateway (client interface)          │  │   │
│  │  │  ├── Tailscale (private mesh to Studex SA)        │  │   │
│  │  │  ├── Obsidian Vault (audit trail, 6h sync)        │  │   │
│  │  │  └── Qwen API + Local Models (Ollama pool)        │  │   │
│  │  └────────────────────────────────────────────────────┘  │   │
│  └──────────────────────────────────────────────────────────┘   │
│                                                                  │
│  ┌──────────────────────────────────────────────────────────┐   │
│  │  Russian Partner Stack (Parallel Deployment)             │   │
│  │  ├── ART Engineering: Modular DC specs for Rwanda       │   │
│  │  ├── NtechLab: AI/facial recognition demo               │   │
│  │  └── Pharmasyntez: Pharma distribution tracking         │   │
│  └──────────────────────────────────────────────────────────┘   │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

---

## Phase 1: Pre-Trip Preparation (Aug 15 - Sep 3, 2026)

### Week 1 (Aug 15-22): Infrastructure Setup

| Task | Owner | Status | Notes |
|------|-------|--------|-------|
| Provision Rwanda VM on Orgo.ai (4 CPU / 8GB RAM / 100GB SSD) | Tumelo | ⏳ Pending | Template: RW-Template |
| Install Agent OS (Control Hub + dependencies) | Tumelo | ⏳ Pending | Use existing port 42069 stack |
| Configure Tailscale mesh (SA ↔ Rwanda) | Tumelo | ⏳ Pending | Test latency, throughput |
| Set up WhatsApp Gateway (test number) | Tumelo | ⏳ Pending | Use existing OpenMausBot |
| Deploy CEO Agent + Support Agent | Tumelo | ⏳ Pending | Morning/evening briefs |
| Test Obsidian vault sync (6-hour interval) | Tumelo | ⏳ Pending | Verify audit trail |

### Week 2 (Aug 23-30): Partner Integration

| Task | Owner | Status | Notes |
|------|-------|--------|-------|
| ART Engineering: Request Rwanda DC spec sheet | Natalia | ⏳ Pending | Modular unit pricing, deployment timeline |
| NtechLab: Prepare AI demo (facial recognition use case) | Natalia | ⏳ Pending | Rwanda government presentation (Aug 17) |
| Pharmasyntez: Define pharma tracking workflow | Natalia | ⏳ Pending | Cold chain + AU/EU funding angle |
| Integrate partner data into Agent OS | Tumelo | ⏳ Pending | Tech Agent ingests partner APIs |

### Week 3 (Aug 31 - Sep 3): Dry-Run Testing

| Task | Owner | Status | Notes |
|------|-------|--------|-------|
| End-to-end test: WhatsApp → Agent → Resolution | Tumelo | ⏳ Pending | Simulate L1 ticket |
| Generate morning video brief (7am Rwanda time) | Tumelo | ⏳ Pending | Qwen API + Higgsfield |
| Generate evening summary (9:30pm Rwanda time) | Tumelo | ⏳ Pending | Validate Obsidian sync |
| Load test: 50 concurrent WhatsApp messages | Tumelo | ⏳ Pending | Measure response time |
| Prepare demo script (60-second agent task) | Tumelo | ⏳ Pending | For government meetings |

---

## Phase 2: Rwanda Deployment (Sep 4-11, 2026)

### Day 1 (Fri Sep 5): SVHQ / Chris Alignment
- **Meeting:** Chris Perelta, SVHQ
- **Demo:** Show RW-Template VM live
- **Ask:** Confirm Agentic Rise cohort (5+ startups)
- **Outcome:** Evolve AI Summit date agreed

### Day 2 (Sat Sep 6): Arcade + RGIDA
- **Activity:** Gaming tournament (FIFA, Tekken)
- **Prize:** 6-month VM + Agentic Rise entry
- **Target:** 50+ registrations
- **Agent Role:** Support Agent handles FAQ via WhatsApp

### Day 3 (Sun Sep 7): Government Day 1 (RDB / MINICT)
- **Meeting:** Rwanda Development Board
- **Demo:** RS1-POC stack (60-second agent task)
- **Pitch:** "Sovereign AI infrastructure, deployed in weeks"
- **Ask:** LOI for ART modular DC pilot
- **Partner Angle:** ART Engineering (Russian DC tech)

### Day 4 (Mon Sep 8): Government Day 2 (Health / Education)
- **Meeting:** Ministry of Health
- **Demo:** Pharmasyntez pharma tracking workflow
- **Pitch:** AU/EU funding for African pharma manufacturing
- **Ask:** Support for funding application

- **Meeting:** Ministry of Education
- **Demo:** University VM deployment model
- **Pitch:** Campus data centres + Agentic Rise chapters
- **Ask:** MOU for 2+ universities

### Day 5 (Tue Sep 9): Wrap + Signings
- **Activity:** Sign LOI/MOU documents
- **Handover:** RW-Template VM to Agentic Rise cohort
- **Next Steps:** Monthly billing starts Oct 1

---

## Phase 3: Post-Trip Execution (Sep 12 - Oct 15, 2026)

### Week 1 (Sep 12-18): Follow-Up
| Task | Owner | Status |
|------|-------|--------|
| Send thank-you WhatsApp to all meeting contacts | Tumelo | ⏳ Pending |
| Email signed LOIs/MOUs to government contacts | Tumelo | ⏳ Pending |
| SVHQ debrief: Finalize SPV documents | Tumelo | ⏳ Pending |
| Write trip report (key decisions, pipeline value) | Tumelo | ⏳ Pending |

### Week 2-3 (Sep 19 - Oct 2): Agentic Rise Launch
| Task | Owner | Status |
|------|-------|--------|
| Onboard 5+ Rwandan startups to Agentic Rise | Chris + Tumelo | ⏳ Pending |
| Deploy RW-Agentic-1 VM (cohort-specific) | Tumelo | ⏳ Pending |
| First morning brief sent to cohort (7am Rwanda time) | CEO Agent | ⏳ Pending |
| First evening summary sent (9:30pm Rwanda time) | CEO Agent | ⏳ Pending |

### Week 4 (Oct 3-9): PwC Pitch Prep
| Task | Owner | Status |
|------|-------|--------|
| Compile Rwanda case study metrics | Tumelo | ⏳ Pending |
| Update PwC flowchart with Rwanda data | Tumelo | ⏳ Pending |
| Finalize white-label deck (PwC-branded) | Tumelo | ⏳ Pending |
| Schedule PwC pitch meeting (Oct 15+) | Tumelo | ⏳ Pending |

---

## Success Metrics

| Metric | Target | Measurement |
|--------|--------|-------------|
| **VM Uptime** | 99.5%+ | Orgo.ai monitoring |
| **L1 Ticket Deflection** | 60-70% | Support Agent analytics |
| **Morning Brief Delivery** | 100% on-time (7am CAT) | CEO Agent logs |
| **Evening Summary Delivery** | 100% on-time (9:30pm CAT) | CEO Agent logs |
| **Obsidian Sync** | Every 6h, 100% success | Vault audit trail |
| **WhatsApp Response Time** | <5 seconds | Gateway logs |
| **Agentic Rise Signups** | 5+ startups | Cohort enrollment |
| **Government LOIs/MOUs** | 1+ signed | RDB or MINICT |
| **Russian Partner Activation** | 1+ deployed (ART/Ntech/Pharmasyntez) | Integration complete |

---

## Budget

| Item | Cost (USD) | Notes |
|------|------------|-------|
| **VM Hosting (Orgo.ai)** | $200/mo | 4 VMs (Template, Arcade, Agentic, Business Ghost) |
| **WhatsApp Gateway** | $50/mo | Meta Business API + OpenMausBot |
| **Qwen API Credits** | $100/mo | Morning/evening briefs, LLM inference |
| **Tailscale** | $0 (free tier) | Private mesh networking |
| **Obsidian Sync** | $0 (self-hosted) | Azure Blob Storage (Rwanda region) |
| **Trip Costs** | $2,000-3,000 | Flights, accommodation, transport, events |
| **Pitch Night Venue** | $300 | KIC or CMU Africa |
| **Contingency** | $500 | Misc expenses |
| **TOTAL (excl. trip)** | **$350/mo** | Ongoing operational cost |
| **TOTAL (incl. trip)** | **$2,850** | One-time setup + first month |

---

## Risk Mitigation

| Risk | Likelihood | Impact | Mitigation |
|------|------------|--------|------------|
| **VM provisioning delayed** | Medium | High | Backup: Use local MacBook + Tailscale relay |
| **WhatsApp API approval slow** | Medium | Medium | Fallback: Use personal WhatsApp + manual agent relay |
| **Internet connectivity in Rwanda** | Low | Medium | Pre-download offline demos, record video briefs locally |
| **Government meetings cancelled** | Medium | High | Backup: Chris Perelta introductions, CMU Africa faculty connections |
| **Russian partners unresponsive** | Low | Medium | Proceed without them, pivot to EU/US DC partners |
| **Agentic Rise cohort no-show** | Medium | Medium | Incentivize: Free VM + Chris mentorship for first 5 signups |

---

## Next Steps (This Week)

| When | Action | Owner |
|------|--------|-------|
| **Mon Sep 9** | Create RS1-POC GitHub repo (push initial README) | Tumelo |
| **Mon Sep 9** | Provision RW-Template VM on Orgo.ai | Tumelo |
| **Tue Sep 10** | Install Agent OS on RW-Template | Tumelo |
| **Wed Sep 11** | Test Tailscale mesh (SA ↔ Rwanda) | Tumelo |
| **Thu Sep 12** | Configure WhatsApp Gateway | Tumelo |
| **Fri Sep 13** | Deploy CEO Agent + Support Agent | Tumelo |
| **Mon Sep 16** | Email Russian partners: Rwanda deployment timeline | Natalia |
| **Tue Sep 17** | Dry-run test: End-to-end WhatsApp → Agent flow | Tumelo |
| **Wed Sep 18** | Final pre-trip checklist review | Tumelo |

---

## Repository Structure (RS1-POC GitHub)

```
RS1-POC/
├── README.md                 # This document
├── architecture/
│   ├── vm-specs.md           # RW-Template, RW-Arcade-1, RW-Agentic-1, RW-Business-Ghost
│   ├── agent-os-config.yaml  # Control Hub configuration
│   └── network-topology.md   # Tailscale mesh, WhatsApp Gateway, Obsidian sync
├── deployment/
│   ├── orgo-provisioning.sh  # VM provisioning script
│   ├── agent-install.sh      # Agent OS installation
│   └── tailscale-setup.sh    # Private mesh configuration
├── partners/
│   ├── art-engineering/      # Modular DC specs, pricing, timeline
│   ├── ntechlab/             # AI demo, government presentation
│   └── pharmasyntez/         # Pharma tracking workflow, AU/EU funding
├── rwanda-trip/
│   ├── meetings/             # One-pagers for RDB, MINICT, MoH, MoE
│   ├── events/               # Arcade tournament, Pitch Night, Agentic Rise
│   └── logistics/            # Flights, accommodation, transport
├── metrics/
│   ├── uptime-monitoring.md  # VM uptime, response times
│   ├── ticket-deflection.md  # L1 automation rates
│   └── cohort-tracking.md    # Agentic Rise signups, engagement
└── pwcpitch/
    ├── case-study.md         # Rwanda success story for PwC
    ├── flowchart-update.md   # Implementation journey with Rwanda data
    └── deck-outline.md       # White-label pitch deck structure
```

---

**Owner:** Tumelo Ramaphosa, CEO — Studex Group  
**Last Updated:** September 9, 2026  
**Next Review:** September 16, 2026 (post-deployment check)

---

*This is the blueprint, Agent Lord. RS1-POC is your Rwanda dry-run → PwC proof-point → Russian partner Africa entry. All three plays in one move.*
