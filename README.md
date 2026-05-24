# CleanSwarm

**AI-Powered Multi-Service Cleaning Workforce Management Platform**

> Multi-agent SaaS for cleaning business automation — scheduling, dispatch, biometric verification, job management. Built with LangGraph.

---

## Overview

CleanSwarm is an enterprise-grade workforce management platform purpose-built for multi-service cleaning operations. Our AI-powered swarm intelligence engine automates scheduling, dispatch, quality control, and billing — enabling cleaning businesses to scale from 10 to 500+ workers without proportional admin overhead.

**Target Market:** Commercial cleaning, residential cleaning, vehicle detailing, marine cleaning, industrial/specialty cleaning operations.

---

## Architecture

```
src/
├── agents/           # LangGraph multi-agent system
│   ├── scheduler     # Job scheduling + constraint satisfaction
│   ├── dispatch      # Crew routing + ETA prediction
│   ├── billing       # Stripe metered billing
│   └── biometric     # Truein attendance verification
├── api/              # FastAPI backend
│   ├── routes/       # REST endpoints
│   └── middleware/   # Auth, CORS, rate limiting
├── core/             # Shared infrastructure
│   ├── config        # Environment management
│   ├── database      # SQLAlchemy models
│   └── security      # JWT + RBAC
└── bot/              # Telegram notifications (future)
```

---

## Pricing

| Plan | Monthly Fee | Per-Job Fee | Workers | Best For |
|---|---|---|---|---|
| Starter | $399/mo | $0.65/job | Up to 25 | Single-service operators |
| Growth | $999/mo | $0.45/job | Up to 100 | Multi-location businesses |
| Scale | $2,499/mo | $0.35/job | Unlimited | Enterprise operations |

---

## Tech Stack

| Component | Technology |
|---|---|
| AI Agents | LangGraph + Together AI (Llama 3.1 70B) |
| Backend | FastAPI + Python 3.11 |
| Database | PostgreSQL (Supabase) |
| Payments | Stripe (metered billing) |
| Biometrics | Truein SDK |
| Deployment | Docker → Hetzner Montreal (CAX21 ARM) |
| CI/CD | GitHub Actions |

---

## Quick Start

```bash
git clone https://github.com/franciscoderek7/cleanswarm.git
cd cleanswarm
pip install -r requirements.txt
cp .env.example .env
# Edit .env with your keys
docker-compose up -d
uvicorn src.api.main:app --reload --port 8000
```

---

## Project Status

| Phase | Status | Target |
|---|---|---|
| Landing page | ✅ Complete | Live on GitHub Pages |
| Backend scaffold | ✅ Complete | API routes + auth |
| Agent implementations | ✅ Complete | 4 LangGraph agents |
| Database integration | 🔄 In progress | Supabase PostgreSQL |
| First 3 customers | 🔄 LOIs sent | Ali, Andrew, Matt |
| Production deploy | ⏳ Pending | After first signed contract |

---

## SR&ED Eligible

This project qualifies for Canadian SR&ED tax incentives:
- Multi-agent scheduling optimization (experimental development)
- Constraint satisfaction for workforce allocation (systematic investigation)
- Predictive no-show modeling (applied research)
- Biometric + geofence integration (experimental development)

All commits prefixed with `R&D:` for audit trail compliance.

---

## License

MIT License

---

## Contact

- **Platform:** CleanSwarm
- **Organization:** CleanSwarm Inc.
- **GitHub:** @franciscoderek7
