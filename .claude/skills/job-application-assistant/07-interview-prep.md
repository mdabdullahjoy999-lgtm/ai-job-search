---
framework_version: 1.0.0
---

# Interview Preparation Guide

<!-- SETUP: STAR examples are personalized by running /setup based on your actual experience -->

## STAR Format

Structure answers as: **Situation** (context), **Task** (your responsibility), **Action** (what you did), **Result** (outcome).

Keep answers to 1-2 minutes. Be specific. End with what you learned or would do differently.

## Ready-Made STAR Examples

### 1. ICU Readmission & Mortality Prediction Dissertation (End-to-end ML ownership under ambiguity)
**S:** Needed to scope and deliver an MSc dissertation from a broad brief — predicting ICU readmission and mortality using the MIMIC-IV v3.1 clinical dataset (400,000+ records) — with no prior fixed research questions.
**T:** Define a rigorous, defensible research design, build the full ML pipeline, and produce a clinically credible, TRIPOD+AI-compliant analysis, working independently under academic supervision.
**A:** Structured the ambiguous brief into three fixed research questions (pooled readmission, pooled mortality, sex-stratified mortality). Built the cohort via BigQuery across six clinical tables, engineered 100+ features (SOFA, Charlson, OASIS), evaluated 8 algorithms with StratifiedGroupKFold cross-validation, used cost-sensitive learning instead of SMOTE to protect calibration, tuned with Optuna, and applied SHAP for interpretability.
**R:** Achieved AUPRC 0.65+ with a fully interpretable, calibration-aware pipeline reported to TRIPOD+AI standards.
**Use for:** "Tell me about a time you had to bring structure to an ambiguous problem", "Describe a complex technical project you owned end-to-end", "How do you approach model evaluation beyond accuracy?"

### 2. BCG X Data Science Virtual Experience (Translating a model into a business decision)
**S:** Given a live-style consulting brief: assess churn risk for 14,606 SME energy accounts (9.72% churn rate) and turn the analysis into a business recommendation.
**T:** Scope which client data mattered, build a predictive model, and communicate findings — including limitations — to a non-technical business audience.
**A:** Engineered 61 features from consumption, pricing, and tenure data; trained a Random Forest classifier; identified that consumption and tenure outweighed price sensitivity as churn drivers.
**R:** Delivered a BCG-pyramid-structured executive summary that didn't just report the 0.669 ROC-AUC score — it explicitly flagged the model's low recall (~9%) as a deployment blocker, prioritizing honest business communication over a flattering headline number.
**Use for:** "Tell me about a time you had to communicate a technical limitation to stakeholders", "Describe how you turn a model into a business recommendation", "Give an example of prioritizing honesty over a polished result"

### 3. Merchandising Data Assistant — Demand Forecasting (Delivering measurable business impact)
**S:** Joined Quest Tex Solutions with manual, error-prone SKU-level demand tracking across 200+ products, causing inconsistent overstock costs.
**T:** Build a more reliable forecasting approach and automate the reporting that stakeholders relied on.
**A:** Engineered Python and Excel ETL pipelines for the 200+ SKUs; built a statistical demand-forecasting model; developed Power BI dashboards for recurring stakeholder reporting.
**R:** Reduced manual processing time by 40%, improved forecast accuracy by 15%, cut overstock costs by £8,000/month, and maintained 99.2% data quality across 6+ regular reports to 15+ stakeholders.
**Use for:** "Tell me about a time you delivered measurable business impact", "Describe a project where you owned something from data to stakeholder-facing output", "How do you ensure data quality?"

### 4. Sam Altman YouTube Comment NLP Pipeline (Recovering from a flawed first attempt)
**S:** An earlier attempt at this analysis was flawed — it exposed an API key — and needed to be rebuilt from scratch.
**T:** Rebuild a full comment-analytics pipeline correctly and securely, from data collection through to insight generation.
**A:** Rebuilt the pipeline using the YouTube Data API v3 properly, collecting 47,982 comments across 54 videos, refining to 13,648 English comments via a multi-stage NLP pipeline (VADER sentiment, NRCLex emotion detection, LDA topic modeling).
**R:** Delivered 5 visualizations identifying 58% negative sentiment polarization, framed around actionable insights for a PR-firm audience.
**Use for:** "Tell me about a mistake you made and how you recovered", "Describe a time you had to redo work", "How do you handle security/credentials in your projects?"

<!-- Add more STAR examples as needed. Aim for 4-6 covering different competencies. -->

## Common Tough Questions

### "Why did you leave [previous company]?"
> [PREPARE YOUR ANSWER - be honest, forward-looking, no negativity about former employer]

### "You don't have [specific skill/experience]."
> [PREPARE YOUR ANSWER - acknowledge the gap, bridge to adjacent experience, show willingness to learn]

### "Where do you see yourself in 5 years?"
> [PREPARE YOUR ANSWER - show ambition aligned with the role's growth path]

### "What's your biggest weakness?"
> [PREPARE YOUR ANSWER - genuine weakness with concrete mitigation strategy]

### "Why this company specifically?"
> Customize per company. Must reference: specific projects, company values, market position, or team structure. Never give a generic answer.

## Questions You Should Ask Interviewers

### About the Role
- "What does a typical week look like in this role?"
- "What would success look like in the first 6 months?"
- "What's the biggest challenge the team is facing right now?"

### About the Team
- "How big is the team, and how do you divide work?"
- "What does the development/project lifecycle look like, from idea to production?"
- "How do you onboard new team members?"

### About Tech & Growth
- "What's your current tech stack for [relevant area]?"
- "Is there room to grow into more architectural or strategic decisions?"
- "How does the team stay current with new tools and methods?"

### About Culture (use these to prevent disappointment)
- "How would you describe the team culture?"
- "What does professional development look like here?"
- "Is there flexibility for remote/hybrid work?"
- "What's the balance between development/new projects and maintenance work?"
- "How would you describe the leadership style in this team?"
- "What do people who thrive here have in common?"

## Phone/Video Interview Tips
- Have STAR examples written out (use this file)
- Keep a glass of water nearby
- Smile when speaking (it changes your tone)
- Ask for clarification if a question is vague
- It's OK to take 5 seconds to think before answering
- End with: "Is there anything else you'd like to know about my background?"

## After the Application (Best Practice)

### Follow-Up Etiquette
- **Don't call to "stand out"** or to learn more about the role post-submission - this risks a negative impression
- If the employer specified a timeline, respect it and wait
- If no timeline was given and significant time has passed (2+ weeks), a brief call to ask about status is acceptable
- If you have genuinely new, relevant information to share, a short follow-up is fine

### Thank-You Notes
- When you receive any update (interview invitation, rejection, or status update), send a brief thank-you message
- Express appreciation for their time and the process
- Keep it short (2-3 sentences)

## Roleplay Guidelines
When the user asks for interview practice:
1. Ask which role/company to simulate
2. Start with easy warm-up questions ("Tell me about yourself")
3. Progress to role-specific technical questions
4. Include 1-2 behavioral questions using the competencies from the job posting
5. End with a tough question or curveball
6. After each answer, give brief feedback: what worked, what to sharpen
7. Suggest which STAR example would work best for each question
