# RS1-POC VM Specifications

**Purpose:** Define the four virtual machine tiers for the Rwanda Studex 1 Proof of Concept.

---

## VM Tier 1: RW-Template (Demo VM)

**Use Case:** Government demonstrations, partner onboarding, PwC pitch dry-run

### Specifications
| Component | Value |
|-----------|-------|
| **CPU** | 4 vCPU |
| **RAM** | 8GB |
| **Storage** | 100GB SSD |
| **OS** | Ubuntu 22.04 LTS |
| **Network** | 1Gbps (Orgo.ai) |
| **Location** | Orgo.ai (closest to Rwanda: Mumbai or EU) |

### Software Stack
```yaml
Agent OS:
  - Control Hub (port 42069)
  - Agent Gateway (WhatsApp integration)
  - OpenMausBot (message routing)
  - Obsidian Sync (6-hour vault sync)

Models:
  - Qwen-Max (cloud API, via PwC OpenAI reseller)
  - Qwen3-8B (local, via Ollama)
  - Mistral-7B (local, fallback)

Integrations:
  - Tailscale (private mesh to Studex SA)
  - WhatsApp Business API (Meta-compliant)
  - Azure Blob Storage (Rwanda region, Obsidian vault)
```

### Agent Configuration
| Agent | Model | Purpose |
|-------|-------|---------|
| **CEO Agent** | Qwen-Max | Morning brief (7am), evening summary (9:30pm) |
| **Support Agent** | Qwen3-8B | L1 ticket deflection, FAQ, runbook queries |
| **Tech Agent** | Qwen3-8B | Data ingestion (Dynatrace, New Relic, ServiceNow) |
| **Research Agent** | Qwen-Max | Deep investigation, cross-tool correlation |
| **Ops Agent** | Qwen3-8B | Boltic orchestration, CI/CD remediation |

### Demo Script (60-Second Agent Task)
```
1. User sends WhatsApp message: "Server CPU at 95%, what do I do?"
2. Support Agent receives via WhatsApp Gateway (0.5s)
3. Tech Agent queries Dynatrace API for server metrics (2s)
4. Research Agent cross-references with recent deployments (3s)
5. Ops Agent generates remediation: "Scale from 2→4 nodes" (2s)
6. CEO Agent logs action to Obsidian vault (0.5s)
7. Support Agent sends WhatsApp response with approval button (1s)
8. User approves → Ops Agent executes auto-scaling (5s)
9. CEO Agent sends confirmation: "Scaled successfully. Cost: $0.42/hr" (1s)

Total Time: ~15 seconds
```

---

## VM Tier 2: RW-Arcade-1 (Gaming Server)

**Use Case:** StudEx Arcade tournaments, community building, talent recruitment

### Specifications
| Component | Value |
|-----------|-------|
| **CPU** | 2 vCPU |
| **RAM** | 4GB |
| **Storage** | 50GB SSD |
| **OS** | Ubuntu 22.04 LTS |
| **Network** | 1Gbps (low latency optimized) |

### Software Stack
```yaml
Game Servers:
  - FIFA/EA Sports FC server
  - Tekken 8 server
  - Arc Raiders server

Agent Integration:
  - Support Agent (tournament FAQ)
  - CEO Agent (prize announcements)
  - WhatsApp Gateway (registration, results)
```

### Tournament Flow
```
1. User messages WhatsApp: "Register for FIFA tournament"
2. Support Agent confirms registration + sends rules
3. Tournament runs (Saturday 6 Sep, 2pm CAT)
4. Winner announced via WhatsApp broadcast
5. Prize delivered: 6-month VM + Agentic Rise entry
```

---

## VM Tier 3: RW-Agentic-1 (Startup Cohort VM)

**Use Case:** Agentic Rise cohort (5+ Rwandan startups)

### Specifications
| Component | Value |
|-----------|-------|
| **CPU** | 4 vCPU |
| **RAM** | 8GB |
| **Storage** | 100GB SSD |
| **OS** | Ubuntu 22.04 LTS |
| **Network** | 1Gbps |

### Software Stack
```yaml
Agent OS:
  - Control Hub (multi-tenant, per-startup isolation)
  - Agent Gateway (WhatsApp per startup)
  - Obsidian Sync (shared vault, per-startup folders)

Models:
  - Qwen-Max (shared, cloud API)
  - Qwen3-8B (local, per-startup instance)

Tools:
  - Gitea (code repo, per startup)
  - Open WebUI (chat interface, per startup)
  - LiteLLM (model routing, cost tracking)
```

### Cohort Onboarding
| Startup | VM Allocation | Agent Team | Mentor |
|---------|---------------|------------|--------|
| **Startup 1** | 1 CPU / 2GB RAM | CEO + Support | Chris Perelta |
| **Startup 2** | 1 CPU / 2GB RAM | CEO + Support | Chris Perelta |
| **Startup 3** | 1 CPU / 2GB RAM | CEO + Support | Tumelo |
| **Startup 4** | 1 CPU / 2GB RAM | CEO + Support | Tumelo |
| **Startup 5** | 1 CPU / 2GB RAM | CEO + Support | Local Partner |

### Morning Brief Template (7am CAT)
```
Good morning, [Startup Name]! 🇷🇼

Yesterday's Progress:
- ✅ [Task 1 completed]
- ✅ [Task 2 completed]
- ⏳ [Task 3 in progress]

Today's Priorities:
1. [Priority 1]
2. [Priority 2]
3. [Priority 3]

Market Intelligence:
- [Relevant news/trend for startup's vertical]

Mentor Availability:
- [Chris/Tumelo] available [time slot] for [topic]

Let's build! 🚀
```

