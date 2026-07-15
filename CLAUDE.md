# Job Application Assistant for MD Abdullah

## Role
This repo is a job application workspace. Claude acts as a career advisor and application assistant for MD Abdullah, helping with:
1. **Job fit evaluation** - Assess job postings against your profile (skills, experience, behavioral traits)
2. **CV tailoring** - Adapt existing CV templates (LaTeX/moderncv) to target specific roles
3. **Cover letter writing** - Draft targeted cover letters using existing templates (LaTeX)
4. **Interview preparation** - Prepare answers, questions, and talking points for interviews
5. **Career strategy** - Advise on positioning and personal branding

## Candidate Profile

<!-- This section is auto-populated by /setup. You can also fill it in manually. -->

### Identity
- **Name:** MD Abdullah
- **Location:** London, United Kingdom (open to hybrid/onsite in London, or remote UK-wide)
- **Right to work:** Pre-settled status under the EU Settlement Scheme (UK) — no sponsorship required
- **Languages:** Bengali (native), English (professional working proficiency)
- **Status:** Currently studying — MSc Data Science and Analytics, University of Westminster (Sept 2025 – Sept 2026), seeking internship or graduate-level roles
- **LinkedIn headline:** "MSc Data Science candidate | AI/ML | Data Scientist"

### Education
- **MSc Data Science and Analytics** (2025-2026) - University of Westminster, London
  - Dissertation: "ICU Readmission and Mortality Prediction with AI and Machine Learning" (MIMIC-IV v3.1, Google BigQuery)
  - Topics: Data Mining & Machine Learning, Web & Social Media Analytics, Business Analytics, Big Data Theory and Practice, Data Warehousing and Business Intelligence
- **BSc Textile Engineering, First Class Honours** (2016-2020) - Bangladesh University of Textiles
  - Specialization: Apparel Engineering

### Professional Experience
- **Merchandising Data Assistant** (2021 - 2022) - **Quest Tex Solutions** (Dhaka, Bangladesh)
  - Engineered Python and Excel ETL pipelines for 200+ SKUs, reducing manual processing time by 40%
  - Built a statistical demand-forecasting model, improving forecast accuracy by 15% and cutting overstock costs by £8,000/month
  - Developed Power BI dashboards delivering 6+ reports to 15+ stakeholders; maintained 99.2% data quality
- **Data Science Virtual Experience Program** (2026) - **BCG X, Forage**
  - Analyzed churn for 14,606 SME energy accounts (9.72% churn rate); engineered 61 features and trained a Random Forest classifier reaching 0.669 ROC-AUC
  - Identified energy consumption and tenure as stronger churn drivers than price sensitivity; flagged low recall (~9%) as a deployment blocker
- **GenAI Virtual Experience Program** (2026) - **BCG X, Forage**
  - Built a rule-based financial chatbot prototype in Python (Pandas) for BCG's GenAI Consulting team, parsing 10-K/10-Q filings into plain-language answers

### Technical Skills
- **Primary:** Python (Pandas, NumPy, scikit-learn, TensorFlow/Keras, LightGBM, XGBoost), SQL, Google BigQuery
- **Secondary:** R, HuggingFace Transformers/BERT/T5/spaCy (NLP), Power BI, Tableau, Excel (Solver, PrecisionTree)
- **Domain:** Clinical/healthcare ML (ICU outcome prediction), business analytics & decision analysis, quantitative/financial analysis (equity clustering, portfolio risk), operations research (linear programming)
- **Software:** Google Colab, Git/GitHub, Jupyter

### Certifications
- **BCG X Data Science Job Simulation** - Forage - completed 2026
- **BCG X GenAI Job Simulation** - Forage - completed 2026

### Publications
None yet.

### Awards
None yet.

### Behavioral Profile
- **Structured autonomy** - Thrives with a clear problem and defined success criteria; comfortable bringing structure to ambiguous starting points (e.g. scoping a dissertation) through planning and milestones
- **Deliberate, evidence-first decision-maker** - Defaults to testing assumptions and comparing metrics over gut calls; moves quickly on low-risk, time-boxed decisions
- **Strengths:** Deep independent technical ownership (end-to-end modelling), clear and concise communication of technical work to non-technical audiences, coordinating a workstream within a larger team project
- **Growth areas:** Limited industry (non-academic) production ML experience so far - actively building this through the MSc dissertation and virtual experience programs
- **Thrives in:** Structured but intellectually demanding environments with clear problems and room to go deep

### What Excites You
- Building end-to-end ML systems (data → model → interpretable results) for problems with real-world stakes
- Translating technical/statistical findings into plain-language recommendations for non-technical stakeholders

### Target Sectors
- AI / Machine Learning / Data Science (primary): tech companies, consultancies, healthcare analytics
- Open to adjacent sectors (e.g. energy/commodities analytics) where the quantitative toolkit transfers

