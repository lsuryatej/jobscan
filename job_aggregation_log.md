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

## 2026-07-10

**Search window:** last 48 hours (2026-07-08 ~04:36 IST → 2026-07-10 ~06:06 IST)
**Sources searched:** LinkedIn job alert emails (`jobalerts-noreply@linkedin.com`,
`jobs-noreply@linkedin.com`) and Naukri (`naukri.com`, subject "job alert" /
"recommended jobs"). **No Naukri job-alert emails were found in this window.**
All jobs below come from LinkedIn job-alert digests, "jobs picked for you," and
similar-jobs notifications.

Raw emails scanned: 18 LinkedIn threads in the window; 6 were excluded as
non-job-alert noise (application-viewed/sent confirmations, an engagement/reactions
digest). The remaining 12 job-alert/digest emails yielded 59 unique job postings
(by LinkedIn job ID), 57 after deduping identical Company + Role combinations
(e.g. duplicate "AI Engr I at Honeywell Technologies" postings, duplicate "Data
Engineer at Aeris" postings across locations).

### Ranked Top 20

| Rank | Job Title | Company | Location | Source | Apply Link |
|---|---|---|---|---|---|
| 1 | Senior Analyst-Data Science | American Express | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4436877141) |
| 2 | Machine Learning Ops Engineer | Inovalon | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4362256862) |
| 3 | Applied Data Scientist | dunnhumby | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437748079) |
| 4 | Associate Data Scientist | Amgen | Hyderabad, Telangana, India | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4433337253) |
| 5 | Machine Learning Engineer | Helfie.AI | Greater Hyderabad Area | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4433935249) |
| 6 | Associate AI/ML Engineer | Optum India | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4438135722) |
| 7 | AI/ML Engineer | Optum India | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4434223764) |
| 8 | Machine Learning Engineer | S&P Global | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4434607893) |
| 9 | AI/ML Engineer -Tech Lead | State Street | Hyderabad | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437133714) |
| 10 | Associate Data Scientist - Enterprise & Reporting | Circle K | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4436529087) |
| 11 | Associate - Data Scientist | United Airlines India Knowledge Center | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437425413) |
| 12 | Data Scientist | Affluense | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4436869995) |
| 13 | Data Scientist II - VR Performance Analytics | Expedia Group | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4436246042) |
| 14 | Data Scientist | Fast Code AI | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4436561944) |
| 15 | Senior Associate — Data Scientist, Applied AI/ML | JPMorganChase | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4437456730) |
| 16 | Data Scientist - LLM Training and Fine Tuning | Prismforce | Bengaluru, Karnataka, India | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4436948519) |
| 17 | Data Scientist | TWID | Bengaluru | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4436579954) |
| 18 | Data Engineer | Aeris | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4422482257) |
| 19 | Data Engineer (AI) | Gresham | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4411883088) |
| 20 | AI Engineer - AI, Data & Platforms | KKR | Gurugram | LinkedIn | [Apply](https://www.linkedin.com/jobs/view/4422277100) |

⚠️ **Consulting/body-shop roles flagged (skip fast unless desperate):** none landed
in today's top 20. In the wider 57-job pool, ranked outside the top 20 and scored
down via the company-type sub-score (2/5): Portage Point Partners (#28, financial
advisory), Trigent Software - Professional Services (#29, IT staffing), Accenture
in India (#30), GlobalLogic (#33), Luxoft (#35), Bain & Company (#42 and #54, two
separate roles), BigStep Technologies (#43), Mercer (#44), Deloitte (#47), Prospect
Infosystem Inc. (#52), and PwC Acceleration Center India (#55).

Also excluded from the ranking pool as off-target on role fit (score 1): "AI
Developer - Salesforce Admin" at Sitetracker, "Associate Software Developer" at
Advance Auto Parts India, and "Associate – Data Ops & Estimations" at Bain &
Company. A batch of Amsterdam-based roles (Booking.com, TomTom, Mistral, Xomnia,
Da Vinci, Elsevier, Cocoroco.com, Planner 5D) surfaced via a "similar jobs" digest
but scored low on location (1/5, non-India) and were excluded from the top 20.

### Top 5 companies → cold outreach drafts

Drafts were created in Gmail (not sent) for the top 5 *distinct* companies from the
ranked list: **American Express, Inovalon, dunnhumby, Amgen, Helfie.AI**.

| Company | Role targeted | Draft subject | Recipient in draft |
|---|---|---|---|
| American Express | Senior Analyst-Data Science | ML Engineer - Suryatej - American Express | `recruiting@aexp.com` (placeholder — replace with a real recruiter's address before sending) |
| Inovalon | Machine Learning Ops Engineer | ML Engineer - Suryatej - Inovalon | `recruiting@inovalon.com` (placeholder — replace before sending) |
| dunnhumby | Applied Data Scientist | ML Engineer - Suryatej - dunnhumby | `recruitment@dunnhumby.com` (placeholder — replace before sending) |
| Amgen | Associate Data Scientist | ML Engineer - Suryatej - Amgen | `recruiting@amgen.com` (placeholder — replace before sending) |
| Helfie.AI | Machine Learning Engineer | ML Engineer - Suryatej - Helfie.AI | `careers@helfie.ai` (placeholder — unverified domain, replace before sending) |

**Note on labeling:** the `job-outreach` Gmail label could not be created this run
either — `create_label` returned "MCP server Gmail requires re-authorization (token
expired)," the same recurring scope issue noted on 2026-07-08. Drafts were created
successfully; find them by subject prefix `ML Engineer - Suryatej -` in Gmail
Drafts until the Gmail connector is re-authorized with label-management scope,
then label them manually (or re-run this step once fixed).
