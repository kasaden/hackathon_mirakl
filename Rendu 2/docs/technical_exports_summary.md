# UC3 — Technical Exports Summary

## Project
Talent Market Intelligence System — France scope

## Objective
Provide Mirakl Talent Acquisition with a working MVP that transforms public market signals into sourcing intelligence and strategic competitor intelligence.

---

# 1. Workflow exports

| Workflow | File | Purpose |
|---|---|---|
| Workflow 1 | `workflow_1_collect_signals.json` | Collects and classifies market signals |
| Workflow 2 | `workflow_2_talent_intelligence.json` | Scores talent pools and generates candidate intelligence |
| Workflow 3 | `workflow_3_competitor_brief.json` | Generates a strategic competitor brief |
| Workflow 4 | `workflow_4_prospect_watchlist.json` | Generates sourcing queries from priority talent pools |

The n8n workflow JSON exports are included in the `/workflows` folder.

---

# 2. Agent prompts

| Agent | Prompt file | Output |
|---|---|---|
| Signal Classifier Agent | `signal_classifier_prompt.md` | Classified market signals |
| Talent Pool Intelligence Agent | `talent_pool_scoring_prompt.md` | Company scores and sourcing priorities |
| Candidate Intelligence Agent | `candidate_intelligence_prompt.md` | Candidate reasoning and outreach angle |
| Latent Seniority Agent | `latent_seniority_prompt.md` | Seniority inference and timing |
| Competitor Strategic Brief Agent | `competitor_brief_prompt.md` | Strategic competitor intelligence |
| Prospect Watchlist Agent | `prospect_watchlist_prompt.md` | Search queries for recruiters |

The MVP uses OpenAI through n8n HTTP nodes. The prompts are Dust-ready: each includes system instructions, user prompt, expected JSON output, and role-specific constraints.

---

# 3. Knowledge base

No dedicated Dust knowledge base was deployed in the MVP.

The MVP knowledge base is implemented as structured Google Sheets tables used by the n8n workflows:

- `role_queries`
- `seed_market_signals`
- `market_signals`
- `talent_pools`
- `candidate_seed`
- `candidate_leads`
- `competitor_watchlist`
- `competitor_briefs`
- `prospect_watchlist`

---

# 4. Datasets

| Dataset | Purpose |
|---|---|
| `role_queries.csv` | Input TA queries |
| `seed_market_signals.csv` | Demo seed signals |
| `market_signals.csv` | Classified signals |
| `talent_pools.csv` | Ranked companies and talent pools |
| `candidate_seed.csv` | Demo candidate inputs |
| `candidate_leads.csv` | Candidate intelligence output |
| `competitor_watchlist.csv` | Competitors monitored by the system |
| `competitor_briefs.csv` | Strategic intelligence output |
| `prospect_watchlist.csv` | Generated sourcing queries |

Some candidate records are demo-grade simulated profiles used to demonstrate the intelligence layer. They must be validated before real outreach.

---

# 5. Interface

The MVP interface is the Google Sheets / n8n command center.

If an Airtable, Lovable, or deployed interface is added later, include the URL here:

```text
Demo interface link: [insert link]
```

---

# 6. GitHub repository

```text
GitHub repository: Not applicable for this MVP / [insert link if available]
```

The prototype was implemented using n8n workflows, Google Sheets datasets, and OpenAI prompts.

---

# 7. Compliance note

The MVP does not scrape LinkedIn directly.

Candidate records are either demo seed profiles or recruiter-validated inputs. The system demonstrates the intelligence layer: signal interpretation, talent pool scoring, latent seniority inference, strategic competitor analysis, and outreach recommendation.