---

## VM Tier 4: RW-Business-Ghost (Local Partner VM)

**Use Case:** Rwandan on-ground agent's operational VM

### Specifications
| Component | Value |
|-----------|-------|
| **CPU** | 2 vCPU |
| **RAM** | 4GB |
| **Storage** | 50GB SSD |
| **OS** | Ubuntu 22.04 LTS |
| **Network** | 1Gbps |

### Software Stack
```yaml
Agent OS:
  - Control Hub (single-tenant)
  - Agent Gateway (WhatsApp Business)
  - Obsidian Sync (local vault)

Models:
  - Qwen3-8B (local, primary)
  - Qwen-Max (cloud, fallback)

Tools:
  - Meeting scheduler (government bookings)
  - Document generator (LOI/MOU templates)
  - Expense tracker (trip budget monitoring)
```

### Agent Team
| Agent | Purpose |
|-------|---------|
| **CEO Agent** | Daily task planning, meeting prep |
| **Support Agent** | WhatsApp FAQ for local businesses |
| **Research Agent** | Government contact lookup, policy research |
| **Ops Agent** | Travel logistics, accommodation booking |

---

## Network Topology

```
┌─────────────────────────────────────────────────────────────┐
│                     Orgo.ai Cloud                            │
│                                                              │
│  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐      │
│  │ RW-Template  │  │ RW-Arcade-1  │  │ RW-Agentic-1 │      │
│  │ (Demo)       │  │ (Gaming)     │  │ (Cohort)     │      │
│  │ Port 42069   │  │ Port 25565   │  │ Port 42069   │      │
│  └──────┬───────┘  └──────┬───────┘  └──────┬───────┘      │
│         │                 │                 │               │
│         └─────────────────┼─────────────────┘               │
│                           │                                 │
│                  ┌────────▼────────┐                        │
│                  │ Tailscale Relay │                        │
│                  │ (Private Mesh)  │                        │
│                  └────────┬────────┘                        │
└───────────────────────────┼─────────────────────────────────┘
                            │
                            │ Encrypted Tunnel
                            │
┌───────────────────────────▼─────────────────────────────────┐
│                 Rwanda (Local)                               │
│                                                              │
│  ┌──────────────┐              ┌──────────────┐             │
│  │ RW-Business- │              │  WhatsApp    │             │
│  │ Ghost        │◄────────────►│  Gateway     │             │
│  │ (Partner VM) │              │  (Meta API)  │             │
│  └──────┬───────┘              └──────┬───────┘             │
│         │                              │                     │
│         └──────────────┬───────────────┘                     │
│                        │                                     │
│               ┌────────▼────────┐                            │
│               │  Local Devices  │                            │
│               │  - MacBook      │                            │
│               │  - Government   │                            │
│               │  - Startups     │                            │
│               └─────────────────┘                            │
└─────────────────────────────────────────────────────────────┘

External Connections:
- Qwen API (UAE Azure endpoint, via PwC reseller)
- Obsidian Sync (Azure Blob Storage, Rwanda region)
- Studex SA (Tailscale mesh to Control Hub port 42069)
```

---

## Cost Breakdown (Monthly)

| VM Tier | Orgo.ai Cost | Qwen API | WhatsApp | Total/mo |
|---------|--------------|----------|----------|----------|
| **RW-Template** | $100 | $50 | $25 | $175 |
| **RW-Arcade-1** | $50 | $10 | $10 | $70 |
| **RW-Agentic-1** | $100 | $50 | $25 | $175 |
| **RW-Business-Ghost** | $50 | $20 | $15 | $85 |
| **TOTAL** | **$300** | **$130** | **$75** | **$505/mo** |

**Note:** First month covered by trip budget ($2,000-3,000). Ongoing cost: $505/mo until PwC deal closes (then transferred to PwC engagement).

---

## Provisioning Checklist

### Pre-Trip (Aug 15 - Sep 3)
- [ ] Create Orgo.ai account + add $500 credit
- [ ] Provision RW-Template VM (4 CPU / 8GB / 100GB)
- [ ] Provision RW-Arcade-1 VM (2 CPU / 4GB / 50GB)
- [ ] Provision RW-Agentic-1 VM (4 CPU / 8GB / 100GB)
- [ ] Provision RW-Business-Ghost VM (2 CPU / 4GB / 50GB)
- [ ] Install Ubuntu 22.04 LTS on all VMs
- [ ] Configure SSH keys (Tumelo's MacBook)
- [ ] Set up Tailscale relay node

### Agent OS Installation
- [ ] Deploy Control Hub on RW-Template (port 42069)
- [ ] Install Agent Gateway + OpenMausBot
- [ ] Configure Obsidian Sync (Azure Blob, Rwanda region)
- [ ] Deploy CEO Agent + Support Agent on RW-Template
- [ ] Test WhatsApp Gateway (send test message)
- [ ] Verify 6-hour Obsidian sync

### Dry-Run Testing
- [ ] Execute 60-second demo script (end-to-end)
- [ ] Generate morning brief (7am CAT, verify delivery)
- [ ] Generate evening summary (9:30pm CAT, verify delivery)
- [ ] Load test: 50 concurrent WhatsApp messages
- [ ] Measure response time (<5s target)
- [ ] Validate uptime (99.5%+ target)

---

**Owner:** Tumelo Ramaphosa  
**Last Updated:** September 9, 2026  
**Next Review:** September 16, 2026 (post-deployment)
