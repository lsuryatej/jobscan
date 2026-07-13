# Daily Job Aggregation Log

Tracks results from the daily Gmail job-alert aggregation run: search window, ranked
job table, consulting/body-shop flags, and the cold-outreach drafts generated for the
top 5 companies each day.

**Candidate stack:** GCP, Vertex AI, BigQuery, Kubeflow, Airflow, LightGBM, XGBoost, Python.
2 years production ML at a UK bank. IIT Guwahati.

**Scoring:** sum of 3 sub-scores (1-5 each) — Role fit (ML Engineer/MLOps/Applied AI/Data
Scientist = 5, adjacent = 3, off-target = 1), Location (Delhi/GGN/Noida = 5, Hyderabad = 4,
Remote India = 4, Bangalore = 3, other = 1), Company type (product/fintech/startup = 5,
consulting/outsourcing = 2, other corporate/GCC = 3). Max score = 15.

---

## 2026-07-08

**Search window:** last 48 hours (2026-07-06 12:37 IST → 2026-07-08 12:37 IST)
**Sources searched:** LinkedIn job alert emails (`jobalerts-noreply@linkedin.com`,
`jobs-noreply@linkedin.com`) and Naukri (`naukri.com`, subject "job alert" /
"recommended jobs"). **No Naukri job-alert emails with listings were found in this
window** — only a Naukri promotional/engagement email (no job cards), which was excluded.
All 20 ranked jobs below come from LinkedIn job alert digests.

Raw emails scanned: 9 distinct LinkedIn job-alert digest threads (some duplicated across
multiple alert triggers), yielding 39 unique job postings (deduped by Company + Role)
after filtering out non-job-alert LinkedIn emails (application confirmations, engagement/
newsletter emails, invitation notifications).

### Ranked Top 20

| Rank | Job Title | Company | Location | Source | Apply Link |
|---|---|---|---|---|---|
| 1 | Applied Data Scientist | dunnhumby | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437748079) |
| 2 | Data Scientist | NEMA AI | South Delhi | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4436520433) |
| 3 | Associate Data Scientist | TriNet | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437174315) |
| 4 | Gen AI Engineer | Experian | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4418958775) |
| 5 | AI/ML Engineer | Optum India | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4434223764) |
| 6 | AI/ML Engineer -Tech Lead | State Street | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437133714) |
| 7 | Machine Learning Engineer | Helfie.AI | Greater Hyderabad Area | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4433935249) |
| 8 | Data Scientist (ML/AI) | Philips | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4423244065) |
| 9 | Machine Learning Engineer | Toyota Automated Logistics | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437169500) |
| 10 | Software Engineer, Machine Learning | HARMAN India | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4433963822) |
| 11 | Data Scientist II - VR Performance Analytics | Expedia Group | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4436246042) |
| 12 | Associate - Data Scientist | United Airlines India Knowledge Center | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437425413) |
| 13 | AI Developer | Ciena | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4436234134) |
| 14 | Associate Data Scientist - Enterprise & Reporting | Circle K | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4436529087) |
| 15 | Senior Associate — Data Scientist, Applied AI/ML | JPMorganChase | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437456730) |
| 16 | AI ML Engineer | Optum India | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437479077) |
| 17 | AI & Automation Associate | NeoFinity | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4436203398) |
| 18 | Gen AI Engineer ⚠️ consulting | BigStep Technologies | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4434518783) |
| 19 | Data Scientist ⚠️ consulting | Softkode Technologies | New Delhi | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4433964604) |
| 20 | ML Engineer | Clean Harbors | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4423595925) |

