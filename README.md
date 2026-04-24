# Hackathon Mirakl - UC3 Talent Market Intelligence System

## Technical Exports Package

This folder contains the Markdown files required to document the UC3 MVP.

## Contents

```text
UC3_md_files/
├── prompts/
│   ├── signal_classifier_prompt.md
│   ├── talent_pool_scoring_prompt.md
│   ├── candidate_intelligence_prompt.md
│   ├── latent_seniority_prompt.md
│   ├── competitor_brief_prompt.md
│   └── prospect_watchlist_prompt.md
└── docs/
    ├── methodology_note.md
    └── technical_exports_summary.md
```

## MVP summary

The MVP demonstrates two levels of output for Mirakl Talent Acquisition:

1. **Sourcing output** — candidate leads for a target role with LinkedIn URLs, fit reasoning, latent seniority scoring, and personalized outreach angles.
2. **Strategic output** — competitor intelligence brief detecting hiring intent and recommending concrete TA actions.

The system follows the logic:

```text
public signals → talent pool intelligence → candidate reasoning → strategic recommendations
```

## Workflows included separately

The n8n JSON exports should be placed in a `/workflows` folder:

```text
workflow_1_collect_signals.json
workflow_2_talent_intelligence.json
workflow_3_competitor_brief.json
workflow_4_prospect_watchlist.json
```

## Datasets included separately

The CSV exports should be placed in a `/datasets` folder:

```text
role_queries.csv
seed_market_signals.csv
market_signals.csv
talent_pools.csv
candidate_seed.csv
candidate_leads.csv
competitor_watchlist.csv
competitor_briefs.csv
prospect_watchlist.csv
```

## Compliance note

The MVP does not scrape LinkedIn directly. Candidate records are demo seed profiles or recruiter-validated inputs. The system demonstrates the intelligence layer: signal interpretation, talent pool scoring, latent seniority inference, competitor intelligence, and outreach recommendation.
