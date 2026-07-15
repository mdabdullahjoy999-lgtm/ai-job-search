# Search Queries for Job Scraper

## Installed portal CLIs (primary for `/scrape`)

`/scrape` discovers every portal skill under `.agents/skills/*/SKILL.md` and runs its CLI first. Enabled for this profile: `linkedin-search` and `freehire-search` (country-agnostic). The four Danish portal demos (Jobbank, Jobdanmark, Jobindex, Jobnet) are installed but disabled (`enabled: false`) since this profile is UK-based — re-enable them individually if ever relevant. You do **not** need a matching `site:` line below for enabled CLIs to run.

The `site:` query templates in this file are the **WebSearch fallback** — for portals without a CLI, company career pages, or when a CLI fails.

## Search Sites

Primary:
- **linkedin.com/jobs** - LinkedIn job listings (filter: United Kingdom / London); covered by `linkedin-search` CLI
- **freehire.dev** - tech/software/data/ML aggregator across ~50 ATS platforms; covered by `freehire-search` CLI

Secondary (company career pages via Google, or if you want to add a specific UK board later with `/add-portal`):
- Direct Google searches with `site:` filters for known target companies
- If a specific UK job board becomes a priority (e.g. Reed, Totaljobs, CV-Library, Indeed UK), scaffold it with `/add-portal`

## Query Categories

Queries are grouped by priority. Each query should be combined with your location terms (London, UK, or "Remote") where the site supports it.

### Priority 1: Data Scientist / ML Engineer (graduate & internship)

These match your strongest and most desired career direction.

```
linkedin-search: -q "Graduate Data Scientist" -l "London, United Kingdom"
linkedin-search: -q "Data Scientist Intern" -l "London, United Kingdom"
linkedin-search: -q "Machine Learning Engineer" -l "Remote"
freehire-search: --query "data scientist" --country "United Kingdom"
freehire-search: --query "machine learning engineer" --remote true
site:linkedin.com/jobs "Graduate Data Scientist" United Kingdom
```

### Priority 2: AI Engineer (graduate & internship, incl. forward-deployed)

```
linkedin-search: -q "Graduate AI Engineer" -l "London, United Kingdom"
linkedin-search: -q "AI Engineer Internship" -l "United Kingdom"
linkedin-search: -q "Forward Deployed AI Engineer" -l "Remote"
freehire-search: --query "AI engineer" --country "United Kingdom"
site:linkedin.com/jobs "forward deployed engineer" OR "forward deployed AI" United Kingdom
```

### Priority 3: Data Analyst (adjacent / broader net)

```
linkedin-search: -q "Data Analyst" -l "London, United Kingdom"
linkedin-search: -q "Graduate Data Analyst" -l "United Kingdom"
freehire-search: --query "data analyst" --country "United Kingdom"
```

### Priority 4: Broader Technical / Consulting

Wider net for adjacent roles that the profile's skill set (Python, SQL, BigQuery, statistical/decision analysis) could also fit.

```
linkedin-search: -q "Technical Consultant" -l "London, United Kingdom"
linkedin-search: -q "Data Science Consultant" -l "Remote"
freehire-search: --query "python developer" --country "United Kingdom"
```

## Location Filter

When evaluating results, verify the job location is within reasonable commute distance from home, or remote:
- London and Greater London (ideal)
- Remote, UK-wide (ideal — no commute constraint)
- Hybrid roles requiring occasional London office presence (acceptable)
- Roles requiring relocation outside the UK (too far — deal-breaker given visa/study constraints)

## Date Filter

Only include jobs posted within the last 14 days, or with an application deadline that has not yet passed. If a posting date cannot be determined, include it but flag as "date unknown".

## Adapting Queries

If the user specifies a focus area, select queries from the matching category and also generate 2-3 custom queries for that focus. For example:
- "/scrape healthcare" -> Priority 1/2 queries + custom queries combining "data scientist" or "ML engineer" with "healthcare" / "clinical" / "NHS"
- "/scrape internship" -> re-run all categories filtered to internship/graduate-level titles only
