# UC3 — Methodology Note

## How the agent adapts sourcing strategy by profile type

The system adapts its sourcing strategy depending on the target profile type. It does not apply the same signal logic to technical, business, and leadership roles.

---

## 1. Tech profiles

Examples:

- Senior AI Engineer
- ML Engineer
- Data Scientist
- AI Platform Engineer
- Agent Builder

For technical profiles, the agent prioritizes evidence of technical environment and production capability.

The most important signals are:

- current and previous companies;
- engineering blogs;
- GitHub or open-source activity;
- job descriptions mentioning relevant stacks;
- conference talks or technical content;
- AI, ML, LLM, RAG, data platform and deployment keywords;
- tenure in strong technical environments.

The agent does not rely only on visible job titles. A candidate may still be titled “Machine Learning Engineer” but may be senior in practice if they have spent several years in a high-density AI environment such as Dataiku, Criteo, Dust, Mistral AI or Contentsquare.

For technical profiles, the system prioritizes:

```text
skills + technical environment + tenure + production context
```

Recommended sources:

- company career pages;
- GitHub;
- engineering blogs;
- technical talks;
- conference speaker pages;
- public job descriptions;
- recruiter-validated LinkedIn profiles.

---

## 2. Business profiles

Examples:

- Sales Operations
- RevOps
- Marketplace Operations
- Customer Success Operations
- Product Marketing
- GTM Strategy

For business profiles, the agent prioritizes market context and operating environment rather than technical proof.

The most important signals are:

- company growth;
- new market launches;
- GTM hiring spikes;
- CRM / RevOps tooling exposure;
- marketplace or SaaS business model experience;
- customer segment ownership;
- previous experience in scale-up environments.

For business profiles, a strong signal is not GitHub activity. It is whether the person has operated in the right commercial context.

The system prioritizes:

```text
company stage + GTM context + business model fit + operating scope
```

Recommended sources:

- LinkedIn Recruiter or recruiter-validated profiles;
- company pages;
- job boards;
- sales / RevOps communities;
- webinars;
- podcasts;
- customer case studies;
- company growth news.

---

## 3. Leadership profiles

Examples:

- AI Engineering Manager
- Head of Data
- VP Engineering
- Director of Product
- Head of Talent
- General Manager

For leadership profiles, the agent looks for scope, influence and organizational context.

The most important signals are:

- team size;
- management scope;
- funding rounds;
- reorgs;
- leadership announcements;
- conference panels;
- previous scale-up experience;
- hiring responsibility;
- visibility in strategic company initiatives.

A leadership profile is not assessed only by title. The agent looks for evidence that the person has led teams, scaled systems, managed transformation or owned strategic outcomes.

The system prioritizes:

```text
scope + influence + timing + strategic relevance
```

Recommended sources:

- press releases;
- leadership announcements;
- company blogs;
- funding news;
- podcasts;
- conference panels;
- org charts when available;
- recruiter-validated LinkedIn profiles.

---

# Source prioritization logic

| Source | Tech | Business | Leadership | Why |
|---|---:|---:|---:|---|
| Career pages | High | High | Medium | Shows hiring intent and team expansion |
| Engineering blogs | High | Low | Medium | Reveals technical maturity and stack |
| GitHub | Medium | Low | Low | Useful for technical validation but incomplete |
| Product announcements | Medium | Medium | High | Shows strategic direction |
| Funding news | Medium | High | High | Indicates hiring capacity and growth stage |
| Layoffs / reorgs | Medium | Medium | High | Indicates mobility windows |
| Conference talks | High | Medium | High | Reveals expertise and influence |
| LinkedIn / recruiter-validated profiles | High | High | High | Useful for profile validation, not automated scraping |
| ATS / Talent CRM | High | High | High | Best enterprise source when available |

---

# How ambiguity is handled

The system treats every signal as probabilistic.

## High confidence

Multiple aligned signals from reliable sources.

Example:

```text
career page + engineering blog + role-specific keywords + France location
```

## Medium confidence

One strong signal or several weak but consistent signals.

Example:

```text
candidate tenure + strong company environment + adjacent role title
```

## Low confidence

Single weak source or unclear role relevance.

Example:

```text
generic AI mention without team, role or location evidence
```

The agent must never say:

```text
This person is definitely senior.
```

It should say:

```text
The combination of tenure, technical environment and role adjacency suggests senior-level capability.
```

This makes the system safer, more credible and more useful for an enterprise TA team.