### Deal-breakers
- None specified yet - open, revisit with `/setup --section experience` as preferences firm up

## Repo Structure
- `cv/` - LaTeX CV variants (moderncv template, banking style)
- `cover_letters/` - LaTeX cover letters (custom cover.cls template)
- `.claude/skills/` - AI skill definitions for the application workflow
- `.agents/skills/` - Job search CLI tools

## Workflow for New Job Applications
1. User provides a job posting (URL or text)
2. **Always evaluate fit first**: skills match, experience match, behavioral/culture match. Present this assessment to the user before proceeding.
3. If good fit: create targeted CV (`cv/main_<company>.tex`) and cover letter (`cover_letters/cover_<company>_<role>.tex`)
4. **Verify both documents** (see Verification Checklist below)
5. Prepare interview talking points based on the role requirements and your strengths

**Important:** When mentioning agentic coding or AI tooling in CVs/cover letters, explicitly reference **Claude Code** by name.

## Verification Checklist
After creating or updating a CV or cover letter, re-read the generated file and verify **all** of the following before presenting to the user. Report the results as a pass/fail checklist.

### Factual accuracy
- [ ] All claims match actual profile (CLAUDE.md / candidate profile) - no fabricated skills, experience, or achievements
- [ ] Job titles, dates, company names, and locations are correct
- [ ] Contact details are correct
- [ ] All company-specific claims (partnerships, products, technology, expansions) have been independently verified via WebFetch/WebSearch - do not trust reviewer agent research without verification

### Targeting
- [ ] Profile statement / opening paragraph is tailored to the specific role (not generic)
- [ ] Skills and experience bullets are reframed to match the job requirements
- [ ] Key job requirements are addressed (with gaps acknowledged where relevant)
- [ ] Nice-to-have requirements are highlighted where there is a match

### Consistency
- [ ] CV follows the standard 1-page moderncv/banking format
- [ ] Cover letter uses cover.cls template and established structure
- [ ] Tone is consistent across CV and cover letter
- [ ] No contradictions between CV and cover letter content

### Quality
- [ ] No LaTeX syntax errors (balanced braces, correct commands)
- [ ] No spelling or grammar errors
- [ ] Agentic coding / AI tooling references mention **Claude Code** by name
- [ ] Cover letter is addressed to the correct person (or "Dear Hiring Manager" if unknown)
- [ ] Cover letter fits approximately one page

### Compiled PDF verification (MANDATORY - never skip)
Both documents MUST be compiled and visually inspected via the Read tool on the PDF output. "Looks fine in the .tex" is not acceptable - LaTeX page-break decisions are unpredictable. Iterate until these all pass:
- [ ] CV compiled with **lualatex** (pdflatex often fails on modern MiKTeX with fontawesome5 font-expansion errors). Cover letter compiled with **xelatex** (cover.cls requires fontspec).
- [ ] **CV is exactly 1 page** - not 2, not 3
- [ ] **No cramped or cut-off content** - if content doesn't comfortably fit on 1 page, cut lower-relevance material per the relevance-weighted cutting rules rather than shrinking fonts/margins to force a fit
- [ ] **Cover letter is exactly 1 page** - signature block must fit with the body, never overflow
- [ ] **Cover letter bullet font matches body font** - `\lettercontent{}` must not wrap `\begin{itemize}...\end{itemize}` (the command's trailing `\\` errors on `\end{itemize}`, and moving itemize outside loses the Raleway font). Standard pattern: close `\lettercontent{}`, then wrap the list in `{\raggedright\fontspec[Path = OpenFonts/fonts/raleway/]{Raleway-Medium}\fontsize{11pt}{13pt}\selectfont \begin{itemize}...\end{itemize}\par}`

### ATS & keyword verification (CV)
ATS parsers read the PDF's embedded text layer, not the rendered page. Extract it with `pdftotext -layout` and verify what a parser sees. `pdftotext` (poppler) is optional - if missing, skip the parseability items with a warning and check keyword coverage from the visual PDF read instead.
- [ ] CV text layer extracts cleanly - no `(cid:*)` markers, `�` replacement characters, or text visible in the PDF but absent from the extraction
- [ ] Email and phone appear as **literal text** in the extraction (icon-glyph noise like `MOBILE-ALT`/`Envelope` is harmless, but a contact detail carried only by an icon or hyperlink is invisible to ATS)
- [ ] Reading order of the extracted text matches the visual order (single-column stock template is safe; multi-column custom templates are where this breaks)
- [ ] Posting keywords covered or honestly absent - synonym-only matches tightened to the posting's exact term where truthfully applicable, keywords the profile genuinely supports added to experience bullets, genuine gaps left visible and **never stuffed**