⚠️ **Consulting/body-shop roles flagged in this batch (skip fast unless desperate):**
BigStep Technologies (#18), Softkode Technologies (#19). Also present in the wider
39-job pool but ranked outside the top 20: PwC Acceleration Center India, Bain & Company,
Deloitte, Luxoft, Accenture in India, EY, L.E.K. Consulting, PwC India, Thought Pilot,
IBM, Infosys — all scored down via the company-type sub-score (2/5) and mostly bumped
further down by weak role fit.

### Top 5 companies → cold outreach drafts

Drafts were created in Gmail (not sent) for the top 5 *distinct* companies from the
ranked list: **dunnhumby, NEMA AI, TriNet, Experian, Optum India**.

| Company | Role targeted | Draft subject | Recipient in draft |
|---|---|---|---|
| dunnhumby | Applied Data Scientist | ML Engineer - Suryatej - dunnhumby | `recruiter@dunnhumby.com` (placeholder — replace with a real recruiter's address before sending) |
| NEMA AI | Data Scientist | ML Engineer - Suryatej - NEMA AI | `talent@nemaai.com` (placeholder — unverified domain, replace before sending) |
| TriNet | Associate Data Scientist | ML Engineer - Suryatej - TriNet | `recruiter@trinet.com` (placeholder — replace before sending) |
| Experian | Gen AI Engineer | ML Engineer - Suryatej - Experian | `recruiter@experian.com` (placeholder — replace before sending) |
| Optum India | AI/ML Engineer | ML Engineer - Suryatej - Optum India | `recruiter@optum.com` (placeholder — replace before sending) |

**Note on labeling:** the `job-outreach` Gmail label could not be created/applied this
run — the connected Gmail account's OAuth grant allows creating drafts but returned a
403/scope error on label management. Find the 5 drafts by subject prefix `ML Engineer -
Suryatej -` in Gmail Drafts until the label issue is resolved (re-authorize the Gmail
connector with label-management scope, then label them manually or re-run).

**Also flagged:** a stray test draft ("test draft - please ignore", thread
`19f41c4d25872fd5`) was created while probing the Gmail connection issue above and
could not be trashed due to the same scope error — delete it manually from Drafts.

---

## 2026-07-13

**Search window:** last 48 hours (2026-07-11 ~04:37 IST → 2026-07-13 ~00:37 IST)
**Sources searched:** LinkedIn job alert emails (`jobalerts-noreply@linkedin.com`,
`jobs-noreply@linkedin.com`) and Naukri (`naukri.com`, subject "job alert" /
"recommended jobs"). **No Naukri job-alert emails were found in this window.** All 20
ranked jobs below come from LinkedIn.

Raw emails scanned: 12 distinct LinkedIn threads in the window — 1 was a "reacted to
this post" social notification (excluded, not a job alert) and 11 were job-alert digests
or saved/viewed-job reminders. Those 11 threads yielded 69 individual job listings, which
deduped by Company + Role (and after excluding 2 Executive Assistant postings as clearly
off-target on role) came to **67 unique job postings** considered for ranking.

### Ranked Top 20

| Rank | Job Title | Company | Location | Source | Apply Link |
|---|---|---|---|---|---|
| 1 | Research Engineer - Applied AI/ML | ixigo | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439061772) |
| 2 | Artificial Intelligence Engineer | SKV (Studiokon Ventures Private Limited) | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439000797) |
| 3 | Forward Deployed Engineer - Gen AI & Voice AI (Backend Engineer) | Blue Machines AI | Delhi | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4438886777) |
| 4 | AI/ML Engineer -Tech Lead | State Street | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437133714) |
| 5 | Machine Learning Engineer | Helfie.AI | Greater Hyderabad Area | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4433935249) |
| 6 | Associate Data Scientist | TriNet | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437174315) |
| 7 | Data Science Associate | The Depository Trust & Clearing Corporation (DTCC) | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439046946) |
| 8 | Applied AI Engineer | Convatec | Greater Hyderabad Area | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439091242) |
| 9 | Artificial Intelligence Engineer | Blend | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4425626254) |
| 10 | Machine Learning Engineer | S&P Global | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4434607893) |
| 11 | Associate AI/ML Engineer | Optum India | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4439044122) |
| 12 | Adv. Data Scientist II, SIP | Invesco | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4438665939) |
| 13 | Artificial Intelligence Engineer | Ameriprise Financial Services, LLC | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4435883622) |
| 14 | Associate - AI Engineer (CTE) | Tech Economy | Delhi | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4438319649) |
| 15 | AI Engineer - Agentic AI & Automation | LUXASIA | Delhi | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4438631482) |
| 16 | Applied Scientist I | Amazon Science | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4412834723) |
| 17 | Associate AI/ML Engineer – Predictive Maintenance | Boeing | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4435943294) |
| 18 | Applied AI/ML Senior Associate | JPMorganChase | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4438881311) |
| 19 | MLOps Engineer (Bangalore, KA, IN, 560037) | Vestas | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4438916474) |
| 20 | Applied Data Scientist — Medical AI & Model Fine Tuning | Clinvvo | Greater Bengaluru Area | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4435976099) |

⚠️ **Consulting/body-shop/staffing roles flagged in the wider 67-job pool (skip fast,
none made the top 20):** EXL (2 postings), UST (3 postings: ML Engineer I, MLOps
Engineer, AI Engineer), "Jobs Opportunity" generic recruiter postings (3), Quanteon
Solutions, ARNsofttech, AVP Vigilant Technology, Jade Global, Maganti IT Resources,
Viraaj HR Solutions, Teamware Solutions, Asian Hires, Innova ESI, Adept Global,
SourcingXPress, Axtria - Ingenious Insights, RZR, ANSR, CloudSutra — all scored down via
the company-type sub-score (2/5) for being staffing/outsourcing/consulting shops.

### Top 5 companies → cold outreach drafts

Drafts were created in Gmail (not sent) for the top 5 *distinct* companies from the
ranked list: **ixigo, SKV (Studiokon Ventures), Blue Machines AI, State Street,
Helfie.AI**.

| Company | Role targeted | Draft subject | Recipient in draft |
|---|---|---|---|
| ixigo | Research Engineer - Applied AI/ML | ML Engineer - Suryatej - ixigo | `recruiter@ixigo.com` (placeholder — replace with a real recruiter's address before sending) |
| SKV (Studiokon Ventures) | Artificial Intelligence Engineer | ML Engineer - Suryatej - SKV (Studiokon Ventures) | `careers@studiokonventures.com` (placeholder — unverified domain, replace before sending) |
| Blue Machines AI | Forward Deployed Engineer - Gen AI & Voice AI | ML Engineer - Suryatej - Blue Machines AI | `talent@bluemachines.ai` (placeholder — replace before sending) |
| State Street | AI/ML Engineer -Tech Lead | ML Engineer - Suryatej - State Street | `recruiter@statestreet.com` (placeholder — replace before sending) |
| Helfie.AI | Machine Learning Engineer | ML Engineer - Suryatej - Helfie.AI | `talent@helfie.ai` (placeholder — replace before sending) |

**Note on labeling:** same recurring issue as 2026-07-08 — the connected Gmail
account's OAuth grant allows creating drafts (read + draft-create scopes) but
`create_label` still returns a token re-authorization error, so the `job-outreach`
label could not be created or applied this run either. Find the 5 drafts by subject
prefix `ML Engineer - Suryatej -` in Gmail Drafts. This needs a one-time
re-authorization of the Gmail connector (with label-management scope) from the
claude.ai connector settings to fix permanently.
